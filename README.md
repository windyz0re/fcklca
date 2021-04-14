# fcklca

> "**NOTE:** just intended for proof of concept, no real harm should be generated with this code"

proof of concept that you are able to generate endless number of garbage accounts for any location

## How to use?

I am an backend guy. So I'm just not able to create a good interface or interact with browser rules.
So just scan the QR Code of a certain location, extract the id at the end and enter it into the
input field. For the requests to work, you need to disable cors. I suggest [chrome moesif-origin-cors-change](https://chrome.google.com/webstore/detail/moesif-origin-cors-change/digfbfaphojjndkpccljibejjbppifbc).

Just click generate and take a look at your network requests in the dev tools.

To serve this http page, open as an file or just start a python static file server `python -m http.server 8080` and open `localhost:8080`

## Why?

I spent a day reversing the luca app and finding some issues. I'm not a security expert, just a student somewhere in the
world that anted to code instead of learning for his exams.

## Why so bad syntax?

I'm no js professional. Additionally, I'm currently really cold and hungry, as I haven't done anything else today. I will just
finish this for today, submit it to some news sources and scream on twitter about it, and then I'll see.

## TODO

- [ ] handle cors stuff
- [ ] host on gh pages
- [ ] built-in qr code scanner
- [ ] better interface
- [ ] fix final issues with the data field in the checkin data

Let us see who is faster. Fixing the bug or finishing theses TODOs.

## LICENSE

Just use it as you wish. Modify it. Share it.