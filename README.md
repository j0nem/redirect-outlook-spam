# Redirect outlook.com "junk" emails
PHP CLI tool to redirect spam from the outlook `Junk`-folder to another mailbox

If you use an outlook.com mailbox, you may found out that the spam filter of the platform does not really work. In my case, 70-80% of important emails are marked as junk.

Because the filter options on outlook.com are applied AFTER the junk filtering, there is no native option to handle new incoming "spam" mails. This tool connects via IMAP to your outlook.com mailbox and redirects all emails in the folder to the given mail address via the outlook.com SMTP server. After that, it moves the emails to the Inbox.

# Installation:
Via composer in an existing project:

```bash
php composer.phar require j0nem/redirect-outlook-spam
```

Or clone the repository and install the dependencies:

```bash
php composer.phar install
```

# Usage:
Call the script with your outlook.com email & password and the email address you want to send the emails to.

```bash
php bin/redirect-spam <authEmail> <authPassword> <sendToEmail>
```

Maybe you want to install a cronjob (e.g. every 5 minutes) to run the task regularly.
