require 'rubygems'
require 'pony'

task :cron do
  if Date.today.wday == 3 && Date.today.cweek % 2 == 1 then
    Pony.mail :to => 'to-address@example.com',
              :from => 'from-address@example.com',
              :subject => '[Subject] ' + Date.today.to_s,
              :body => "Message here. You can use \n to start a new line!",
              :via => :smtp,
              :via_options => {
                :address        => 'smtp.sendgrid.net',
                :port           => '25',
                :authentication => :plain,
                :user_name      => ENV['SENDGRID_USERNAME'],
                :password       => ENV['SENDGRID_PASSWORD'],
                :domain         => ENV['SENDGRID_DOMAIN']
              }
  end
end
