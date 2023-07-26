# Virtual Host Setup on Windows with XAMPP
 <br>
 <em>Edit host file<em>
 <code>File Location -> C:/Windows/System32/drivers/etc/hosts</code> 
 <em>Open with VS Code (Recommended) Add this lines and save (VS Code will prompt to Retry to save with Administrator rights)<em>
 <code>
	127.0.0.1   localhost
        127.0.0.1   yoursitename.xyz
 </code>
 <br>
 <em>Edit httpd.conf</em>
 <code>File Location -> C:/xampp/apache/conf/httpd.conf</code>
 <em>Open file with any text editor and search # Virtual hosts and uncomment the next line and save</em>
 <code>
	# Virtual hosts
	# Include conf/extra/httpd-vhosts.conf
 </code>
 <em>After editing it should look like this</em>
 <br>
 <code>
	# Virtual hosts
	Include conf/extra/httpd-vhosts.conf
 </code>
 <br>
 <em>Edit httpd-vhosts.conf</em>
 <br>
 <code>File Location -> C:/xampp/apache/conf/extra/httpd-vhosts.conf</code>
 <br>
 <em>Add this lines and save<em>
 <br>
 <code>
	<VirtualHost *:80>
        	DocumentRoot "C:/xampp/htdocs"
        	ServerName localhost
        </VirtualHost>
 </code>
 <br>
 <code>
	<VirtualHost *:80>
    		DocumentRoot "C:/xampp/htdocs/your-project-foldername"
    		ServerName yoursitename.xyz
	</VirtualHost>
 </code>
 <br>
 <b>Now you can access your local website by typing <code>yoursitename.xyz</code> instead of <code>localhost/your-project-foldername</code> on your browser</b>
