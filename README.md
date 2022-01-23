# Google Workspace Migration
Legacy GSuite to Personal Account

## TOC

- [Takeout](#takeout)
- [Gmail](#gmail)
- [Calendar](#calendar)
- [Photos](#photos)
- [Contacts](#contacts)
- [My Business](#my-business)
- [Password Manager](#password-manager)
- [Drive](#drive)

## What's going on?

Hi! Google has announced that the users of the free GSuite will soon have to pay to keep the accounts active (if that's not true, then please correct me - however this is what I understood). I've partially started moving to my private Gmail account some time ago, as I was missing a lot of features that were simply not available to the GSuite (now Google Workspace) users, but it seems that now is as good time as any to finally finish this.

Also, if your anything like me, you had your family or friends or whoever else there, so you're not looking at paying just for yourself (in this case I might have just given up and do that), you're looking at a bill that gives you nightmares. The instructions below will require doing them for each account individually. Yeah, I know.

As there is no official "click here to migrate to personal account" tool yet (and I guess it's unlikely to appear, as Google's product teams don't seem to talk to each other), I'm gonna publish my journey here, for others to find it easier to migrate the accounts - hopefully before the deadline. All of the methods below were tested by me and were working at the time of when they were added. I will do my best to keep this up to date. If something's not working or you know a better way, let me know.

This assumes you're what some call _a computer person_. This is because you have set up a GSuite, which itself does require some computer skills.

Also - this is not [degoogle](https://github.com/tycrek/degoogle). You might be able to use some of this stuff to move to another service provider, but it's mostly Workspace (GSuite) to Personal (Gmail).

## Contributing

If you have a way of migrating some service that's not here, or you have a better way - feel free to fork this and shoot me a PR.

---

## Takeout

Whatever you do, it's probably a good idea to do the [Takeout](https://takeout.google.com/). You'll at least will have a copy of your data in case you won't be able to import it - and who knows, there might be a way to do it later?

## Gmail

Gmail has an official tool for importing e-mails from other accounts. 

You'll have to have enabled [less-secure access](https://myaccount.google.com/lesssecureapps) or generate an [app password](https://myaccount.google.com/apppasswords). I went with the app password.

1. Make sure that you have [enabled POP](https://support.google.com/mail/answer/7104828) on the Workspace account.
2. Login to personal account, go to [Gmail's](https://mail.google.com/mail/) Settings -> See all settings -> Accounts and Import -> Import mail and contacts.
3. Enter the Workspace account's address. Let it do its thing, it may take a moment.
4. Enter the app password.
5. Enter full e-mail address as username, then `pop.gmail.com` as POP server, click on Edit next to the port. Select 995 and check `Use SSL`. Click Continue.
6. Select options however you like. Click Continue.

The process has started. It can take hours or even days, depending on how much mail you had.

## Calendar

1. Login to your Workspace account and go to [Google Calendar](https://calendar.google.com/calendar/).
2. Go to Settings and select Import & Export.
3. Click Export. Wait a bit, then download and unzip the file.
4. Login to your Personal account, go to the Import & Export.
5. Import all the files you just unzipped (unless you don't want to). This may take a second and there is no indication of progress on the UI. Just wait.
6. Once finished you'll get a message of how many events were imported.

## Photos

1. Go to Workspace's [Google Photos](https://photos.google.com/).
2. Set up Partner Sharing, share all photos.
3. Accept invitation on Private account.
4. On Private account, go to Settings -> Partner Sharing and make sure you enable saving to your photos.

From now on all the photos will be shared with private account and saved there, so once the account is removed, the photos will still be there (in the info you'll find a message saying `Shared by a Google user, Saved to your photos`.

[Based on this](https://support.google.com/photos/thread/80602212/i-want-to-transfer-all-google-photos-to-another-account)

## Contacts

1. Go to Workspace's [Google Contacts](https://contacts.google.com/). On the left select Export, Contacts (so it's all contacts), Google CSV and click Export.
2. Go to private Contacts. Select Import, upload the file and click Import. Let it do it's job.

IMHO it's now a good time to check the list - merge or delete duplicates, remove old contacts, etc.

## My Business

This one is easy. Log in to [My Business](https://business.google.com/dashboard/) on the Workspace's account, select the business you want to move, click Users, add your private account as new owner, then change that account to primary owner.

## Password Manager

If you're using [Google Password Manager](https://passwords.google.com/), it offers Export & Import options.

1. On Workspace account go to [Google Password Manager's settings](https://passwords.google.com/options).
2. Click Export, confirm that you understand that the file stores passwords in plain text and if anyone gets their hands on this file you're doomed.
3. Confirm that you are you, then wait for the file to be generated. This can take a moment.
4. On private account go to the settings again, select Import and upload the file.

You can also do it from Chrome, if you're using a Workspace account in your profile.

1. Go to [Passwords](chrome://settings/passwords) - click on your profile icon and then on a key.
2. Click three dots next to the Saved passwords and select Export.
3. Confirm you know what you're doing.
4. Import the file to [Google Password Manager](https://passwords.google.com/options).

That's it - when you log in to Chrome as your private account, it will get the passwords from the Password Manager

## Drive

Easiest and fastest option I've found was to do the following:

1. Create a transfer folder on Workspace's Drive.
2. Share that folder with your private account. Make sure you have given yourself Editor permissions.
3. Move all files to the transfer folder. When prompted for access, allow editing and accept.
4. For folders here's a trick - you can move the ones you own (if you select list view, you will see "me" in the Owner column). Select those and use Move to from the right-click menu to move them to the transfer folder. 
   For others:
   - publicly shared ones you can just copy link and add shortcut in personal drive;
   - privately shared ones - if you can share them, nice. If not, you'll have to talk to people. Sorry.
6. On private account's Drive go to the Sharing, open transfer folder, select everything, right click, select Move then left arrow in the top left corner. Select My Drive and click Move. Accept the message that in order for others to have access file will have to be shared again.

Ta dah - all files moved!

---

More to come
