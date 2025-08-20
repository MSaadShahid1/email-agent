# 📧 Gmail Automation Agent  

This project is a **Python-based automation tool** that connects with Gmail using **Google OAuth2** and allows sending emails from an already logged-in Gmail account securely.  

---

## 🛠 What I Have Done in This Project  

1. **Authentication Setup**  
   - Configured `google_auth_oauthlib.flow` for Gmail authentication.  
   - Used my Chrome/Edge browser’s existing login session (`User Data` path) so I don’t have to log in again every time.  
   - Created a `credentials.json` file from Google Cloud Console (OAuth Client ID).  
   - On first run, the script generates a `token.json` file which stores the access/refresh token securely.  

2. **Browser Profile Integration**  
   - Specified my local browser profile path:  
     ```
     C:\Users\bilal\AppData\Local\Microsoft\Edge\User Data
     ```  
   - Ensured that when Gmail is opened, it uses my **already logged-in account** instead of asking for credentials again.  

3. **Email Sending Logic**  
   - Implemented message creation with subject and body.  
   - Used Gmail API (`googleapiclient.discovery`) to send the message.  
   - Supported both plain text and HTML formats.  

4. **Error Handling**  
   - Handled common login errors like  
     - “This browser or app may not be secure.”  
     - Token expiration and refresh logic.  
   - Ensured that the script automatically refreshes tokens when they expire.  

5. **Project Structure**  
