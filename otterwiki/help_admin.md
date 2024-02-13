## Admin Guide

An Otter Wiki can be configured by Admin users who can find <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-cogs"></i></span> Application Preferences</span>, <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-users"></i></span> User management</span> etc. in the sidebar menu of
their <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-ellipsis-v"></i></span> <i class="fas fa-caret-right"></i> <span class="btn btn-square btn-sm"><i class="fas fa-cog"></i></span> Settings</span>.

### Branding

In the <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-cogs"></i></span> Application Preferences</span> the <span class="help-button">Site Name</span>, which is
displayed in the navigation bar on the top of the site and in emails, can be
configured.

The <span class="help-button">Site Logo</span> is displayed next to the site
name, while the <span class="help-button">Site Icon</span> (or favicon) is displayed in the
browser tab and in bookmarks. Both Site Logo and Site Icon can be attachments.
An Otter Wikis logo is the default for both.

The <span class="help-button">Site Description</span> is used in the
`<meta name="description">` tag.

### User management

All users are listed in a table under <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-users"></i></span> User management</span>. You can update the flags of the users by checking and unchecking the checkboxes, where <span class="help-button"><input type="checkbox" style="display:inline;" id="true" checked></span> means the flag is set and <span class="help-button"><input type="checkbox" style="display:inline;" id="false"></span> means the flag is not set. A set flag grants a privilege to a user.

Privileges granted per user add to the general permissions. For example, if in general only users with the **Admin** flag are allowed to upload attachments, the `user@example.org` can be allowed to Upload without being flagged as Admin.

A user with a <span class="help-button"><input type="checkbox" style="display:inline;" id="true-admin" checked></span> in the **Admin** column has Admin permissions. The changes are applied with <span class="btn btn-primary btn-sm btn-hlp">Update Privileges</span>.

#### Edit a user

With <span class="help-button"><a hre="#"><i class="fas fa-user-edit"></i></a></span>
you can open up a single user for editing. Here you can update
<span class="help-button">Name</span> and <span class="help-button">eMail</span>
of a user, and set flags and permissions. Changing a users name or email does not change
the commit history and only affects future commits.

Like in the User management table you can control the users flags using the
checkboxes.

The changes will be applied with <span class="btn btn-primary btn-sm btn-hlp">Update</span>.

#### Delete a user

On the Edit user page you can remove a user from the wiki's database. Check the
box and hit <span class="btn btn-danger btn-sm btn-hlp" style="border: None;" role="button">Delete</span>.
Please note that this neither changes any edit history nor 
prevents the user from signing up again.


### Access Permissions and Registration Preferences

What is necessary for a user to be able to Read/Write pages or upload and modify
attachments is controlled in the <span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-users-cog"></i></span> Permissions and Registration Preferences</span>.

- `Read Access` enables users to display pages and attachments. Including the
    history and every single commit.
- `Write Access` enables users to edit pages.
- `Attachments Access` enables users to upload and modify attachments.

Who can access what is defined via

- `Anonymous` - Everyone can access the wiki without being logged in.
- `Registered` - Users need an account and have to be logged in.
- `Approved` - Users have to be logged in and the <span class="help-button">Approved</span> flag has to be set.
- `Admin` - Users have to be logged in and the <span class="help-button">Admin</span> flag has to be set.

Additionally, you can configure privileges per user. The privileges granted per user add to the general permissions. See [User Management](#user-management) above.

<span class="help-button"><input type="checkbox" style="display:inline;" id="true-reg-req" checked> Registration requires email confirmation</span>, which is supposed to prevent users to register using fake mail addresses.

If a user needs to be approved, an admin user either needs to set the flag manually
or enable <span class="help-button"><input type="checkbox" style="display:inline;" id="true-auto-approve" checked> Auto approve of newly registered users</span>. When admins need
to approve users, <span class="help-button"><input type="checkbox" style="display:inline;" id="true-notify" checked> Notify admins on new user registration</span> helps with that.


### Mail Preferences

To enable An Otter Wiki to send mails to users registering, resetting their lost
password and notify admins about new users, configure the
<span class="help-button"><span class="btn btn-square btn-sm"><i class="fas fa-envelope"></i></span> Mail Preferences</span>. See the [flask-mail documentation](https://pythonhosted.org/Flask-Mail/) for configuration details.

You can test the configuration using <span class="help-button">Send Test Mail</span>. Per default the test mail is sent to yourself.


[modeline]: # ( vim: set fenc=utf-8 spell spl=en sts=4 et tw=80: )
