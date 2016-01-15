# content_mig
Uses git pre-commit and post-merge hooks to send content from source to destination

##Use case

You want Drupal 8 node, block, user, or menu content transferred from a source to a destination. These hooks help move things that aren't tracked by CMI. Essentially a mysqldump is run on the source when commiting code via git and then the MySQL tables are updated on the destination when merging code (merging branch or git pull). The scripts ask for user import to determine when to export or import content. The scripts also try to find your database connection info by searching settings.php.

##Setup

1.) Download "pre-commit" and "post-merge" files from this repository<br />
2.) Put files in the hooks directory of your git enabled project so they appear like so:<br />
&nbsp;&nbsp;&nbsp;&nbsp;`.git/hooks/pre-commit`<br />
&nbsp;&nbsp;&nbsp;&nbsp;`.git/hooks/post-merge`<br />
3.) Make sure the scripts are executable:<br />
&nbsp;&nbsp;&nbsp;&nbsp;`chmod u+x .git/hooks/pre-commit`<br />
&nbsp;&nbsp;&nbsp;&nbsp;`chmod u+x .git/hooks/post-merge`<br />
