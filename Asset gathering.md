Look for ASN
https://bgp.he.net/


echo <NUMBER> | asnmap -silent | naabu -silent

asnmap - prints the exact ip adresses, naabu - ports.


echo <NUMBER> | asnmap -silent | naabu -silent -nmap-cli 'nmap -sV'
smap - for red team, for makin less noise



git dorking


/[A-Za-z0–9-_]+\.example\.com\/+/ AND (apikey OR api_key OR secret OR password OR credentials OR token OR bearer OR authorization OR client_secret OR client_id OR access_token OR private_key OR ssh-rsa OR ssh-dss OR -----BEGIN OR -----END OR .env OR config OR aws_access_key_id OR aws_secret_access_key OR db_password OR ftp_password OR smtp_password OR auth_token OR bearer_token OR oauth_token OR jwt OR session_token OR s3.amazonaws.com OR s3:// OR .s3.amazonaws.com OR s3-external- OR s3.dualstack. OR s3-website- OR s3.ap OR s3.us OR s3.eu OR s3.ca OR s3.sa)



JS endpoint scrapper
javascript:(function(){var scripts=document.getElementsByTagName("script"),regex=/(?<=(\"|\%27|\`))\/[a-zA-Z0-9_?&=\/\-\#\.]*(?=(\"|\'|\%60))/g;const results=new Set;for(var i=0;i<scripts.length;i++){var t=scripts[i].src;""!=t&&fetch(t).then(function(t){return t.text()}).then(function(t){var e=t.matchAll(regex);for(let r of e)results.add(r[0])}).catch(function(t){console.log("An error occurred: ",t)})}var pageContent=document.documentElement.outerHTML,matches=pageContent.matchAll(regex);for(const match of matches)results.add(match[0]);function writeResults(){results.forEach(function(t){document.write(t+"<br>")})}setTimeout(writeResults,3e3);})();
