Alien smilies for Moodle
========================

This is an example of local plugin for Moodle 2.0 that provides a custom set
of emoticons for the Moodle site. The smiley pictures have been released into
the public domain by their author at

http://commons.wikimedia.org/wiki/Category:Alien_smiley

Installation
------------

1. Copy the plugin into /local/aliens/ folder of your Moodle 2.0 installation
2. Visit the Site administration home page to install the plugin
3. Go to Site administration > Appearance > HTML settings and register the
   smilies from this plugin you want to use (see details below).
4. Make sure you have enabled 'Display emoticons as images' filter

How to register smilies from this plugin
----------------------------------------

Let us say you want to use the file pix/unhappy.png provided by this filter as
an image for the unhappy :-( smiley. Then add a row into the emoticons table at
Site administration > Appearance > HTML settings with the following values:

    +-------+---------------+-------------------+--------------------------+
    |  Text |   Image name  |  Image component  |    Alternative text      |
    +-------+---------------+-------------------+-----------+--------------+
    | :-(   | unhappy       | local_aliens      | sad       | core_pix     |
    +-------+---------------+-------------------+-----------+--------------+

The row says: the image for the emoticon :-( is called ''unhappy'' (with whatever
extension like .png, .gif or .jpg) and is located in /local/aliens/pix/
folder. As an alternative text, use the string 'sad' defined in core Moodle
language file /lang/en/pix.php (or its translation).

If Moodle core does not provide a suitable string for the alternative text,
you can the string provided by the local plugin itself. For example, for the
'sick' emoticon, fill the last two columns with values 'sick' and
'local_aliens' respectively. Then the strings defined in
/local/aliens/lang/XX/local_aliens.php file are used.

Or you can leave the ''Alternative text'' fields blank. In that case, the
value from the first column (that is the emoticon text) is used as alternative
text. For accessibility reasons, we encourage you to provide proper
alternative texts though.

How to localize or customize the alternative texts for emoticon images
----------------------------------------------------------------------

1. Copy the folder /local/aliens/lang/en/local_aliens.php into
   /local/aliens/lang/XX/local_aliens.php where XX is the language code
2. Go to Site administration > Language > Language customization and modify
   the strings in the component you used for emoticon alternative texts

Example: if you used ''sad'' and ''core_pix'' as the alternative text for the
smiley, you want to modify the string ''sad'' in the core component
''pix.php''

Example: if you used ''unhappy'' and ''local_aliens'' as the alternative text
for the smiley, you have to modify the string ''unhappy'' in the local
component ''local_aliens.php''
