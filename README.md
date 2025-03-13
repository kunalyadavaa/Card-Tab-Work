# Card-Tab: Bookmark Card Management

Card-Tab is a bookmark card management tool that allows you to freely move bookmarks, add and delete them, categorize websites, and switch between light and dark themes.

## Updates & Features

### **2025.01.09 - New Additions**
- **bookmarks-export-addons** (located in the `bookmarks-export-addons` directory)
- **Tampermonkey script** (located in the `bookmarks export script` directory)
- Two ways to convert Chrome-exported bookmarks into JSON format and save them to KV storage

### **2024.10.30 - Updates**
- Added front-end verification and removed browser log saving. Now, you need to log in again after 15 minutes of inactivity to enhance privacy.
- Bookmarks are automatically backed up before entering settings, with the latest 10 backups saved in KV storage.
- Slight changes to the color scheme.

### **2024.10.26 - Fixes**
- Replaced the original interface for obtaining website icons:
  - **Old:** `https://favicon.zhusl.com/ico?url=` (seems to be invalid)
  - **New:** `https://www.faviconextractor.com/favicon/`
  - **Backup:** `https://api.iowen.cn/favicon`
- Thanks to the authors of these interfaces for providing services.

### **2024.09.17 - Update**
- Adapted to mobile phones

### **2024.09.14 - Update**
- **Fixed:**
  - Bookmark display issue caused by the 'Delete Category' operation
  - 'Delete Category' button being hidden after clicking
- **Added:**
  - Website icons
  - Operation log

### **2024.09.09 - Update**
- Added private bookmarks (visible after logging in)
- Added website category management (now possible to add/delete categories via UI without editing code)
- Added search box and one-word interface

**Note:** If you deployed the first version (`20240902`), previously saved bookmarks will not be visible after updating the workers' code. You need to re-add the bookmarks.

### **2024.09.02 - Initial Release**
- A lightweight first version, with code stored in `worker-js` file.
- Subsequent updates are placed in the `update-workers.js` file.

## **Demo**
- [Demo Site](https://card.kunalyadavaa.site/)
  
- [Alternate URL](https://demo.linuxdo.nyc.mn)
- **Login Credentials:**
  - **Username:** admin
  - **Password:** admin

### **User Interfaces**
#### Not Logged In
*![Screenshot 2025-03-09 133900](https://github.com/user-attachments/assets/4bd0c79e-00c3-48cf-9b10-940415497861)
*

#### Logged In (Dark Theme)
*![Screenshot 2025-03-09 134627](https://github.com/user-attachments/assets/f7989e61-c72d-4e70-b016-efcd68acc4b0)
*

#### Settings Interface
*![Screenshot 2025-03-09 134755](https://github.com/user-attachments/assets/6aee7045-1fb7-43aa-8b7f-cdab3f38166a)
*

## **Deployment Guide**
### Deployment can be completed in 5 steps:

1. **Log in or Signup to Cloudflare** ([Cloudflare](https://www.cloudflare.com))
   
2. **Go to Worker and pages. Then you will see Hello World Template click on that and then  setup a name and deploy.**

   ![Screenshot 2025-03-09 133929](https://github.com/user-attachments/assets/5749c65d-fd7c-48ba-97c0-67be7759b27e)


3.**Then remove Hello world text and replace it by  `update-workers.js` code copy and paste in vs code to deploy**

![Screenshot 2025-03-09 134021](https://github.com/user-attachments/assets/902ad6dc-193c-4753-b692-f182c8eb263f)

   
4.  Create a Worker and copy the `update-workers.js` code to deploy
  


5. **Create a new KV storage named `CARD_ORDER`.**

6. **Set an environment variable for backend management password.**
   - Variable Name: `ADMIN_PASSWORD`
   - Value: Replace `your_password` with your actual password.

7. **Bind the `CARD_ORDER` variable of Workers to the newly created KV storage** to store bookmarks.

8. **Add a domain name.**

## **Final Notes**
Article = http://blog.kunalyadavaa.site/
This project is suitable for lightweight use. Feel free to modify it as needed. If you find it helpful, consider giving it a star ⭐ on GitHub. & support us for more content like this 'buy me a kofi' = https://ko-fi.com/yadavaakunal Thank you!
## **Credits **
Github = https://github.com/hmhm2022
original Repo = https://github.com/hmhm2022/Card-Tab
