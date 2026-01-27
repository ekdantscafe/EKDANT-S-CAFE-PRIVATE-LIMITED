# 🔐 Security Documentation

## Admin Password Security

### Overview
The admin panel password is now **securely protected** using SHA-256 cryptographic hashing. The actual password is **never stored** in the code - only its hash is stored.

### Why This is Secure

1. **No Plaintext Storage**: The password is not visible in the source code
2. **One-Way Hashing**: SHA-256 is a one-way cryptographic function - you cannot reverse the hash to get the password
3. **Secure Comparison**: Passwords are compared by hashing the input and comparing hashes, not plaintext
4. **Browser Security**: Uses the Web Crypto API for secure hashing

### Current Password

The current admin password is: **`ekdant2026`**

⚠️ **IMPORTANT**: Change this password immediately for production use!

---

## How to Change the Admin Password

### Method 1: Using the Password Hash Generator (Recommended)

1. Open `password-hash-generator.html` in your web browser
2. Enter your new desired password
3. Click "Generate Hash"
4. Copy the generated hash
5. Open `script.js` in your code editor
6. Find this line (around line 159):
   ```javascript
   const ADMIN_PASSWORD_HASH = '8c6976e5b5410415bde908bd4dee15dfb167a9c873fc4bb8a81f6f2ab448a918';
   ```
7. Replace the hash value with your newly generated hash
8. Save the file
9. **Remember your new password!** (Store it securely)

### Method 2: Using Browser Console

1. Open your browser's Developer Tools (F12)
2. Go to the Console tab
3. Paste this code (replace 'YourNewPassword' with your actual password):
   ```javascript
   async function generateHash(password) {
       const encoder = new TextEncoder();
       const data = encoder.encode(password);
       const hashBuffer = await crypto.subtle.digest('SHA-256', data);
       const hashArray = Array.from(new Uint8Array(hashBuffer));
       const hashHex = hashArray.map(b => b.toString(16).padStart(2, '0')).join('');
       console.log('Your hash:', hashHex);
   }
   generateHash('YourNewPassword');
   ```
4. Copy the generated hash
5. Update `script.js` as described in Method 1

---

## Security Best Practices

### ✅ DO:
- Change the default password immediately
- Use a strong, unique password (mix of letters, numbers, symbols)
- Keep your password confidential
- Use the password hash generator tool
- Store your password in a secure password manager

### ❌ DON'T:
- Share your admin password with unauthorized users
- Use simple or common passwords
- Store the password in plaintext anywhere
- Reuse passwords from other services
- Share the hash generator tool with untrusted users

---

## How It Works

### Password Verification Process:

1. User enters password in the admin panel
2. Password is hashed using SHA-256 algorithm
3. The generated hash is compared with the stored hash
4. If hashes match → Access granted ✓
5. If hashes don't match → Access denied ✗
6. Password field is cleared for security

### Technical Details:

- **Algorithm**: SHA-256 (Secure Hash Algorithm 256-bit)
- **Implementation**: Web Crypto API (`crypto.subtle.digest`)
- **Hash Length**: 64 hexadecimal characters (256 bits)
- **Collision Resistance**: Cryptographically secure
- **Performance**: Asynchronous hashing (non-blocking)

---

## Troubleshooting

### Problem: "Incorrect password!" message
**Solution**: 
- Verify you're using the correct password
- Check for typos or extra spaces
- Ensure Caps Lock is off
- If you forgot the password, generate a new hash and update script.js

### Problem: Admin panel not working
**Solution**:
- Clear browser cache and reload
- Check browser console for errors (F12)
- Verify script.js is properly loaded
- Ensure the hash in script.js is valid (64 hex characters)

### Problem: Need to reset password
**Solution**:
1. Use password-hash-generator.html to create a new hash
2. Update the ADMIN_PASSWORD_HASH in script.js
3. Save and reload the page

---

## Additional Security Recommendations

For production environments, consider:

1. **Backend Authentication**: Move authentication to a server-side solution
2. **HTTPS**: Always use HTTPS to encrypt data in transit
3. **Rate Limiting**: Implement login attempt limits
4. **Session Management**: Add session timeouts
5. **Two-Factor Authentication**: Add 2FA for extra security
6. **Audit Logging**: Track admin panel access

---

## Files Related to Security

- `script.js` - Contains the password hash and verification logic
- `password-hash-generator.html` - Tool for generating new password hashes
- `SECURITY.md` - This documentation file

---

## Support

If you need help with password security or have questions:
1. Review this documentation
2. Check the password-hash-generator.html tool
3. Consult the troubleshooting section above

---

**Last Updated**: January 2026  
**Security Level**: Client-Side Hashing (Suitable for low-security applications)

⚠️ **Note**: For high-security applications, implement server-side authentication with proper database storage and additional security measures.
