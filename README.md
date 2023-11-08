# htpasswd-cloudways
How to use htpasswd in Cloudways with Wordpress

## 1.How get the path to the root of your application in Wordpress
You can use this php snippet to print in front-end and copy the path
<code>echo ABSPATH;</code>
It's something like:
- /home/XXXXXX.cloudwaysapps.com/aplicationfolder/public_html/

### Using Oxygen Builder
- Create a page
- Add a code block
- add echo ABSPATH;
- check the page in front-end

## 2.Create a password
I use this website: https://hostingcanada.org/htpasswd-generator/ to generate the code to .htpasswd file.
- Add the user name
- Add the password
- Generate the file
- Create a file called .htpasswd
- it will be used in the website root
- not upload the file yet

## Add the protection data in .htaccess
- Download the .htaccess
- Add the code below
<code>AuthName "Add your login message here."
AuthType Basic
AuthUserFile path/to/file/.htpasswd
require user name-fo-the-user
ErrorDocument 401 default</code>

Replace <code>name-fo-the-user</code> with the user you use in the previous step
Replace <code>path/to/file/</code> with the path you get in the step 2. The code in this part will be like:
<code>AuthUserFile /home/XXXXXX.cloudwaysapps.com/aplicationfolder/public_html/.htpasswd</code>

## Add to the application root and it's done
Upload both files (.htaccess e .htpasswd)to public_html folder and website it's protected.
