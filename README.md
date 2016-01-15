# content_mig
Uses git pre-commit and post-merge hooks to send content from source to destination

##Use case

You want Drupal 8 node, block, user, or menu content transferred from a source to a destination. These hooks help move things that aren't tracked by CMI. The pre-commit hook goes with the source installation and the post-merge hook goes in the destination. Essentially a mysqldump is run on the source and then the MySQL tables are updated on the destination.

##Setup

1.) Download the "pre-commit" file to the source environment and the "post-merge" file to the destination environment<br />
2.) Put files in the hooks directory of your git enabled project so they appear like so:<br />
&nbsp;&nbsp;&nbsp;&nbsp;`.git/hooks/pre-commit`<br />
&nbsp;&nbsp;&nbsp;&nbsp;`.git/hooks/post-merge`<br />
3.) Edit files so the environment specific variables correspond to the correct values for your Drupal application<br />
4.) Make sure the scripts are executable:<br />
&nbsp;&nbsp;&nbsp;&nbsp;`chmod u+x .git/hooks/pre-commit`<br />
&nbsp;&nbsp;&nbsp;&nbsp;`chmod u+x .git/hooks/post-merge`<br />
