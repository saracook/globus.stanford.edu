---
layout:      page
title:       How Do I … ?
description: Describes different data transfer scenarios, and how Globus can help.
permalink: scenarios.html
customjs: ./assets/js/faq.js
toc: false
toc-min: true
---

<p>Everyone who wants to use Globus has to start somewhere, and that place is
here.  You might have been told "Oh, you need to do X", or you might not be
sure what you need to do. This page is for you!</p>

<p>This page contains common Globus scenarios and questions.  Each answer
either contains a direct answer to your question
or a link to a different part of the site.</p>

<p>The entries are grouped into sections: </p>
<ul className="list-unstyled">
  <li><a href="#accountshead">Accounts/Globus ID</a></li>
  <li>Transfers in the browsers via the <a href="#webhead">Globus Web Application</a></li>
  <li>Transfers via <a href="#clienthead">Globus Client</a> software</li>
  <li>Using <a href="#serverhead">Globus Server</a></li>
  <li><a href="#policieshead">Policies and Support options</a></li>
</ul>

<p>After reading here, you should also take a look at the section of the site
specific to your needs: <a href="{{ "accounts.html" | relative_url }}"
name="Globus @ Stanford, Accounts">Accounts</a>, <a href="{{ "client.html" |
relative_url }}" name="Globus @ Stanford, Client">Client</a>, or <a href="{{
"server.html" | relative_url }}" name="Globus @ Stanford, Server">Server</a>.
Finally, if you still have questions, you should reach out to <a href="{{
"support.html" | relative_url }}" name="Globus @ Stanford,
Support">Support</a>.</p>



<h2 id="starthead">Start Here</h2>


{% capture z1 %}

<p>You are probably here because you've heard about Globus and you want to use
it for something!</p>

<p>Globus is used to transfer data between two points.  Those two points could
be a collection of data on a server (such as SCG Lab space), or a personal
endpoint running on a laptop, or a space in the Cloud.</p>

<p>To get started, you should <a href="{{ "accounts/create.html" | relative_url }}"
title="Create a Globus Account">create a Globus account</a> by signing in to
Globus for the first time.  If you have accounts at multiple institutions, you
should also <a href="{{ "accounts.html" | relative_url }}" title="About Globus
Accounts">learn about how Globus accounts work</a>, and how to
<a href="{{ "accounts/link.html" | relative_url }}" title="Link Identities">link
identies together</a>.</p>

<p>(Here is a side challenge: If you have already registered for <a
href="https://library.stanford.edu/orcid-id" title ="Stanford Libraries: My
ORCID">your ORCID iD</a>, try linking it to your Stanford Globus identity!)</p>

<p>Now that you have your Globus account, you need to access either the
collection or the endpoint which has the data you want.
Every endpoint and collection can be identified either by name, or by unique
ID.  You can search for both on the <a href="https://app.globus.org/endpoints"
title="Endpoints">Endpoints search page</a>.  Be careful when searching by
name, because names are not guaranteed to be unique.</p>

<p>If the source or destination is a server, ask the server administrator for a
link to the appropriate collection.  (For example, see <a
href="https://login.scg.stanford.edu/tutorials/data_movement/#globus"
title="Moving Data to/from SCG: Globus">SCG</a> and <a
href="https://www.sherlock.stanford.edu/docs/storage/data-transfer/#globus"
title="Storage on Sherlock: Data Transfer: Globus">Sherlock</a>.)
If you are the server administrator, you can install <a
href="https://docs.globus.org/globus-connect-server/" title="Globus Connect
Server">Globus Connect Server</a> to make your data available.</p>

<p>If the Cloud is one end (or both ends) of the transfer, Stanford supports
using Globus with a number of cloud providers!  <a
href="{{ "cloud.html" | relative_url }}" title="Globus and the Cloud">See the
list of supported cloud services</a>.</p>

<p>If you want to transfer to or from an endpoint (a laptop or desktop), you
can install <a href="{{ "client.html" | relative_url }}" title="Globus Connect
Personal">Globus Connect Personal</a>, giving you access to your endpoint's
storage via Globus.  Globus Connect Personal is smart enough to pause transfers
when you laptop goes to sleep, and is able to cope with unstable network
connections.</p>

<p>Once you have identified both ends of your transfer, you can move data!  The
<a href="https://docs.globus.org/how-to/get-started/#the_file_manager"
title="How To Log In and Transfer Files with Globus">Globus instructions</a>
are very helpful here.</p>

{% endcapture %}
<div class="accordion" id="started">

{% include panel.html
     parent="started"
     id="z1"
     scenario="How do I get started?"
     content=z1
%}

</div>


<div class="section-head d-flex">
<h2 id="accountshead" class="p-2 flex-grow-1">Accounts and Globus ID</h2>
<button class="btn btn-default align-self-end toggle-all p-2" data-segment="scenario"><i class="fa-solid fa-plus"></i> Open All</button>
</div>
<div class="accordion" id="scenario">
  {% capture a1 %}

<p>Creating a Globus account is easy!  If you have never used Globus before,
just go to <a href="{{ "accounts/create.html" | relative_url }}" title="Create
a Globus Account">Create a Globus Account</a> and follow the instructions
there.</p><p>If you have used Globus before (for example, at another
institution), then you should first log in to Globus using that institution's
credentials, and <a href="{{ "accounts/link.html" | relative_url }}"
title="Link Identities">link your Stanford identity</a>.</p>

  {% endcapture %}

  {% include panel.html
     parent="scenario"
     id="a1"
     scenario="How do I get access to Globus?"
     content=a1
  %}


  {% capture a2 %}

<p>Although Globus recognizes that a person can have logins at multiple
institutions, Globus only allows one email address per person per instutition.
If you have an email address at another institution, you can <a href="{{
"accounts/link.html" | relative_url }}" title="Link Identities">Link
Identities</a>.  As for your Stanford identity, whichever email address is your
primary email address is what Globus will see.</p>

<p>See also <em>How do I change my email address in Globus?</em>.</p>

  {% endcapture %}
  {% include panel.html
     parent="scenario"
     id="a2"
     scenario="How do I add a new email address to Globus?"
     content=a2
  %}

  {% capture a3 %}

<p>If you change your Stanford email address (in <a
href="https://accounts.stanford.edu" title="Stanford Accounts">Accounts</a>
or <a href="https://stanfordyou.stanford.edu">StanfordYou</a>),
Globus will get the new email address a few days after the change, once you log
back in to the Globus web site.</p>

<p><em>NOTE:</em> Within Globus, people can be discovered by their identity
(which, for Stanford, is always <em>SUNetID@stanford.edu</em>) or by their
email address.  So, even if you change your email address to something else,
you will still be discoverable in Globus by your SUNetID.</p>

  {% endcapture %}
  {% include panel.html
     parent="scenario"
     id="a3"
     scenario="How do I change my email address in Globus?"
     content=a3
  %}

  {% capture a4 %}

<p><em>Globus ID</em> is a form of identity—similar to your Stanford identity,
but for entities (like labs and departments) and for users who can not get an
identity through other means.  At Stanford, a Globus ID is only needed when you
want to run a Globus Connect Server, because Globus Connect Server instances
can only be owned by entities (like your group), not by people.  Globus IDs are
also used at Stanford by developers, so that their Globus-using applications
are not tied to individuals.</p>

<p>Getting a Globus ID for Globus Connect Server use is covered in the <a
href="{{ "accounts.html" | relative_url }}" title="Globus Accounts">Globus
Accounts</a> section, on the <a href="{{ "accounts/globusid.html" |
relative_url }}" title="Globus ID">Globus ID</a> page.</p>

  {% endcapture %}
  {% include panel.html
     parent="scenario"
     id="a4"
     scenario="How do I get a Globus ID?  Do I even need one?"
     content=a4
  %}

<!-- Next item is a5 -->
</div>
<div class="section-head d-flex">
<h2 id="webhead" class="p-2 flex-grow-1">The Globus Web Site</h2>
<button class="btn btn-default align-self-end toggle-all p-2" data-segment="web"><i class="fa-solid fa-plus"></i> Open All</button>
</div>
<div class="accordion" id="web">
{% capture w1 %}

<p>There are several ways to refer to an endpoint: By short name, by full name,
or by UUID.  You can look up an endpoint on the Globus web site using each of
these identifiers.</p>

<ul> <li>You may have been given an <em>endpoint UUID</em>.  For example,
<code>db57ddde-6d04-11e5-ba46-22000b92c6ec</code> is the UUID (unique ID) of
the ESnet test endpoint in Sunnyvale.  With this unique ID, you can construct
bookmarkable URLs.  For example, if you take the following template…<br />

<pre>https://www.globus.org/app/transfer?destination_id=UUID</pre>

… and replace <code>UUID</code> with the unique ID of the endpoint, you will
have a URL that takes you directly to the transfer screen, with that endpoint
filled in.</li>

<li>Your contact may have given you a <em>short name</em> (like
<code>srcc#oak</code>), or a full name (like <em>Stanford SRCC Oak</em>).  In
both cases, you can go to the
<a href="https://www.globus.org/app/endpoints?scope=all" title="Globus
Endpoints Search">endpoints search page</a>.  Paste in the name you were given,
and the endpoint should appear in the results.</li>

<li>If the endpoint is a shared endpoint, your contact may have given you
explicit access to the endpoint.  In that case, the endpoint will appear in the
<a href="https://www.globus.org/app/endpoints?scope=shared-with-me"
title="Globus Endpoints shared with me">endpoints shared with me</a> list.</li>

</ul>

<p>Once you have located an endpoint, and you click on its name, if you check
the URL of the page you are on, it will look like this…<br />

<pre>https://www.globus.org/app/endpoints/db57ddde-6d04-11e5-ba46-22000b92c6ec/overview</pre>

In the above URL, <code>db57ddde-6d04-11e5-ba46-22000b92c6ec</code> is the
endpoint's unique ID.  You should make a note of it, as that unique ID will
not change (unless the endpoint is deleted).</p>

{% endcapture %}
  {% include panel.html
     parent="web"
     id="w1"
     scenario="Someone gave me access to a Globus endpoint.  How do I access it?"
     content=w1
  %}

{% capture w2 %}
<p>If you are getting a <em>permission denied</em> error when trying to login
to the endpoint, then you should check which credentials you are using.  For
example, endpoints normally only accept logins through their institution.  So,
if you have accounts at Stanford and UC Santa Cruz, your UC
credentials will not let you in to a Stanford endpoint.</p>

<p>(If you have multiple logins to Globus, you might be logged in with the
wrong one.  You should <a href="{{
"accounts/link.html" | relative_url }}" title="Link Identities">Link
Identities</a> to keep that from happening again.)</p>

<p>If your credentials are being accepted; but you are getting <em>permission
denied</em> when you try to do a directory listing, or when you are trying to
transfer data <em>from</em> the endpoint, then the endpoint's configuration is
not allowing access to that directory.  For Globus Connect Server and shared
endpoints, you need to reach out to the endpoint administrator.  For Globus
Connect Personal endpoints, you need to make sure you have configured access to
the directory.  See the Globus Connect Personal <a href="{{
"client/install.html" | relative_url }}" title="Globus Connect Personal
Installation">installation instructions</a> (specifically, the <em>Add Allowed
Paths</em> section).</p>

<p>If you get <em>permission denied</em> errors when transferring data
<em>to</em> an endpoint, then you probably only have read-only access to the
directory.  You either need to talk to the endpoint administrator (for Shared
endpoints and Globus Connect Server endpoints), or check your endpoint
configuration (for Globus Connect Personal endpoints).</p>

{% endcapture %}
  {% include panel.html
     parent="web"
     id="w2"
     scenario="I am getting <em>Permission Denied</em> errors when I try accessing an endpoint.  How do I get access?"
     content=w2
  %}

{% capture w5 %}
<p>Shared endpoints do not exist on their own.  They require a <em>host
endpoint</em>, which is either a Globus Connect Personal endpoint or a Globus
Connect Server endpoint.</p>

<p>If the host endpoint is a Globus Connect Personal endpoint, then you (the
owner of that endpoint) must have access to Globus Plus, which is an optional
Globus feature that is included in Stanford's campus subscription.  <a
href="{{ "client/plus.html" | relative_url }}" title="Globus Connect
Personal: Globus Plus">Read more about Globus Plus</a>.</p>

<p>If your host endpoint is a Globus Connect Server endpoint,
the endpoint administrator may have disabled sharing.  Or, the endpoint might
not be a <em>managed endpoint</em> (which requires access to the Stanford
campus Globus subscription).  In the latter case, the endpoint administrator
should read our guides for Globus Connect Server, specifically the pages on
<a href="{{ "server/pre-install.html" | relative_url }}">Pre-Installation Planning</a> and <a href="{{ "server/finish.html" | relative_url
    }}">Finishing Installation</a>.</p>

<p>The other possible reason is, sharing might not be allowed for the directory
you are trying to share.  For Globus Connect Personal-hosted endpoints, you must
explicitly give Globus Connect Personal access to the directory you wish to
share (or to a parent directory), <em>and sharing must be explicitly
enabled</em>.  For Globus Connect Server-hosted endpoints, the default
configuration is to allow sharing for any directory users can access, but this
can be changed by the Globus Connect Server administrator.</p>

<p>So, if the host endpoint is running Globus Connect Personal, you need to
make sure that you have Globus Plus, and that sharing is explicitly enabled.
And if your host endpoint is running Globus Connect Server, you need to talk
to the administrator of your host endpoint.</p>

{% endcapture %}
  {% include panel.html
     parent="web"
     id="w5"
     scenario="I am getting <em>Permission Denied</em> errors when I try making a shared endpoint.  How do I fix this?"
     content=w5
  %}

{% capture w3 %}

<p>Transfers between endpoints can be paused by endpoint administrators.  If
you got an email saying your transfer has been paused—and you didn't pause the
transfer yourself—then an endpoint administrator (at one or both ends) has
either paused your specific transfer, or has paused all transfers to/from their
endpoint.</p>

<p>Transfers are often paused when endpoint maintenance is taking place.  This
is an alternative to simply letting connections fail (for example, during an
endpoint restart).</p>

<p>Once the pause is lifted, your transfer will resume.  If that does not
happen, you should reach out to the administrator of the endpoint who paused
your transfer.</p>

{% endcapture %}
  {% include panel.html
     parent="web"
     id="w3"
     scenario="I got an email saying my transfer has been paused.  How do I restart it?"
     content=w3
  %}

{% capture w4 %}

<p>In order to transfer files, Globus needs your credentials at both ends of
the transfer.  Giving Globus these credentials is called <em>activating an
endpoint</em>.</p>

<p>For Globus Connect Personal endpoints, and for shared endpoints, activation
is permanent; as long as you have access to the endpoint, no additional
credentials are required.  Globus Connect Server activations are
time-limited.  If your transfer involves a Globus Connect Server endpoint, and
the activation expires during a transfer, your transfer will be paused and you
will get this email.</p>

<p>To solve this problem, <a
href="https://www.globus.org/app/endpoints?scope=in-use" title="Globus In-Use
Endpoints">view your in-use endpoints</a>, and look for any with expired
credentials.  For each endpoint with expired credentials, click on the endpoint
to reactivate it.  Once reactivated, your transfer will automatically
resume.</p>

<p>Transfers already started will continue to attempt to run for up to a day
before being terminated.</p>

{% endcapture %}
  {% include panel.html
     parent="web"
     id="w4"
     scenario="I got an email saying my credentials have expired.  How do I fix it?"
     content=w4
  %}
</div>
<!-- Next item is Globus Client -->
<div class="section-head d-flex">
<h2 id="clienthead" class="p-2 flex-grow-1">The Globus Client (Globus Connect
Personal) and Globus Plus</h2>
<button class="btn btn-default align-self-end toggle-all p-2" data-segment="client"><i class="fa-solid fa-plus"></i> Open All</button>
</div>
<div class="accordion" id="client">
{% capture c1 %}

<p><em>Globus Connect Personal</em> (the proper name for the Globus client
software) is how you can use Globus to transfer files to/from your
laptop/desktop.  The software runs on your system in the background, and gives
you access to transfer files between your system and other Globus
endpoints.</p>

<p>Read more about <a href="{{ "client.html" | relative_url }}"
title="Globus Connect Personal">Globus Connect Personal </a>.</p>

{% endcapture %}
  {% include panel.html
     parent="client"
     id="c1"
     scenario="Someone told me that I need the Globus client.  What even is it?  How do I get it?"
     content=c1
  %}

    {% capture c8 %}

<p>There is no ready-made, pre-approved solution for using Globus with High
Risk data.  Stanford does not have a BAA with Globus or the University of
Chicago, and
Stanford's use of Globus has not undergone a 
<a href="https://uit.stanford.edu/security/dra"
title="How to Request and Complete a Data Risk Assessment, Information Security,
Stanford University IT">Data Risk Assessment</a>.</p>

<p>Your best route forward may be to get your data into a form that is Low or
Moderate Risk, and onto systems that are also Low or Moderate Risk, and install
Globus Connect Personal (or Globus Connect Server) there.  You should reach out
to your IT people to assist, or <a href="mailto:srcc-support@stanford.edu"
title="Contact SRCC">engage with us</a>.</p>

<p>If you are set on using Globus with High Risk data, or on a system that is
exposed to High Risk data, you should expect to
bear substantial costs in both money and time.  <a
href="mailto:srcc-support@stanford.edu" title="Contact SRCC">Reach out</a> if
you are still interested!</p>

    {% endcapture %}
    {% include panel.html
       parent="client"
       id="c8"
       scenario="My laptop or desktop handles High Risk (including PCI / PHI) data.  Can I use Globus on it?"
       content=c8
  %}

{% capture c5 %}

<p>No, but if you firewall outbound connection, then some ports will need to be
opened.  Globus Connect Personal does not need to accept connections from the
outside, except in some cases when performing a transfer between two Globus
Connect Personal endpoints.</p>

<p>Read more in <a href="{{ "client/install.html" | relative_url }}"
title="Installing Globus Connect Personal">the installation instructions</a>.</p>

<p>If you are unable to get your firewall changed, then your last-resort
option is to use the <a href="https://uit.stanford.edu/service/vpn"
title="Stanford University IT VPN Service">Stanford VPN</a>, but you
must use <em>Full Traffic (non-split-tunnel)</em> mode, which sends all
traffic (even non-Stanford traffic) through the VPN.</p>

{% endcapture %}
{% include panel.html
		 parent="client"
		 id="c5"
		 scenario="Do I need to open ports for Globus Connect Personal to work?"
		 content=c5
	%}

{% capture c2 %}

<p>Globus Connect Personal already works to transfer data as quickly as
possible, without making your Internet connection unusable.  That being said,
there are a few things you can do to help make things go faster.</p>

<ul>
<li>Leave your laptop plugged in.  Laptops will agressively power-save when it
detects that you aren't using it.  Plugging in your laptop typically reduces
the level of power-saving.</li>

<li>Use a wired connection.  With a wireless network, your traffic has to
contend with all of the other laptops, phones, and other devices in the local
area, along with other miscellaneous forms of interference (such as
walls and microwaves).  Using a wired connections removes these forms of
interference.</li>

<li>Have good upstream bandwidth.  For example, let's say your desktop is
connected to a small Belkin Gigabit switch, shared with five other lab
members, with one Ethernet cable to the wall.  In that case, you are sharing
a single Gigabit connection.  Ideally, your desktop should be plugged directly
into a network port on the wall, which goes back to a building switch, which
then has at least a 10 Gbps link back to the core network.  If you are in a
residence that does not have ports on the wall (for example, because you have a
cable modem), you should plug in the router.</li>

</ul>

<p>If you routinely need to perform large (multi-TB) data transfers, you should
consider taking advantage of the <a
href="https://srcc.stanford.edu/stanford-research-network-srn" title="Stanford
Research Network">Stanford Research Network</a>.</p>

{% endcapture %}
  {% include panel.html
     parent="client"
     id="c2"
     scenario="I am transferring data to/from my laptop/desktop.  How do I make my transfer go faster?"
     content=c2
  %}

{% capture c4 %}

<p><em>relay.globusonline.org</em> is the link between Globus Connect Personal
and Globus.  All transfer operations—except for the actual data being
transferred—goes through this connection.</p>

<p>Globus Connect Personal must be able to make outbound connections to
relay.globusonline.org on TCP port 2223.  To fix this, you will need to reach out to your IT person. For students (undergrads and grads), reach out to <a href="https://thehub.stanford.edu/services/student-technical-support">Student Technical Support</a> at the <a href="https://thehub.stanford.edu/">Lathrop Learning Hub</a>.  For everyone else, go to your <a
href="https://web.stanford.edu/group/networking/dist/sunet.reports/LNA.html"
title="Local Network Administrators by Department">LNA</a>.</p>

<p>If you are unable to get your firewall changed, then your last-resort
option is to use the <a href="https://uit.stanford.edu/service/vpn"
title="Stanford University IT VPN Service">Stanford VPN</a>, but
you must use <em>Full Traffic (non-split-tunnel)</em> mode, which sends all
traffic (even non-Stanford traffic) through the VPN.</p>

<p>Transfers already started will continue to attempt to run for up to a day
before being terminated.</p>

{% endcapture %}
{% include panel.html
		 parent="client"
		 id="c4"
		 scenario="I am getting errors connecting to relay.globusonline.org.  How do I fix this?"
		 content=c4
	%}

  {% capture c3 %}

<p>First, try transferring a file from the <a
href="https://www.globus.org/app/transfer?destination_id=db57ddde-6d04-11e5-ba46-22000b92c6ec&destination_path=%2Fdata1%2F"
title="Globus Transfer from ESNet Sunnyvale">ESNet Sunnyvale test endpoint</a>
to your system.  If the transfer is successful, then your system is probably
OK.</p>

<p>If ESnet transfers are also reporting 'connection failed', then the most
likely problem is a network-level block.  Globus Connect Personal needs to be
able to make outbound connections to TCP ports 50000 through 51000.  If that is
blocked, then you will be able to start transfers, but they will not run.  To fix this, you will need to reach out to your IT person. For students (undergrads and grads), reach out to <a href="https://thehub.stanford.edu/services/student-technical-support">Student Technical Support</a> at the <a href="https://thehub.stanford.edu/">Lathrop Learning Hub</a>.  For everyone else, go to your <a
href="https://web.stanford.edu/group/networking/dist/sunet.reports/LNA.html"
title="Local Network Administrators by Department">LNA</a>.</p>

<p>If you are unable to get your firewall changed, then your last-resort
option is to use the <a href="https://uit.stanford.edu/service/vpn"
title="Stanford University IT VPN Service">Stanford VPN</a>, but
you must use <em>Full Traffic (non-split-tunnel)</em> mode, which sends all
traffic (even non-Stanford traffic) through the VPN.</p>

<p>Your transfer will continue to attempt to run for up to a day before being
terminated.</p>

{% endcapture %}
  {% include panel.html
		 parent="client"
		 id="c3"
		 scenario="All of my transfers are saying 'connection failed'.  How do I fix this?"
		 content=c3
	%}

    {% capture c6 %}

<p>When you transfer files between a Globus Connect Personal endpoint and a
Globus Connect Server endpoint, regardless of the direction of the transfer,
the Globus Connect Personal endpoint is always the one that opens the
connection (so that all connections are outbound from your endpoint).  This is
done because Globus Connect Server administrators make sure that inbound
connections are allowed.</p>

<p>When both ends of a transfer are running Globus Connect Personal, one end
has to allow an incoming connection, and that is not always possible.  For
example, if one laptop is on a home network (behind a router), and another
laptop is on a different home network (behind a different router), the two
routers will block inbound connections.</p>

<p>In a case like this, both ends of the connection should be brought onto a
common network, in order for the data transfer to succeed.  One way of doing
this is by putting both endpoints onto the
<a href="https://uit.stanford.edu/service/vpn"
title="Stanford University IT VPN Service">Stanford VPN</a>.  If that still
does not work, try using the <em>Full Traffic (non-split-tunnel) mode</em>,
which routes all network traffic through the VPN.</p>

    {% endcapture %}
    {% include panel.html
       parent="client"
       id="c6"
       scenario="I am having problems transferring files between two Globus Connect Personal endpoints.  How do I fix this?"
       content=c6
    %}

    {% capture c7 %}

<p>If you have a full-service (or full-sponsored) SUNetID (in other words, if
you have Stanford email service), you can have the <em>Globus Plus</em> feature
enabled on your account.  If you already have a Globus Connect Personal
endpoint, Globus Plus allows you to share part of it with others.</p>

<p><a href="{{ "client/plus.html" | relative_url }}"
title="Globus Plus">Read about Globus Plus</a>.</p>

    {% endcapture %}
    {% include panel.html
       parent="client"
       id="c7"
       scenario="How do I allow sharing?"
       content=c7
    %}
</div>
<!-- Next item is Globus Server -->

<div class="section-head d-flex">
  <h2 class="p-2 flex-grow-1" id="serverhead">The Globus Server (aka Globus Connect Server)</h2>
  <button class="btn btn-default align-self-end toggle-all p-2" data-segment="server"><i class="fa-solid fa-plus"></i> Open All</button>
</div>

<div class="accordion" id="server">

{% capture s1 %}

<p>You will need to <a href="{{ "server.html" | relative_url }}" title="Globus Connect
Server">install Globus Connect Server</a> onto a system that has access to the
data your users wish to share.  As you follow the process, make sure to watch
out for sections that talk about enabling sharing.  In the end, you will have
an endpoint name, or a UUID.</p>

<p>Once your users have the endpoint information, they should go to the <a
href="https://www.globus.org/app/transfer" title="Globus Transfer Files">Globus
Transfer Files</a> page, where they can search for your endpoint, activate it
(by authenticating), and transfer files.</p>

<p>See also the question <em>Someone gave me access to a Globus endpoint.
How do I access it?</em>.</p>

<p>If your users want to transfer files to/from another environment (like, for
example, another lab's storage), then that other environment will also need
Globus Connect Server; you should direct the lab's IT person to this question.
Once a Globus Connect Server is up and running there, your users will need that
server's information (a name, a UUID, etc., just like with your endpoint).</p>

<p>If your users want to transfer files to/from their own systems (a laptop or a
desktop), they will need Globus Connect Personal.  You should point your users
to this page, and the question <em>Someone told me that I need the Globus
client.  What even is it? How do I get it?</em>.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s1"
     scenario="I want my users to be able to transfer files using Globus.  How do I do this?"
     content=s1
  %}

{% capture s21 %}

<p>This can be done, but it has to be done in two steps:</p>

<ol>

<li>First, <a href="{{ "server.html" | relative_url }}" title="Globus Connect
Server">install Globus Connect Server</a> onto a system that has access to the
data your users wish to share.  As you follow the process, make sure to watch
out for sections that talk about enabling sharing.  In the end, you will have
an endpoint URL.  It will look something like this:

<pre>https://www.globus.org/app/endpoints/96a13ae8-1fb5-11e7-bc36-22000b9a448b/overview</pre>

Give that URL to your users.</li>

<li>Next, each user who wishes to share must access the endpoint using the URL
provided (or, see the question <em>Someone gave me access to a Globus endpoint.
How do I access it?</em> for alternative ways of discovering your endpoint).
The endpoint's web page will have a <em>My Shares</em> tab; where users can
authenticate, create a share, and give others access (read-only or read-write)
to the share.</li>
</ol>
{% endcapture %}

  {% include panel.html
     parent="server"
     id="s21"
     scenario="I want my users to be able to share files with others (who do not have local accounts).  How do I do this?"
     content=s21
  %}

{% capture s8 %}

<p>Globus Connect Server works fine with storage that is accessed via NFS.
With NFSv3, no changes are needed.  With NFSv4, you will need to use
<code>sec=sys</code>.  The Kerberos security model does not work
with Globus, because Globus has no way of getting Kerberos credentials for
users.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s8"
     scenario="How can I use Globus Connect Server with NFS?"
     content=s8
  %}

{% capture s11 %}

<p>To meet the requirements for Moderate Risk data, simply follow the normal
installation instructions on the <a href="{{ "server.html" | relative_url }}">
Globus Connect Server</a> pages, but <em>be sure to use SUNetID Auth with
CILogon</em>.  Other than that, the installation instructions will mention the
settings which need to be in place for Moderate Risk environments.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s11"
     scenario="How do I use Globus for Moderate Risk data?"
     content=s11
  %}

{% capture s12 %}

<p>There is no ready-made, pre-approved solution for using Globus with High
Risk data.  Stanford does not have a BAA with Globus or the University of
Chicago, and
Stanford's use of Globus has not undergone a 
<a href="https://uit.stanford.edu/security/dra"
title="How to Request and Complete a Data Risk Assessment, Information Security,
Stanford University IT">Data Risk Assessment</a>.</p>

<p>Your best route forward may be to get your data into a form that is Low or
Moderate Risk, and onto systems that are also Low or Moderate Risk, and
do your transfers from there.  You should reach out to your IT people to
assist, or <a href="mailto:srcc-support@stanford.edu" title="Contact SRCC">
engage with us</a>.</p>

<p>If you are set on using Globus with High Risk data, you should expect to
bear substantial costs in both money and time.  <a
href="mailto:srcc-support@stanford.edu" title="Contact SRCC">Reach out</a> if
you are still interested!</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s12"
     scenario="How do I use Globus for High Risk (including PCI / PHI) data?"
     content=s12
  %}

{% capture s2 %}

<p>Beyond the documentation on the <a href="{{ "server/pre-install.html" | relative_url }}" title="Globus Connect Server Pre-Installation Planning">Pre-Installation Planning</a> page, there is a simple checklist for determining which authentication method to use:</p>

<ol>

<li>In your environment, are your users using SUNetIDs as usernames?  Then use
CILogon.</li>

<li>If your data are Moderate Risk, and your users are <em>not</em> using
SUNetIDs as usernames, then you will need to set up some form of username
mapping—or change everyone's usernames—and then use CILogon.</li>

<li>If your data are Low Risk, and your users are not using SUNetIDs as
usernames, then you can set up MyProxy OAuth authentication.</li>

<li>If you get pushback about opening a web server to the world (which is
required for MyProxy OAuth authentication), and you trust Globus enough to
handle your user's credentials, then use legacy MyProxy.</li>

</ol>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s2"
     scenario="How do I know which authentication method to use?"
     content=s2
  %}

{% capture s3 %}

<p>In general, if you follow <a
href="https://uit.stanford.edu/guide/securitystandards" title="Stanford Minimum
Security Standards">MinSec</a>, using MyProxy OAuth is more secure than using
legacy MyProxy.  It all has to do with where your password goes.</p>

<p>With legacy MyProxy, your username and password are sent to Globus, which
passes it on to the MyProxy service running on your endpoint.  Although each
connection (from you to Globus, and from Globus to MyProxy) uses TLS, it still
means that your username and password are being held (albeit temporarily) by a
third-party (Globus).</p>

<p>With MyProxy OAuth, your username and password are sent directly to the
OAuth server running on your endpoint.  Globus then receives a client cert, the
same as if you were authenticating using CILogon.</p>

<p>Although MyProxy OAuth does require that you have a web server (HTTPS only)
open to the world, as long as you follow proper installation and patching
procedures, you should remain reasonably secure.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s3"
     scenario="How is MyProxy OAuth better than legacy MyProxy if they both use MyProxy?"
     content=s3
  %}

{% capture s4 %}

<p>Right now, it is not possible to handle Moderate Risk data in Globus without
using CILogon.  The reason is, <a
href="https://uit.stanford.edu/guide/securitystandards#security-standards-applications"
title="Stanford Minimum Security Standards for Applications">MinSec for
Applications</a> for Moderate Risk applications requires that Duo two-step
authentication be used for all interactive user logins, and many end-user
Globus activities are interactive.</p>

<p>Unfortunately, none of the MyProxy-based authentication methods (legacy
MyProxy or MyProxy OAuth) support any form of multi-factor authentication, due
to the limitations of the MyProxy protocol.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s4"
     scenario="How can I handle Moderate Risk data without using CILogon?"
     content=s4
  %}

{% capture s5 %}

<p>Not easily, no.  At least, not without a sizeable amount of effort.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s5"
     scenario="Can I use CILogon without using SUNetIDs?"
     content=s5
  %}

{% capture s6 %}

<p>OK, yes, it <em>is</em> possible, but it will either require constant
maintenance and setup work, or will require software development.</p>

<p>When using CILogon, Globus uses client certs to authenticate to GridFTP as a
person.  That client cert includes a <em>Distinguished Name</em> (or
<em>DN</em>) to identify the user, as well as an
<em>eduPersonPrincipalName</em> (or <em>EPPN</em>) attribute that contains the
user's "scoped username" (that is, their username in the context of the
institution), which for Stanford is always <code>sunetid@stanford.edu</code>.</p>

<p>For example, to see your CILogon distinguished name, go to <a
href="https://cilogon.org" title="CILogon">CILogon</a> and log in with your
Stanford University credentials.  The "Certificate Subject" is your DN.</p>

<p>The first way to convert a client cert into a username is to use a
<em>gridmap file</em>.  This is a mapping from DN to local username, and is
described in <a
href="http://toolkit.globus.org/toolkit/docs/latest-stable/gsic/admin/index.html#_configuring_identity_mappings_using_literal_gridmap_literal_files_files"
title="Grid Security documentation, Section 5.1, Configuring Identity using
Gridmap files">Grid Security documentation Section 5.1</a>.  You will need to
have each user go to CILogon, get their DN, and send it to you for inclusion in
the gridmap file.</p>

<p>The second way is to write a <em>callout</em>.  This is a shared library
containing code that takes in various parameters (like a client cert) and
returns a local username.  The file format and calling convention is documented
in <a
href="http://toolkit.globus.org/toolkit/docs/latest-stable/gsic/admin/index.html#_configuring_alternate_credential_mappings"
title="Grid Security documentation, Section 5.2, Configuring Alternative
Credential Mappings">Grid Security documentation Section 5.2</a> and is also
explained on <a href="http://www.cilogon.org/gsi-c-authz#TOC-Gridmap-Callouts"
title="GSI Gridmap Callouts">CILogon's site</a>.  You can see the code for
Globus' EPPN callout <a
href="https://github.com/globus/globus-toolkit/tree/globus_6_branch/gsi/gridmap_eppn_callout">on
GitHub</a>.</p>

<p>Unfortunately, due to the complexity involved in this process, must Stanford-based support groups are unable to provide free support for custom gridmaps.  Your first call for support should be the <a href="https://groups.google.com/a/globus.org/forum/#!forum/developer-discuss" title="Globus Developer Discuss forum">Globus "Developer Discuss" forum</a> on Google Groups, which you can join using your Stanford Google account.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s6"
     scenario="Can I <em>really</em> not use CILogon without SUNetIDs?"
     content=s6
  %}

{% capture s7 %}

<p>Happily, in this scenario, nothing else needs to be done!  That is because,
with CILogon, the authentication and authorization functions are separate.</p>

<p>With CILogon, authentication is handled by <a
href="https://uit.stanford.edu/service/saml" title="Stanford UIT SAML
(Authentication)">Stanford SAML</a>.  Globus passes the results of this
successful authentication on to your endpoint, which extracts the SUNetID and
looks for a matching user.  So, no local authentication (password or otherwise)
is needed.</p>

<p>It is important to note, CILogon only handles authentication.  The
authorization function (which determines what the user can access) is still
handled by the operating system.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s7"
     scenario="My users coincidentally use SUNetIDs already, but not for passwords.  How can I use CILogon?"
     content=s7
  %}

{% capture s9 %}

<p>Globus Connect Server works even when users are not able to log in directly.
The server just needs to be able to identify users, and rely on the OS'
authorization mechanisms to verify permissions.</p>

<p>See also the question <em>How do I allow sharing when my users don't have
home directories?</em></p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s9"
     scenario="How can I run Globus Connect Server on a server where users cannot log in?"
     content=s9
  %}

{% capture s10 %}

<p>Files uploaded to a Globus Connect Server endpoint are owned by the user
who activated the endpoint.  Files uploaded to a shared endpoint are owned by
the user who created the shared endpoint.  The file's group will be set to the
owning user's primary group.</p>

<p>File permissions are set based on the GridFTP server's umask, and its
default permissions.  GridFTP's default permissions are <code>644</code>
(read/write for owner; read-only for everyone else).  To change GridFTP's
default permissions, edit <code>/etc/gridftp.conf</code>, adding the following
line:</p>

<pre>
perms 664
</pre>

<p>(Change <code>664</code> to whatever value is appropriate for your
situation.)</p>

<p>GridFTP's umask is set by your system's service-management software
(normally either SysV init, or systemd).  It is normally set to
<code>022</code>.  This umask means group and world write access will always
be disabled, regardless of the permissions you set.</p>

<p>If you want to change the umask, you will have to modify the
<code>/etc/init.d/globus-gridftp-server</code> script in two ways:</p>

<ol>

<li>First, look for this block of code in the script…<br />

<pre>
lsb=""
if [ -f /lib/lsb/init-functions ]; then
    lsb=_lsb
    lsb_ok=1
    . /lib/lsb/init-functions
    if [ -f /etc/redhat-release ] && lsb_release -v | grep -q 'core-[123]'; then
        unset lsb_ok
    fi

fi
</pre>

In that block, change the string <code>lsb=_lsb</code> to <code>lsb=""</code>.
This is needed to stop LSB-specific startup scripts from running, as they will
override the umask in all cases.</li>

<li>Next, in the <code>start()</code> block, locate this line:<br />

<pre>
        $gridftpd -S -c $conf -C $confdir -pidfile "${pidfile}"
</pre>

Immediately before that line, add a new line, where you set the umask to be
what you want.</li>

</ol>

<p>This work is required because GridFTP does not have a built-in way to change
its umask.  Once the changes are made, restart GridFTP, and test.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s10"
     scenario="How do I control permissions for uploaded files?"
     content=s10
  %}

{% capture s13 %}

<p>When the 'encrypt transfer' box is checked, at the start of a transfer,
Globus generates a 2048-bit RSA key, and a temporary SSL certificate valid for
two days.  The key and cert are given to both endpoints involved in the
transfer.</p>

<p>When one endpoint connects to the other, it immediately opens a TLS
connection, using the key and certificate provided.  The default cipher list is
the OpenSSL <code>HIGH</code> cipher list, which means the endpoints will
generatlly use Elliptic-Curve Diffie-Hellman Ephemeral (ECDHE) symmetric-key
negotiation (falling back to RSA key negotiation if needed), and some form of
AES symmetric encryption.</p>

<p>If necessary (for example, for transfers which take more than two days to
complete), Globus will automatically generate a new key and cert.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s13"
     scenario="How does Globus encrypt data traffic when encryption is requested?"
     content=s13
  %}

{% capture s14 %}

<p>The control traffic between Globus and you (used for directory listings and
to control data transfer) also uses TLS.  When an endpoint is created, Globus
generates a very-long-lived 2048-bit RSA key and certificate.  This is used as
a server cert, only for connections coming from Globus.  The default cipher
list is the OpenSSL <code>HIGH</code> cipher list, but containing only the RSA
key-exchange ciphers.</p>

<p>The only other traffic is API traffic during endpoint setup, and when
checking for a new software version.  Both connections are out to services on
AWS, which use TLS with normal server certs.  This API traffic comes from code
written in Python, which uses whatever TLS client configuration is the default
for the OS-provided Python 2 <a
href="https://docs.python.org/2/library/ssl.html" title="ssl - TLS/SSL wrapper
for socket objects">ssl module</a>.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s14"
     scenario="How does Globus encrypt other traffic?"
     content=s14
  %}

{% capture s15 %}

<p>First, you need to set up a managed Globus Connect Server endpoint.  Start
at the <a href="{{ "server/pre-install.html" | relative_url }}" title="Globus
Connect Server Pre-Installation Planning">Pre-Installation Planning</a> page
and go from there.</p>

<p>In that section, you will learn about the different sharing capabilities, how to enable them, and how to limit them.  That will have the information you need!</p> 

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s15"
     scenario="How do I allow sharing?"
     content=s15
  %}

{% capture s16 %}

<p>When a user creates a shared endpoint, Globus Connect Server must write some
sensitive data related to the share; this data must only be accessible by the
user who creates the shared endpoint.  Normally, this information is stored in
the user's home directory, but if users do not have home directories, an
alternative storage location must be used.</p>

<p>This is a delicate procedure—the layers of permissions are fairly
complex—but it is doable!  Read more in the <em>GridFTP: Sharing State</em>
section of the Globus Connect Server
<a href="{{ "server/configure.html" | relative_url }}"
title="Globus Connect Server Initial Configuation">Initial Configuration</a>
page.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s16"
     scenario="How do I allow sharing when my users don't have home directories?"
     content=s16
  %}

{% capture s17 %}

<p>This is the unique ID of the Stanford Globus Statistics Gateway.  See the
next question for more information.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s17"
     scenario="What is 503fc893-67ba-44d2-94f4-3c6365c5a9c7@clients.auth.globus.org ?"
     content=s17
  %}

{% capture s18 %}

<p>The Stanford Globus Statistics Gateway is a program that is operated by
<a href="https://srcc.stanford.edu/" title="Stanford Research Computing
Center">SRCC</a>, which collects information on transfers made using Globus.
It is primarily meant for gathering usage statistics, but the information can
also be used to get a picture of who is transferring data (alhtough,
information on <em>what</em> is transferred is not collected).  Granting
access to this program is a condition for accessing Stanford's Globus
subscription.</p>

<p>You need to give the Stanford Globus Statistics Gateway "Activity Monitor"
access to your Globus Connect Server endpoints.  This gives read-only access,
both to your endpoint and to shared endpoints hosted by your endpoint.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s18"
     scenario="What is the Stanford Globus Statistics Gateway?  Why do I need to give it access to my stuff?"
     content=s18
  %}

{% capture s19 %}

<p>This is the unique ID of the old Stanford Globus Statistics Gateway, which
was active during the time this site was initially being developed.  It has
been retired, and you can remove its access from your endpoints.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s19"
     scenario="What is aa57f001-4ec4-424b-93f0-9b0c73b0d0b0@clients.auth.globus.org?"
     content=s19
  %}

{% capture s20 %}

<p>This is a complex question, because there are lots of factors that influence
transfer speed, and only some of those factors can be adjusted on your end;
performance depends as much on the other end as it does on you.  That being
said, here are some things you should consider:</p>

<ul>

<li><b>Dedicate a modern machine.</b>  This is especially impotant when
encryption is used, because it will give you access to CPUs that are able to do
AES encryption operations natively.  Dedicating an entire machine also ensures
that the system is not being distracted with other work.</li>

<li><b>Have a 10 GBps or better link.</b>  A single Globus Connect Server
installation, set to aggressive network use, will happily saturate a 10 Gbps
link.</li>

<li><b>Use a modern OS.</b>  You should use the latest-available version of your
chosen distribution, whichever one includes long-term support.  That includes
the latest RHEL or CentOS, the latest Debian, and the latest LTS Ubuntu.  Using
the latest-available OS ensures that you have the best-available TCP
congestion-control algorithms.</li>

<li><b>Place your endpoint outside the firewall.</b>  Even if the rest of your
environment is firewalled, your endpoint's data-transfer links should be on a
non-firewalled VLAN.  Bypassing the network firewall improves performance,
because the network firewall increases latency, as it has to screen each
connection.  Also, network firewalls may be limited to 10 or 20 Gbps
connections—depending on firewall model—which has to be shared with all other
network firewall users.<br />

Note that this does require careful work to maintain
security: The links outside of the network firewalls must only be used for
data-transfer traffic, not regular user logins.  You must also containue to run
a host-based firewall, to meet <a
href="https://uit.stanford.edu/guide/securitystandards#security-standards-servers"
title="Minimum Security Standards for Servers">MinSec requirements</a>.</li>

<li><b>Tune your host.</b>  Even with the latest OS, there is additional OS and
hardware tuning that can be done to extract more performance.  Note, however,
that some performance adjustments will actually slow down lower-bandwidth
connections (like home Internet connections).<br />

Read more on the <a href="https://es.net/host-tuning/" title="Energy Sciences
Network, Host Tuning">ESnet Host Tuning</a> page.</li>

<li><b>Connect as close to the core as possible.</b>  Ideally, your data
transfer node should be in a Stanford data center, where it will be able to
connect as close as possible to the network core.  The next-best option would
be to have it in a building room with switches that connect directly back to an
ECH.  Either way, it is best if your endpoint bypasses normal rack switches, as
most rack switches only have a 10 or 20 Gbps link back to the core.  One way
of doing this is connecting your host to the <a
    href="https://srcc.stanford.edu/stanford-research-network-srn">Stanford
    Research Network</a>.</li>

<li><b>Consider multiple servers.</b>  If all of the above options have been
exhausted, and your back-end storage still has available throughput capacity,
you can add another server to your existing Globus Connect Server endpoint.
When Globus sees multiple servers for a single endpoint, it will spread
transfer work across the multiple servers.  Besides the performance increase,
this gives you some redundancy, as you can take one server down for maintenance
without taking the entire endpoint offline.</li>

</ul>

<p>You should also be <b>monitoring your endpoint</b>.  Beyond monitoring CPU,
memory, and utilization of the data-transfer interface, you should also monitor
the performance of the link to your storage.  You can use the <a
href="https://www.globus.org/app/transfer?destination_id=db57ddde-6d04-11e5-ba46-22000b92c6ec"
title="Globus web site, ready to transfer from ESnet Sunnyvale">ESnet Sunnyvale
endpoint</a> to test transfer performance to your storage.</p>

{% endcapture %}
  {% include panel.html
     parent="server"
     id="s20"
     scenario="How do I make transfers to/from my endpoints go faster?"
     content=s20
  %}
</div>
<!-- Next item is Policies &amp; Support -->

<div class="section-head d-flex">
  <h2 class="p-2 flex-grow-1" id="policieshead">Policies &amp; Support</h2>
  <button class="btn btn-default align-self-end toggle-all p-2" data-segment="support"><i class="fa-solid fa-plus"></i> Open All</button>
</div>

<div class="accordion" id="support">

    {% capture p2 %}

<p>At this time, Stanford pays for a <a href="https://www.globus.org/subscriptions"
title="Globus Subscriptions">Globus Standard subscription</a>, and the
following <a href="https://www.globus.org/connectors" title="Premium Storage
Connectors">Premium Storage Connectors</a>: Box, Google Cloud Storage, Google
Drive, and S3.</p>

<p>We have not paid for the High Assurance—which would likely be required for
transferring with High Risk data—or HIPAA BAA—which would be required for
transferring PHI—levels.</p>

    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p2"
     scenario="What does Stanford pay for?"
     content=p2
  %}

    {% capture p1 %}

<p>Anyone can use the free portions of Globus (such as Globus Connect
Personal), regardless of Stanford affiliation.</p>

<p>For the parts of Globus that Stanford pays for, the license is
"campus-wide".  Some notable exclusions from "campus-wide" are the Carnegie
Institution, SLAC, Stanford Children's Health, and Stanford Health Care (the
adult hospital).  For people affiliated with those entities.</p>

<p>It does not matter if you are a student, staff, postdoc, or whatever: If
your group is not part of one of the excluded entities, you can take advantage
of our campus subscription!</p>

<p>For full details, see the <a href="{{ "policies.html" | relative_url }}"
title="Globus @ Stanford Policies & Agreements">policies page</a>.</p>


    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p1"
     scenario="Who can use this?"
     content=p1
  %}

    {% capture p3 %}

<p>There is only one limit on the type of data: <b>No High Risk data may be
transferred using Globus.</b>  Other than that limit, there is no limit on
the types of data you can transfer.  (For example, some services—not
Globus—have exclusions on administrative data.  That is <em>not</em> the case
here.)</p>

<p>There is one caveat: If you are working with Moderate Risk data, there are
certain things you have to do as part of setting up Globus.  For example, you
have to make sure that encryption is required for all transfers, and that TLS
1.0 is disabled.  The instructions on this site take all of this into
account.</p>

<p>Also, <a href="https://docs.globus.org/api/search/">Globus Search</a> only
supports Low Risk data.  This is OK, because it is meant for searching public
data sets.</p>

<p>There are <b>absolutely no limits</b> on the quantity of data that you may
transfer under our subscription.  The only limits are those that are naturally
imposed by your storage space, and your network connection.</p>

    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p3"
     scenario="Are there any limits on the type or quantity of data that I can transfer?"
     content=p3
  %}

    {% capture p4 %}

<p>Yes, you can!  Check out our <a href="{{ "cloud.html" | relative_url  }}"
title="Globus and the Cloud">Cloud page</a> to see what we have licensed.</p>

    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p4"
     scenario="Can I use this with Amazon S3, GCP, or other cloud services?"
     content=p4
  %}

    {% capture p5 %}

<p>Your best starting point is <a href="{{ "support.html" | relative_url  }}"
title="Globus @ Stanford Support">the support page</a>.  This page has
pointers to various common problems, places where you can get in-person help,
and pointers to local support contacts.  There are also several mailing lists
that are run by Globus.  Finally, if your issue is particularly weird, there
are several people on-campus who have direct access to Globus support.</p>

    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p5"
     scenario="Where do I go for support?"
     content=p5
  %}

    {% capture p6 %}

<p>Funding for Globus at Stanford comes from several sources.</p>

<p>The Standard Subscription is currently paid for by the <a href="http://srcc.stanford.edu"
title="Stanford Research Computing Center">Stanford Research Computing
Center</a>, a joint effort of the <a href="https://doresearch.stanford.edu/office/office-vice-provost-and-dean-research"
title="Office of the Vice Provost and Dean of Research">Dean of Research</a>
and <a href="http://uit.stanford.edu" title="University IT">University IT</a>;
and <a href="http://library.stanford.edu" title="Stanford Libraries">Stanford
Libraries</a>.</p>

<p>The funding for the S3 connector—supporting Amazon S3, Wasabi, and other
S3-compatible platforms—comes from the <a href="http://gbsc.stanford.edu"
title="Genomics Bioinformatics Service Center">Genomics Bioinformatice Service
Center</a>.  The funding for the Box, Google Cloud, and Google Drive connectors
comes from the <a href="https://uit.stanford.edu/project/box-migration"
title="Stanford University Box Migration">Box Migration project</a>, run by the
<a href="https://uit.stanford.edu/organization/service-strategy"
title"Service Strategy">Service Strategy unit</a> within <a href="http://uit.stanford.edu"
title="University IT">University IT</a>.</p>

    {% endcapture %}

  {% include panel.html
     parent="support"
     id="p6"
     scenario="Who pays for this?"
     content=p6
  %}

<!-- Next item is p7 -->

</div>
