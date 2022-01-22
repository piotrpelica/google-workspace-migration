# Google Workspace Migration
Legacy GSuite to Personal Account

## TOC

- [Takeout](#takeout)
- [Gmail](#gmail)
- [Calendar](#calendar)
- [Photos](#photos)

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
2. Login to personal account, go to Settings -> See all settings -> Accounts and Import -> Import mail and contacts.
3. Enter the Workspace account's address. Let it do its thing, it may take a moment.
4. Enter the app password.
5. Enter full e-mail address as username, then `pop.gmail.com` as POP server, click on Edit next to the port. Select 995 and check `Use SSL`. Click Continue.
6. Select options however you like. Click Continue.

The process has started. It can take hours or even days, depending on how much mail you had.

## Calendar

1. Login to your Workspace account and go to Google Calendar.
2. Go to Settings and select Import & Export.
3. Click Export. Wait a bit, then download and unzip the file.
4. Login to your Personal account, go to the Import & Export.
5. Import all the files you just unzipped (unless you don't want to). This may take a second and there is no indication of progress on the UI. Just wait.
6. Once finished you'll get a message of how many events were imported.

## Photos

1. Go to Workspace's Google Photos.
2. Set up Partner Sharing, share all photos.
3. Accept invitation on Private account.
4. On Private account, go to Settings -> Partner Sharing and make sure you enable saving to your photos.

From now on all the photos will be shared with private account and saved there, so once the account is removed, the photos will still be there (in the info you'll find a message saying `Shared by a Google user, Saved to your photos`.

[Based on this](https://support.google.com/photos/thread/80602212/i-want-to-transfer-all-google-photos-to-another-account)

---

More to come
