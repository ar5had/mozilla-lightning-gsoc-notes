## Questions

Q1.  Is Daily similar to what chromium is to google chrome?

Q2.  What's the difference between comm-central and mozzila-central and when to choose what?

A2. `comm-central` is the repo for thunderbird which works on the top of firefox as it has inbuild browser functionality. `mozilla-central` is the repo for firefox browser. 

Q3. If same bug is present in `mozilla-central` and `comm-central`, should I need to make two separate patch?

A3. No, you can make one patch for `mozilla-central` and the browser code of `comm-central` will be in sync with it.

Q4. What is review directory ? `hg push -r . review` will just push those in the current branch not in review directory. Does review directory mean cwd?
	
Q5. What's the difference between `command` and `click` attribute?

Q6. Should I have to use ES6 or ES5 syntax?

Q7. How keyboard shortcuts will trigger react componets(access keys)?

Q8. What about css and what font-size and all other stuff of styling?
