# solarspell-modules
On the DLMS: Copy/paste the solarspell-modules folder and paste it in the same location with the name of the module to created. Let’s assume the module to be created is “voa”. We’ll now be working inside this folder

Copy the folder of content (videos, pdf, etc..) into the voa folder. Name the content folder “content”

Move generate_db.py file into the content folder
Via terminal, navigate to the content folder and run “python generate_db.py”. This command will create a module.db file inside the content folder. ### Move module.db file to backend/db/ folder inside the voa folder 

Place the logo image inside the assets folder and rename it to logo.png (PNG format is recommended, if not available, logo.jpeg should work. Other formats won’t work) 

If there is an about us video, place it in the assets folder and name it to about.mp4 (only .mp4 is allowed)

Edit the index.html file. The change the fourth line that say <base href="/solarspell-modules/"> to <base href="/voa/">. If the library will be hosted on a non-root directory, you’ll need to edit this line to have the correct path. For example, on solarcubed.og: <base href="/health-site/voa/">

Edit the .htaccess file (it is usually hidden, so you can edit it via terminal: sudo nano .htaccess) and change the index.html path to include the name of the module. This line: RewriteRule . /solarspell-modules/index.html [L] should be changed to RewriteRule . /voa/index.html [L]. Again, if the library will be hosted on a non-root directory, you’ll need to edit this line with the subpath. 
Example:  RewriteRule . /health-site/voa/index.html [L] 

That’s it! Now you can use the voa folder as a module and host it on any environment. 
