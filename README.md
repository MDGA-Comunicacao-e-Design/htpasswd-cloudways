# htpasswd-cloudways
How to use htpasswd in Cloudways with Wordpress

## How get the path to the root of your application in Wordpress
You can use this php snippet to print in front-end and copy the path
<code>echo ABSPATH;</code>
It's something like:
- /home/XXXXXX.cloudwaysapps.com/aplicationfolder/public_html/

## Create a password
I use this website: https://hostingcanada.org/htpasswd-generator/ to generate the code to .htpasswd file.

## Add to the application root and it's done
Upload both files to public_html folder and website it's protected.
