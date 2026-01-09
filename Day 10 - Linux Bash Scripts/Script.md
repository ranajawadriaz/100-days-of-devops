<pre>
#!/bin/bash

# A. Create the zip archive and save it to the local backup directory
# Format: zip -r [destination_file] [source_folder]
zip -r /backup/xfusioncorp_news.zip /var/www/html/news

# C. Copy the archive to the Remote Backup Server
# Format: scp [file_to_send] [user]@[remote_server]:[remote_path]
scp /backup/xfusioncorp_news.zip clint@172.16.238.16:/backup/
</pre>