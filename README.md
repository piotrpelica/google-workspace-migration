# Google Workspace Migration
Legacy GSuite to Personal Account

## TOC

- Takeout
- Gmail

## What's going on?

Hi! Google has announced that the users of the free GSuite will soon have to pay to keep the accounts active (if that's not true, then please correct me - however this is what I understood). I've partially started moving to my private Gmail account some time ago, as I was missing a lot of features that were simply not available to the GSuite (now Google Workspace) users, but it seems that now is as good time as any to finally finish this.

Also, if your anything like me, you had your family or friends or whoever else there, so you're not looking at paying just for yourself (in this case I might have just given up and do that), you're looking at a bill that gives you nightmares. The instructions below will require doing them for each account individually. Yeah, I know.

As there is no official "click here to migrate to personal account" tool yet (and I guess it's unlikely to appear, as Google's product teams don't seem to talk to each other), I'm gonna publish my journey here, for others to find it easier to migrate the accounts - hopefully before the deadline.

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
