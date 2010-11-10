Heroku Auto Emailer
===================

Send an email automatically every other Wednesday using Heroku.

Automated emails in 10 seconds
------------------------------

    $ git clone git://github.com/johndbritton/heroku-auto-emailer.git heroku-auto-emailer
    $ cd heroku-auto-emailer
    $ heroku create 
    $ git push heroku master
    $ heroku addons:add sendgrid:free
    $ heroku addons:add cron:daily

Customize
---------

Edit the Rakefile to change subject, from, to, body and message frequency.


Author
------
John Britton - http://www.johndbritton.com
