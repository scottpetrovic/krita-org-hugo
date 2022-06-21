---
title: "Ways to Help Krita: Bug Triaging"
date: "2016-03-14"
---

This is the first article of short series on ways everyone who wants to put some time into helping Krita can make a real difference. There are many ways of helping Krita, ranging from coding to writing tutorials, helping users on forums to helping with fund raisers. But let's take a look at one task that is really important: bug triaging.

Now that there are hundreds of thousands of Krita users, we're getting lots of bug reports. And a lot of those bugs are specific to the reporter's system. Or so it seems. Some bugs only happen with certain combinations of hardware, operating system, other installed software. Some bugs happen for everyone but are rare because not that many use a feature, and some bugs suddenly turn up because we're human and making mistakes.

And every report needs to be read, preferably by several people, who can try to determine whether:

- they can trigger the bug -- and in that case, confirm it
- cannot understand the report, or determine that the report is incomplete -- and in that case ask for more information
- know that the bug has been reported before, and then close the bug as a duplicate of the earlier report.

We're using KDE's bugzilla to track bugs for Krita. Now we admit up-front that bugzilla is an old-fashioned monster of a web application, but it's what we have, and for now we'll have to make it work for us! Here's what you see when you search for open Krita bugs:

[![Spectacle.Lh7342](../images/Spectacle.Lh7342.png)](https://krita.org/wp-content/uploads/2016/03/Spectacle.Lh7342.png)

Whoops, 320 open bugs... Important bits of information are:

- Version: the version of Krita the user was using.
- Severity: is it a crash, or a minor issue or a wish.
- Status: UNCO means Unconfirmed. That means that we either haven't tried to reproduce the bug or couldn't reproduce it.
- Summary: a short description of the issue
- Reporter: who reported it
- OS: which operating system the user used. Windows (often reported as Windows CE), Linux or OSX

As you can see, we really need help! Your friendly author, Boudewijn, is also the maintainer of the project, developer and manager. Together with Wolthera, we're trying to triage all reported bugs, and we're not managing to reply on time. That's where you come in! If you're a reasonably experienced Krita user and want to help out, here's how to get ready and set up!

### Get a Bugzilla Account

Go to https://bugs.kde.org and select "Create new Account"

### [![Spectacle.nS7342](../images/Spectacle.nS7342-1024x492.png)](https://krita.org/wp-content/uploads/2016/03/Spectacle.nS7342.png)

Complete the registration forms, and click on the confirmation link in the email you get sent (I'm using Alpine for reading email, which is a text-mode client... That's optional!).

[![Spectacle.kn7342](../images/Spectacle.kn7342.png)](https://krita.org/wp-content/uploads/2016/03/Spectacle.kn7342.png)

### Setup Email Notifications

Log in into bugzilla and click on the Preferences link at the top, then "Email Preferences". Bugzilla can send a lot of email, but fortunately it includes a number of special headers that make it easy to filter bug mail into special mailboxes. There are two steps: first are the general email preferences:

[![Spectacle.Ti7342](../images/Spectacle.Ti7342.png)](https://krita.org/wp-content/uploads/2016/03/Spectacle.Ti7342.png)

And then there's the important bit, that makes sure you get email for all bugs that are about Krita. Add the user "krita-bugs-null@kde.org" to the list of User Watches:

[![Spectacle.wZ7342](../images/Spectacle.wZ7342-1024x452.png)](https://krita.org/wp-content/uploads/2016/03/Spectacle.wZ7342.png)

Now you will get mail whenever anything happens to a Krita bug. Using the special bugzilla headers, you can sort all the mail ready for handling:

- X-Bugzilla-Reason: None
- X-Bugzilla-Type: new
- X-Bugzilla-Watch-Reason: AssignedTo krita-bugs-null@kde.org
- X-Bugzilla-Product: krita
- X-Bugzilla-Component: tablet support
- X-Bugzilla-Version: 2.9.11
- X-Bugzilla-Keywords:
- X-Bugzilla-Severity: normal
- X-Bugzilla-Who: boudewijnrempt@gmail.com
- X-Bugzilla-Status: UNCONFIRMED
- X-Bugzilla-Priority: NOR
- X-Bugzilla-Assigned-To: krita-bugs-null@kde.org
- X-Bugzilla-Target-Milestone: ---
- X-Bugzilla-Flags:
- X-Bugzilla-Changed-Fields: bug\_id short\_desc product version rep\_platform op\_sys bug\_status bug\_severity priority component assigned\_to reporter

For instance, I have split my bug mail according to whether it's a new bug, a changed bug, a new wish, a changed wish, or a reply to a needs-info query.

### Triage a Bug

And then when a bug lands in your inbox, you can open it in bugzilla and triage it. There are a couple of steps here:

1. Check if the severity is "wish", if so, leave alone. Wish bugs are special.
2. Check whether it's a duplicate, if so, close it.
3. Check whether the subject makes sense and mentions the most pertinent information, if not, update it
4. Check whether the OS is correct. For instance, Windows bugs are often reported for Windows CE, and that needs to be changed to MS Windows.
5. Check whether the version isn't too old. At this moment, we don't try to fix bugs for 2.8 anymore, and after 3.0 is released, if a bug is reported for 2.9 the bug should be marked as NEEDSINFO and the user asked to try to reproduce the issue with 3.0
6. Thank the reporter for his bug report. Keep in mind that reporting a bug can be scary enough, especially for new users, and that it is also a certain amount of effort. Bug reporters are awesome contributors, too!

These are the preliminaries: now then the real work starts. Trying to reproduce the bug. At first, you won't be able to close bugs; so at first all you can do is add comments to the bug report. If you've done that a couple of times, you'll have learned how the system works and gotten a feel for what should be done with new bugs. That's the moment to ask me, Boudewijn (boud@kde.org, boud on #krita on irc.freenode.org) for more powers!

- It's easy to reproduce: add any notes on how you reproduced the issue, on your OS, version of Krita, hardware and set the bug to CONFIRMED.
- There is not enough information to reproduce the bug: set the bug to NEEDSINFO and ask the reporter for more information
- You cannot reproduce the bug even though the report is complete and you can follow all the steps: Note that you cannot reproduce the bug and ask the reporter to reproduce. Set the bug to NEEDSINFO and wait. If the reporter answers that they cannot reproduce either, close the bug as WORKSFORME
- You cannot reproduce the bug but suspect that that's because it's already fixed: add a comment to the bug but don't change the status yet.
- You suspect that the reporter simply doesn't realize that they are using Krita in the wrong way, for instance by painting in 16 bits linear light RGB and saving to a PNG file without a profile. Point the reporter to the manual ([https://docs.krita.org](https://docs.krita.org)) and close with NEEDSINFO. If the reporter replies that that is the case, we can close the bug.
- The bug is about an issue with a drawing tablet. Please ask the user to upload a [tablet log](https://docs.krita.org/KritaFAQ#What_if_your_tablet_is_not_recognized_by_Krita.3F).

And that's it, really.  Now start triaging bugs and earn our undying gratitude! Help with bug triaging is a real and lasting contribution to Krita!
