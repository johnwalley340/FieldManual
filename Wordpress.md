## Wordpress

##### Wordpress User Enumeration
Run this and simply update the URL

	for i in {1..5}; do curl -s -L -i http://www.wordpress-site-to-test.com/?author=$i | grep -E -o "\" title=\"View all posts by [a-z0-9A-Z\-\.]*|Location:.*" | sed 's/\// /g' | cut -f 6 -d ' ' | grep -v "^$"; done


Return to [[-README]]