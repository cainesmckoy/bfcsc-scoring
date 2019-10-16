----------------------
items to fix
----------------------


*for the love of god make the "get - post" aquisition one page to avoid overhead*
    -*if it can be fixed that way; idk how to seperate "get - post" possibly*
    
 *teams logs could probably be displayed through a for loop or two* - instead of directly hardcodng each teams aquisiton to display scores     
    
    


# bfcsc-scoring



teams Webpage(s) needs to be pulled up on a 'neutral machine' (SCOREBOX)



+team1check.php handles team 1 scoring
+team2check.php handles team 2 scoring
+team3check.php handles team 3 scoring

-the duplicate files handles <b>get and post</b> request for scoring machines

+to add more teams check(2/3).php need to be duplicated also

+display only check(2/3).php for corrisponding teams to show live updates

*not built with security in mind sadly (flooding or spoofing possibly?)

+currently running on 777 permissions in /var/www/html, not secure
+owner of most files is www-data, this is most secure 
    -future revisions; secure files. 
            -however there is nothing to directly attack either to my knowledge

-ignore index.html file ( then delete it)

------------------------
scoring engine minutia
------------------------

    -check.php(2/3) will check logs without checking the teams servers too
        -due to the codes function, each team must have a web page (teamXcheckX.php)open from the scoring engine 
        -RUN SCORING ON A NUETRAL MACHINE do not allow teams access to teamXcheckX.php

-If passwords for untangled are changed, notify white team

-if FTP user passwords are changed, notify white team

-DNS requires the server to be up + ftp&HTTP name records *dont notify teams*

-Email based on nameserver resolution
*dont notify teams*

-PING is any machines IP
*dont notify teams*
