----------------------
items to fix
----------------------
*FTP had bleed over between teams*

*FTP scoring stoped after couple-several hours*

*for the love of god make the "get - post" aquisition one page to avoid overhead*
    -*if it can be fixed that way; idk how to seperate "get - post" possibly*
    
 *teams logs could probably be displayed through a for loop or two* - instead of directly hardcoidng each teams aquisiton to display scores     
    
    


# bfcsc-scoring



teams Webpage(s) needs to be pulled up to 



+team1check.php handles team 1 scoring
+team2check.php handles team 2 scoring
+team3check.php handles team 3 scoring

the duplicate files handles <b>get and post</b> request for scoring machines

+to add more teams check(2/3).php need to be duplicated also

*not built with security in mind sadly
currently running on 777 permissions in /var/www/html
owner of most files is www-data, this is most secure (future revisions; secure files) nothing to particuarly attack either 
-ignore index.html file

------------------------
scoring engine minutia
------------------------
-KEEP THE scoring page for each team up at all times
    -admin-check.php will check logs without checking the teams servers too
        -due to the codes function, each team must have a web page open from the scoring engine to perform 'scoring check' (if the primary team pages are exited, scoring stops) 

-If passwords for untangled are changed, notify white team

-if FTP user passwords are changed, notify white team

-DNS requires the server to be up + ftp&HTTP name records *dont notify teams*

-Email based on nameserver resolution
*dont notify teams*

-PING is any machines IP
*dont notify teams*
