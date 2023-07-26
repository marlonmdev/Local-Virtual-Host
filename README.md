# Virtual Host Setup on Windows with XAMPP
 <br>
 <h2>Edit host file</h2>
 <br>
 <code>File Location -> C:/Windows/System32/drivers/etc/hosts</code> 
 <b>Open with VS Code (Recommended) Add this lines and save (VS Code will prompt to Retry to save with Administrator rights)<b>
 <code>
	127.0.0.1   localhost
        127.0.0.1   yoursitename.xyz
 </code>
 <br>
 <h2>Edit httpd.conf</h2>
 <br>
 <code>File Location -> C:/xampp/apache/conf/httpd.conf</code>
 <b>Open file with any text editor and search # Virtual hosts and uncomment the next line and save</b>
 <code>
	# Virtual hosts
	# Include conf/extra/httpd-vhosts.conf
 </code>
 <b>After editing it should look like this</b>
 <br>
 <code>
	# Virtual hosts
	Include conf/extra/httpd-vhosts.conf
 </code>
 <br>
 <h2>Edit httpd-vhosts.conf</h2>
 <br>
 <code>File Location -> C:/xampp/apache/conf/extra/httpd-vhosts.conf</code>
 <br>
 <b>Add this lines and save<b>
 <br>
 <img src="https://github.com/marlonmdev/Local-Virtual-Host/blob/main/thecode.png" alt="code">
 <br>
 <b>Now you can access your local website by typing <code>yoursitename.xyz</code> instead of <code>localhost/your-project-foldername</code> on your browser</b>
