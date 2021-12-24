Find is one of those commands that are crazy powerful but also overly complicated. I like the find command but it took some practice.

Find comes with all versions of linux and unix so no need to install its already there. 

I will be listed a few examples that will really help in pen testing but it is good for other instances as well. 

The following command will  run find against all files and execute by word count by line and put the value in the {} the \; escapes out to run the script line by line. 

	find  .  -type f -exec wc -l {} \;

Another cool thing you can do with find is get rid of errors in your out put. consider something like permission denied. You can do this by sending those errors to /dev/null

 	find <location> 2>/dev/null

Find by group owner you can use the -group flag
Find by user you can use the  - user flag
Find by size you can use the -size # flag 
**Note:**
c=bits for some reason. so a 71bit file would be -size 71c

Another really cool trick it to find out what file a user can run with privledges. This will allow you to execute a file. However if you can see the executable you can point to the path and write your own call by adding to the path and setting it first. 

Here is the find command to look at all files you can execute as that user.

	find / -perm -u=s -type f 2>/dev/null
	
Return to [[README]]

