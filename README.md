Card-Tab bookmark card management, enter the management mode to freely move bookmark positions, add and delete bookmarks, support custom website classification, support switching dark theme
2025.01.09 Added:
1. bookmarks-export-addons (in the bookmarks-export-addons directory);
2. Tampermonkey script (in the bookmarks export script directory);
Two ways to convert Chrome browser exported bookmarks into json format and save them to KV storage
2024.10.30 Update:
1. Added front-end verification and cancelled the log saving in the browser. Now you need to log in again after more than 15 minutes. Timely logout can make your privacy safer;
2. Bookmarks will be automatically backed up before entering the settings, and the latest 10 backups will be saved in KV;
3. Slightly changed the color scheme.
2024.10.26 Fixes:
The original interface for obtaining website icons https://favicon.zhusl.com/ico?url= seems to be invalid. The replacement interface is https://www.faviconextractor.com/favicon/Project address: [Github] ; another backup interface is https://api.iowen.cn/faviconProject address: [Github] Thanks to the authors of the above interfaces for providing services
2024.09.17 Update:
Adapted to mobile phones
2024.09.14 Update:
Fixed 1. Bookmark display issue caused by 'Delete Category' operation; 2. Issue where the 'Delete Category' button is hidden after being clicked; Added website icon and operation log
2024.09.09 Update:
1. Add private bookmarks, visible after logging in
2. Add website category management. Now you can add and delete website categories through the page without editing the code.
3. Add search box and one-word interface
Note: If you have deployed the first version (20240902) of the navigation, you will not be able to see the previously saved bookmarks after updating the workes code. You need to add the bookmarks again. Please be aware!
2024.09.02 Release (the first version is very light, the code is kept in the worker-js file, and subsequent updates are placed in the update-workers.js file)
Demo site: https://demo.usgk.us.kg Alternate URL: https://demo.linuxdo.nyc.mn Password: admin
Not logged in interface

image
Logged in interface (dark theme)

image
Settings interface

image
Deployment method:
Deployment can be completed in five steps:
1. Log in to Cloudflare: https://www.cloudflare.com , create workers, copy the update-workers code, and then deploy

image
2. Create a new KV storage named CARD_ORDER

image
3. Add an environment variable to set the backend management password. The variable name is ADMIN_PASSWORD, and the value your_password is replaced with your own password.

image
4. Bind the CARD_ORDER variable of workers to the newly created KV storage to store bookmarks

image
5. Add a domain name

image
This project is suitable for lightweight use. Feel free to modify it yourself. If you like it, just click the little star. Thank you!
