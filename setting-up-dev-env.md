## Building dev environment for Thunderbird

1. Goto [Simple Thunderbird Build](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Simple_Thunderbird_build)

2. Build prequisites. If they somehow don't work and you dont succesfully install the prequisites, don't worry and just move on.

3. Clone the comm-central repo. The svn client used by mozilla for this project is Mercurial so make sure what command you are running. Goto [Mercurial Help] (https://developer.mozilla.org/en-US/docs/Mercurial) for more info about Mercurial.

4. Get into the comm-central directory and run `python client.py setup`.

5. Create a new file mozcconfig and add `ac_add_options --enable-application=mail` if you want thunderbird to build else firefox will build.

6. Add `echo `ac_add_options --enable-calendar` to the next line in the mozconfig file if you want to enable calendar(Lightning is the project name). 

7. Several mozilla project use `mach` as command line tool to do development stuff so make sure you know its command. I wasted nearly 6 hours just my missing the `mach clobber` command. BTW this command removes the obj-dir or build files so that you can start a fresh build.

8. Run `./mozilla/mach bootstrap` in the terminal to install prequisites. This is probably doing the same thing as step 2 but it is specifically for thunderbird maybe. Although I am not sure. In case this commands fails, don't worry just follow the steps.

9. Run `./mozilla/mach build` to build the the repo. This command will probably take significant amount of time. This step is important so if this step fails then ask for help either on [google group](https://groups.google.com/forum/#!forum/mozilla.dev.builds) or irc channels or any other forum/place that you are aware of.

10. Run `./mozilla/mach run` to run the build app. Make sure you make profile first before starting the development work, it will make your development life easier for this project. To make profile, run `./mozilla/mach run -P` and you can start building ur app with any profile that you've crated with `./mozilla/mach -P ProfileName`.

11. If you are interested in calendar project, everything in `calendar/` directory is used for Lightning. The layout is somewhat historical where it still had the split between Sunbird and Lightning, that is why you see `calendar/lightning/` directory. You should check out the files in `calendar/base/public`, they describe the basic objects used in Lightning. The frontend is mostly in `base/content`. The backend is mostly in `base/src`. Daily is the development name for thunderbird, maybe it is similar to what `Chromium` is for 'Google Chrome'.

12. If you are interested in Lightning project, then enable it in extension tab and restart or rerun the build by './mozilla/mach run'.

### Some helpful links
* [Mercurial Help] (https://developer.mozilla.org/en-US/docs/Mercurial) 
* [Working with Mozilla Source Code ](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Source_Code)
* [Getting mozilla source code] (https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Source_Code/Mercurial)