# envcare

1 Clone repo and install thru composer

``composer install``

2 Enable git templates (This tells git to copy everything in ~/.git-templates to your per-project .git/ directory when you run git init):

``git config --global init.templatedir '~/.git-templates'``

3 Create a directory to hold the global hooks:

``mkdir -p ~/.git-templates/hooks``

4 Make symlink for `post-checkout`:

``ln -s post-checkout ~/.git-templates/hooks/post-checkout``

5 Make sure the hook is executable.

``chmod a+x ~/.git-templates/hooks/post-checkout``

6 Re-initialize git in each existing repo you'd like to use this in:

``git init``