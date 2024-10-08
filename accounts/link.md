---
layout:      page
toc:  false
title:      Globus Account Creation
id: accounts
see-also: true
---

## Linking Additional Identities

As mentioned in the [introduction]({{ "accounts" | relative_url }}), Globus
supports having multiple _identites_ per person, with one identity acting as
the person's _primary identity_.

{% include info-box.html
   icon = "users"
   header="Google, ORCID, or ACCESS?  Now's the time!"
   content="If you have a Stanford Google account, an ORCID, or an NSF ACCESS account, now is a good time to link those identities!"
%}

{% include info-box.html
   icon="window-close"
   header="Do not link your entity's Globus ID"
   content="If your group owns, or has access to, a Globus ID for the group, you <b>must not</b> link it to your primary identity.  Those Globus IDs are for entities, and may not be linked to individual people."
%}

To link an identity, go to [app.globus.org](https://app.globus.org).  If you
are not already logged in, then you will be presented with the login page:

{% include hero-image.html
   src="/assets/accounts/LoginPage.png"
   alt="Globus login screen"
   caption-overlay=true
   caption-header="The Globus login screen"
   caption-text=""
%}

Log in as normal, and you will arrive at the File Manager:

{% include hero-image.html
   src="/assets/accounts/TransferPage.png"
   alt="Globus transfer screen"
   caption-overlay=true
   caption-header="The Globus File Manager"
   caption-text=""
%}

Click on the **<i class="fas fa-cog"></i> Settings** button (near the
bottom-left corner of the page).  This will take you to the Account tab on the
Settings page:

{% include hero-image.html
   src="/assets/accounts/AccountManagement.png"
   alt="Globus Account Management"
   caption-overlay=true
   caption-header="Account Management"
   caption-text="Your primary and all linked identites are displayed here."
%}

The Account tab displays your current primary identity (likely your
Stanford identity) and any linked identites.

To link a new identity, click on the **<i class="fas fa-id-card"></i><i
class="fas fa-plus-circle"></i> Link Another Identity** button (located near
the top-right of the page).

{% include hero-image.html
   src="/assets/accounts/AddLinkedIdentity.png"
   alt="Page asking you to select an institution to log in"
   caption-overlay=true
   caption-header="Selecting an Institution"
   caption-text="Just like when logging in for the first time, when linking an identity, you must choose an institution in which to log."
%}

You will now be sent through the normal login process for the linked identity.
Once that is complete, you will be taken back to the account management page,
with the newly-linked identity listed in the _linked identities_ section.

{% include info-box.html
   icon="exclamation-triangle"
   header="Identities cannot be double-linked"
   content="If you want to 'move' a linked identity, you will need to un-link the identity from the 'losing' primary, before you link it to the 'gaining' primary."
%}
