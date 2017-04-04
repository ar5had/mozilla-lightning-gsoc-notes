## Important Points

* Prefer to message on mailing list or public group then personal message. 

* Start a new bug if the bug that you have found is already marked resolved. 

* Concentrate on the process instead of the code. Link some of the best written code to your proposal and obviously best looking work as well.

* For the gsoc process, it would be good to see how you would do the planning. This includes identifying components that are easy to work upon and components having least dependencies.

* It also includes the timeframe, to see how long you believe you would take for each part of the project. The goal is not for you to do as much as possible in as little time as possible, but much more that the estimates are detailed and realistic

* So not just something like: Week 3-4: migrate Dialog X. Week 5-6: migrate Dialog Y, but rather going into details. You can count 1 point per half a work day in your estimates, so it would be someting like: create basic structure for dialog X: 2pt, move component X from XBL to react: 4pt.

* Tasks that are more than 5-6 points should be split up.. kind of like the scrum points system, if you have experience with that.

* If you want, you could of course also create a html rapid prototype for one dialog. This of course doesn't have to be fully functional nor styled perfectly, but it should show your skills creating react components and html. You are welcome to show your UX skills if you believe the dialog you are converting is not ideal, in this case it would be good to write.

* Write down your thoughts on what you are changing and why.

* Feel free to ask community and mentor's feedback at different stages while you are creating your application.

* If you get remote xul warning, then set dom.allow_XUL_XBL_for_file to true. You can set it by going to EDIT > PREFERENCES > ADVANCED > CONFIG EDITOR

* To do the same thing in browser, goto `about:config` and search for `dom.allow_XUL_XBL_for_file` if found set it true else right click and add new boolean.

* Weekly basis is pretty broad for deliverables, it would be best to plan deliverables using the points system. Calculate how many weeks you have, 5 days per week, 2 points per day. Then you know how many points you have for planning. Then break down each task into small units, not more than 5 points

* Set `set.calendar.item. something` to true to get events in tab.

* Set `calendar.item.useNewItemUI` to open html version of event dialog. 

* The good thing about dialogs is that there is not much to integrate, as most things can happen separate. Event dialog is to create a xul framework with an iframe that contains the html. postMessage was used to exchange messages from xul to HTML

* With a similar approach you could easily develop the html outside of Lightning with the tools you are comfortable with, abstracting everything that needs XUL interaction using postMessage. You could create a simple container so that you can develop even this with your standard html, then just drop in the html into the xul container.

* [Event in Tab](https://wiki.mozilla.org/Calendar:Event_in_a_Tab/documentation)

* [Frontend Mozilla React Redux etc](https://dxr.mozilla.org/comm-central/source/mozilla/devtools/docs/frontend)

* [Mockup N](https://wiki.mozilla.org/images/1/16/Event-in-tab-mockup-n.svg)

* To make sure you dont use same obj-dir files for fx and tb- by adding `mk_add_options MOZ_OBJDIR=path/to/your/obj-dir`(use absolute paths) to mozconfig.
