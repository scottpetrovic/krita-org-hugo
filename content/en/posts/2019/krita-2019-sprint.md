---
title: "Krita 2019 Sprint"
date: "2019-08-12"
categories: 
  - "news"
---

Officially, on Friday the 2019 Krita Sprint was over. However, most people stayed until Saturday... It's been a huge sprint! Almost a complete convention, a meeting of developers and artists.

[![](/images/posts/2019/IMG_20190806_204743139_HDR-1024x576.jpg)](https://krita.org/wp-content/uploads/2019/08/IMG_20190806_204743139_HDR.jpg) All the sprinters together

The sprinters, artists, contributors and artists/contributors, all together.

## Monday

On Monday, people started arriving. It was pretty great to meet again so many people who hadn't seen each other for a long time, and to see so many people who hadn't been to any Krita sprint before. We had rigged a HDR test system in the sprint area, which was, probably for the last time, since it's getting too small, the 12th-century cellar underneath the Krita maintainer's house, in the town centre of Deventer. Wolthera was kept busy all week giving an introduction to painting in HDR -- she is, after all, the first person in the world to have actually done creative painting in HDR.

There was other hardware to test as well, like the Android tablet with Sharaf Zaman's Android port of Krita. Sharaf couldn't come to the sprint; his visum was denied, probably because the Dutch authorities were informed beforehand of the intention of the Indian government to cancel Kashmir's special status. With a blanket closure of internet, mobile telephony and landline telephony, it was impossible to be in touch with Sharaf. We did some [thorough testing](https://phabricator.kde.org/T11355), and we hope contact with Sharaf will be restored soon.

## Tuesday

Since we still weren't complete, we postponed the meeting until Thursday, so this day was a day for hacking and discussions. We had many more artists joining us than previously, so the discussions were lively and the meetings were good -- but there were more bugs reported than bugs fixed.

## Wednesday

On Wednesday, we went on an expedition, to the [Openlucht Museum.](https://openluchtmuseum.nl/en) With twenty-three people attending, it was more efficient to actually rent a bus for the lot of us. The idea about the outing was to make sure people who had never been at a sprint and people who had been at sprints before would mingle and get to know each other. That worked fine!

[![](/images/posts/2019/DSC00283-1024x768.jpg)](https://krita.org/wp-content/uploads/2019/08/DSC00283.jpg)

We had a somewhat disappointing guided tour. I had asked for a solid introduction in the social history of the Netherlands, but the guide still felt he needed to make endless inane and borderline sexist jokes that all fell very flat. Oh well, the buildings were great and the people inside the buildings were giving quite interesting information, with the rosmolen being a high point:

[![From David Revoys sketchbook](/images/posts/2019/04_sketbook-at-krita-sprint-2019_by_david-revoy-768x1024.jpg)](https://krita.org/wp-content/uploads/2019/08/04_sketbook-at-krita-sprint-2019_by_david-revoy.jpg) From David Revoy's sketchbook

And as you can see, it gave the artists and developer/artists amongst us a chance to do some analog painting (althoug at least one sprint attendant tried to paint with Krita on a Surface tablet, unfortunately cut short by battery problems):

[![](/images/posts/2019/mills-1024x631.jpeg)](https://krita.org/wp-content/uploads/2019/08/mills.jpeg)

We followed up with dinner at an Indonesian restaurant, and went home tired but satisfied. There was still hacking and painting going on, though, until midnight.

## Thursday

Today we really had the core of our sprint. Some sprints are for coding, but this sprint was for bringing together people and gathering ideas. On Thursday, we discussed the future of Krita in quite a bit of detail.

In 2018/2019 the focus was fully on fixing bugs. There are now two full-time developers working on fixing bugs and improving stability more than this time last year, and both Boudewijn and Dmitry have dedicated all their coding time to fixing bugs as well. Weirdly enough, that doesn't seems to make much of a dent in our number of open bugs:

[![](/images/posts/2019/bugs-2019-08-12.png)](https://krita.org/wp-content/uploads/2019/08/bugs-2019-08-12.png) Bugs, open, new and closed, since April.

One reason is that we manage to introduce too many regressions. That's partly explained by our new hackers needing to learn the codebase, partly by an enormous increase in our user base (we're on track to break 2,500,000 downloads a year in 2019), but mostly by our changes not getting enough testing before releasing. So, taking things out of the order we discussed them at the meeting, let's report on our Bugs and Stability discussion first.

### Bugs and Stability

As David Revoy reports, the 4.2 releases don't feel as stable as the 4.1 releases. As noted above, this is not unexpected since we have two new full-time developers working on Krita, who aren't that deep in the codebase yet. Another reason we have so much trouble with the 4.2 releases is that we updated to Qt 5.12, which seems to come with many regressions we either have to fix in Qt (and we do submit patches upstream, and those are getting accepted), or work around in Krita itself. On the other hand, we are merging bug fixes into our release branch until the last minute before the release, so those fixes get barely any testing: so the lack of testing isn't something we can blame on our users, it's to a large extent our own fault.

Yet Raghukamath and Deevad noted that they both don't actually test master or the stable branch from day to day anymore because they are too busy actually using Krita, and the same goes for the other artists present. It's clear that the developers cannot do regression testing, that our extensive set of unittests (although most are more like integration tests, technically) doesn't catch the regressions -- we have to find a better way.

Coincidentally (or not...) Anna (who was not present) had started some time ago a discussion about this on phabricator: [T11021: Enhancements to quality assurance](https://phabricator.kde.org/T11021)). There are many parts to that discussion, but one thing we concluded, based on discussions during the sprint, is that we will try the following:

- We will release once a month, at the end of the month (we already try to do that...)
- We will merge bug fixes to the stable branch until the middle of the month: the merge window thus is two weeks, while master is always open to bug fixes.
- We will publish an article on krita.org telling our users what landed in the next stable version. That article will show up in all our users' welcome screen news widget, right inside Krita. There will be links to download a portable version of Krita for every OS.
- We will add a link to a survey (not bugzilla) in the welcome screen of those builds, and in the survey ask people for the results of testing the changes noted in the release article.
- And then, two weeks later, we will release the next stable version of Krita, with only fixes merged during the test period for noted regressions.

Slightly related: we also want to do a monthly update article on changes for master, but without the survey mechanism. However, that would make two development updates a month, which might be a bit much to digest, so we're starting slowly, with the stable release system.

### Development focus for 2019/2020

In October we will release a hopefully super-stable Krita 4.3, with a bunch of new features as well, but still focused on stability. Boudewijn is still working on fixing the resource handling system, but that is going really slow, and is being really hard. It's also hard for the maintainer of the whole project to find time to work on big coding projects, and it's getting harder, the more management-like tasks there are.

Everyone in the meeting agreed that the text tool still needs much more work, maybe even another rewrite to get rid of the dependency on Qt's internal rich text editor: the conversion between QTextDocument and SVG is lossy, and gives problems. We were all aware of the missing bits and the problems and bugs, so we didn't need to discuss this in detail. So one focus is:

- Text Tool: it is still not usable for the primary goal, namely comic book text balloons. We need to make it suitable. We know what to do, we just don't have the time while fighting incoming bugs all the time.

So it's clear that we still need to work on...

- Stability and performance. During the discussion some particular issues were noted:
    - Raghukamath reported that the move tool has become very slow. This definitely is a regression:
    - One year ago, at the 2018 Krita Sprint, we made a list of Unfinished Stuff, ranging from missing features after the vector rewrite, unimplemented layer style options, half-implement animated transform mask, missing undo/redo support in the scripting layer. Most of that is still relevant. See [the original sprint report](https://files.kde.org/krita/krita_meeting_docs/Other%20Meetings/2018%20Krita%20Sprint%20Meeting.odt).
    - Dmitry: noted he had made some expirements that show that we could make our brushes much faster by using new versions of AVX, but this would only help people with newer laptops. Boudewijn wondered whether the brush engines are the true bottleneck -- if the improvement only shows in benchmarks, users won't notice much difference. We might want to do another round of measuring using Intel's VTune, if we can get another license for a year.
    - Resource handling is still being rewritten. That means that when Steven noted that he cannot update a workspace, Boudewijn replied that is part of the bigger problem with the current resource system. Boud is rewriting that, and has been working on it for two years now, leading to [a huge merge request](https://invent.kde.org/kde/krita/merge_requests/54) -- big enough to almost bring gitlab to its knees. The rewrite might be be too big to actually finish, and it's hard to distribute the work over multiple developers.

Since we had some many artists around whose view we had never before been able to canvass, we decided that digging into workflow issues might be the best thing to do: it would make a good theme for the next fundraiser, too. So:

- - Workflow issues
        
        - Stefan brought in multiple issues with animation, like editing on multiple frames at the same time or finally getting the clones feature done. Most issues are already in bugzilla as wishes, but unfortunately, we don't have someone to work on animation full-time at the moment. Some progress was made and demonstrated during the sprint, though!
        - In the nineties and oughties, all desktop applications looked the same and followed more or less the same guidelines. That made sure that users knew they could investigate the contents of the application menus; it would be the first place to look for something relevant for their task at hand. That barely seems to happen anymore. So, discoverability of features in Krita is a problem that is getting worse. We made a list of things that were hard to find:
        - Our dockers are overcrowded and the contents hard to find; a docker hidden behind another docker isn't going to be discovered by many users.
        - If there are tabs in a single docker, like with the transform tool, and some of those tabs aren't visible because there are too many of them, like the liquify transform functionality, that functionality might as well not exist, it won't be found.
        - Deevad suggested making each transform tool option into a separate tool; however, as Raghukamath noted, the objection to that is that we don't want six new tools crowding the toolbox, nor having the weird pop-out tool selection buttons Photoshop has. This is a perennial discussion, and it's next to impossible to come to a conclusion here.
        
    - Related to that is the question of the tool options docker. Right now, users can choose between putting the tool options in a docker, or in a popup button on the toolbar. Another option would be to make a toolbar out of the tool options, with some pop-ups, like Corel Painter and Photoshop did. But none of these options is a real solution. We might do want to do a survey, but from experience. users want to have at least the overview, tool options, color selector, layer docker, brush preset docker visible, as well as some others, and on most displays, there just isn't the space for that...
    - Actually figuring out which dockers we have is pretty hard, too. Most people don't seem to find the dockers submenu in the settings menu, or in the right-click menu on the docker titlebars, and if they find it, the list is too intimidating.
    - So, one thing we decided to do is create a tool to search through Krita's functionality. Other applications are apparently facing the same problem, and this is an easy and cheap solution. Of course, people started asking for this tool to also search e.g. layer names. That lead to the thought that this is starting to look a bit like QtCreator's locator widget...
    - A workflow improvement Steven suggested was to autosave the current session (that is, open windows, views, images) and restoring this on restarting Krita.
    - Mariya said that the combination of clone layers and transform masks doesn't work as well for her as Photoshop's smart objects. After some discussion, it seems that we might want to rethink showing masks in the hierarchy if there's only one mask of a certain type: it's easier to show them as a toggle in the layer's row in the layerbox.
    - Sara asked whether Krita had a screen recorder. This should only record the canvas stroke by stroke and export to PNG or JPG. The old screen recorder could do this, but it was very broken and removed, and never intentionally released. This would be a biggish project, gsoc-sized, and needs to build on first finishing the porting to the generic strokes sytem, and then extend that system with recording. Another option would be to add a timer to save incremental versions and add an option to **export** incremental in addition to save incremental.
    - Emmett and Eoin discussed working with painting assistants: it would be interesting to make a hierarchy with grouped assistants. The conclusion was that we might want to show the assistants in the layer docker on top of the layers; other suggestions were a separate docker or putting the treeview in the tool option widget. If the first solution is chosen, it would be useful to also show reference images and maybe even guides in the layer^Wimage structure docker.

Some of the workflow issues mentioned already sound like new features, and then there were a number of discussions about what really would be new features:

- - It would help a lot with user support if the a statusbar indicator would show whether the stabilizer, canvas acceleration, instant preview (and others) are on or off. A screenshot would then immediately answer the questions we most ask users who need support.
    - After so many months of bug fixes, Dmitry really wants to work on one or two new brush engines: the first has thin bristles that could each have their own color. Sara mentions she really misses a brush like this. The other engine would be more like a calligraphy tool. Dmitry estimates needing two months per engine, which is quite a bit of time.
    - Eoin wants to have a tool, or a brush engine, or at least, something that would make it very easy to paste images or designs and transform them before pasting the next one. The images should come from an ordered or random collection. Currently, people use pipe brushes for that, but that is not convenient. A new tool is suggested.
    - Steven notes that it would be much more convenient to create a pipe brush from an animation on the timeline than the current system based on layers. This is true - we just never thought of it.
    - Mariya really wants to have a font selector where she can mark X fonts as her favourite and created a [wish bug for it](https://bugs.kde.org/show_bug.cgi?id=410809). It turns out that Calligra doesn't have widget like that, and the standard Qt Font combobox doesn't support it either, nor does Scribus: it might be that such a thing hasn't been written in Qt.

Anoother thing that was discussed briefly was telemetry (we tried that, the project failed).

### Marketing and Outreach

Our presence on Twitter, Mastodon, Tumblr, DeviantArt, Reddit is fine. On Facebook, non-official groups are more used than Krita's own account (which is because Boud is the last maintainer standing, and he cannot stand facebook). Youtube needs improvement, we are absent on Instagram.

#### Instagram

Sara Tepes volunteers to handle Krita's instagram account (which we don't have). Sara also wants to run "competitions" on Instagram with the prize being having the a number of selected images shown on either Krita's splash or Krita's welcome screen.

The splash screen is our main branding location, so we shouldn't put other images in there other than the holiday jokes.

We could redesign the welcome screen to include an image location; it needs redesign in any case because it's too drab right now. We wanted it to be not in-your-face, but it's a bit too much not so now.

Once we have the image location, getting and selecting images can be a problem, as it was for the art book or main release announcements. Sara notes that instagram gives easy tools to select images from a larger set; other platforms are not so good.

In any case, selecting images will be quite a bit of work, and we do need to make sure we're not playing favorites or forgetting where we come from: free software, open culture.

Conclusion: we are going to try to run the competition on all social networks for which we have a maintainer (instagram, twitter, mastodon, reddit). We can always extend this later to other places. Each maintainer can propose two images + attribution info + links, which will be shown in rotation for a month.

The system for doing this should be ready for the 4.3 release in October.

Note: we have to make a page with a very clear text explaining the rules: we don't take ownership of the images, the images will be shown in Krita, there will be no licensing requirements for the images, certain kinds of images cannot be used.

Note 2: Scott should ask Ben Cooksley how we can get the welcome screen news widget traffic information on a regular basis.

#### YouTube

We have already started improving our presence on YouTube. We feature existing Krita-related channels, and we are working with Ramon to provide interesting videos. We could do more, but let's give Ramon a chance to build up some momentum first.

### Development Fund and Fundraiser

Financially, Krita is doing okay. We do get between 2000 and 2700 euros a month in donations: that translates to one full time developer (yes, we're not getting rich from working on Krita, these are not commercial fees). Windows Store + Steam bring in enough for three to four extra full-time developers. It would be good to become less dependent on the Windows Store, though, since Microsoft is getting more and more aggressive in promoting getting applications from the Windows Store.

Enter the Krita Development Fund. Like in most things, we try to look at what Blender is doing, and then try to find out whether that works for us. Often it does. We already have a notional Development Fund, but it's basically a monthly paypal subscription or recurring bank transfer. We don't have any feedback or extras for the subscribers, and the subscribers have no way to manage their subscription, or reach us other than in the usual way. We tried to implement a [CiviCRM](https://crm.krita.org/civicrm/dashboard) system for this, but that was way too complex for us to manage.

We need to reboot our Development Fund and migrate existing subscribers to the new fund. A basic list of requirements is:

- - - A place on the website where people can subscribe and unsubscribe
        - A place where the names of people who want that are shown
        - A way to tell people what we are doing with the money and what we will be doing
        - Make sure companies and sponsors will also be able to join

And no doubt there will be other considerations and requirements. We should check [Blender's dev fund website](https://developer.blender.org/source/blender-dev-fund/), of course. We created a [Phabricator task](https://phabricator.kde.org/T11352) to track this, and it's something we really want help with!

### What wasn't discussed

Interestingly, the new gitlab workflow seems to work for everyone. Gitlab's UI is even less predictable and discoverable than Krita's, but we didn't need to discuss anything, people can work with it without much trouble.

Steam wasn't much of a discussion item either: Windows is doing fine on Steam, our macOS version of Krita still has too many niggles to make it worth-while to put on Steam (or the Apple Store either, even if that were possible, license-wise), and the Linux market share is still too small to make it worth the time investment: still Emmet promised to contact Valve to see how we can get the appimage into Steam. At a first glance, the problem seems to be the version of libc required, which might mean we'll have to figure out a way to build Qt 5.12 on older versions of Ubuntu or CentOS. But let's wait and see, first.

Tangentially, we did discuss how to get more people involved in user support, but Agata already has plans towards involving people who already trying to help others in places like Reddit and the forum more recognition. It was late, and the discussion degenerated into hilarity pretty soon -- still, this is something to work on, since the core development team just doesn't have the capacity anymore to help every new Krita user's teething problems anymore.

### Tasks

To create: a task for rethinking what goes into dockers, and what goes somewhere else.

- [T11351 Team Page for krita.org](https://phabricator.kde.org/T11351)
- [T11352 Rethink Krita development fund](https://phabricator.kde.org/T11352)
- [T11346 Welcome Screen refresh](https://phabricator.kde.org/T11346)
- [T11343 Quick Action search functionality](https://phabricator.kde.org/T11343) (branch started)
- [T11345 Assistant Manager](https://phabricator.kde.org/T11345)
- [T11350 Stamp Brush / Tool Proposal](https://phabricator.kde.org/T11350)
- [T11344 Screen Recording](https://phabricator.kde.org/T11344) (bring back MACROs)
- [T11355 General feedback android version](https://phabricator.kde.org/T11355)

## Friday

Friday was the real hacking day. Some people already started leaving, but many people were staying around and started hacking on the issues identified during the meeting, like the action search widget. Bugs were being fixed, regressions identified and blogs posted. And even later on, on Saturday and Sunday, there was still hacking, like on the detached canvas feature.

[![](/images/posts/2019/DSC00293-e1565439023332-1024x768.jpg)](https://krita.org/wp-content/uploads/2019/08/DSC00293-e1565439023332-1024x768.jpg) All the sprinters together again, photo taken by Krzyś
