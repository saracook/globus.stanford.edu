---
layout: post
news: true
toc: false

title: "macOS Users: Upgrade to Globus Connect Personal 3.2.8 Today!"
excerpt: Do you use macOS Sequoia (macOS 15) or Tahoe (macOS 25)?  There is an important Globus Connect Personal upgrade (version 3.2.8) waiting for you!
---

If you run macOS Sequoia (version 15) or Tahoe (version 25), an important
Globus Connect Personal update was released today!  You should upgrade to
Globus Connect Personal version 3.2.8 as soon as possible.

{% include info-box.html
  icon='desktop'
  header='Running Windows or Linux?'
  content='If you are running Globus Connect Personal on Windows or Linux, you should still upgrade, though it is not as urgent.' 
%} 

## What changed?

We have been receiving occasional reports of macOS users having problems using
Globus Connect Personal.  Affected users would be able to install Globus
Connect Personal, and it would start up OK, but it would not be usable.  In
particular, when trying to browse a Globus Connect Personal installation,
affected users would get the error "Directory Listing Timed Out".

Thanks to reports from users, the Globus developers have
identified an issue with how Globus Connect Personal interacts with macOS'
permissions system.  Globus Connect Personal 3.2.8 fixes the problem.

## What do you need to do?

If you are installing Globus Connect Personal for the first time, you don't
need to do anything special!  Simply follow [our
instructions](/client/install.html), and you will get the latest version.

If you already have Globus Connect Personal installed, but not running, Globus
Connect Personal should automatically check for updates when you next launch it.

If Globus Connect Personal is already running, click on the Globus menu icon
and select *Check For Updates…*.  You should be told that
Globus Connect Personal 3.2.8 is available.

To confirm that the upgrade has been applied, click on the Globus menu icon and
select *About Globus Connect Personal*.  If you are running version 3.2.8
(Build 740) or later, then the upgrade was successful!

{% include info-box.html
  icon='stream'
  header='What about running transfers?'
  content='If you have running transfers, you can still upgrade!  Any in-progress transfers will resume automatically, once the upgrade is complete.' 
%} 
