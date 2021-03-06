GroupText
=========
GroupText is a privacy-preserving group SMS web application originally developed for the [GCSE Success](http://www.gcsesuccess.org/) tutoring programme. More information is available in [this blog post](http://markwoodbridge.com/2013/09/05/grouptext.html).

It uses the [Nexmo](https://www.nexmo.com/) platform and is built with [Meteor](http://www.meteor.com/), [Iron Router](https://github.com/EventedMind/iron-router), [Moment.js](http://momentjs.com/) and [Bootstrap](http://getbootstrap.com/).

Screenshot
----------
![Screenshot](https://dl.dropboxusercontent.com/u/1120779/GroupText%20Screenshot.png)

Run
---
1. Download and unzip [the latest release](https://github.com/mrw34/grouptext/releases)
1. ```cp settings.template.json settings.json```
1. Set your Nexmo phone number, api\_key and api\_secret
1. Set inbound\_message\_callback to a random string and configure your Nexmo "Callback URL for Inbound Message" to `http://yourdomain.com/message/<inbound_message_callback>`
1. (Optional) Set delivery\_receipt\_callback to a random string and configure your Nexmo "Callback URL for Delivery Receipt" to `http://yourdomain.com/message/<delivery_receipt_callback>`
1. Set the email and name of an initial admin user (autogenerated password is echoed to console on intial startup)
1. ```meteor run --settings settings.json``` or ```meteor deploy --settings settings.json myapp.meteor.com```

Build
-----
```
git clone https://github.com/mrw34/grouptext.git
cd grouptext
mrt install
bower install
```
