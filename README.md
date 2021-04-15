# fcklca

> "**NOTE:** just intended for proof of concept, no real harm should be generated with this code"

proof of concept that you are able to generate endless number of garbage accounts for any location

The demo can be accessed on [gh pages](https://windyz0re.github.io/fcklca/) for having a proof of concept on the go.

## How to use?

I am an backend guy. So I'm just not able to create a good interface or interact with browser rules.
But I got it working to have an QR Code Scanner with that you can scan the qr-codes yourself which extract the certain id. Or open a file, or eneter the link manually.

For the requests to work, you need to disable cors. I suggest [chrome moesif-origin-cors-change](https://chrome.google.com/webstore/detail/moesif-origin-cors-change/digfbfaphojjndkpccljibejjbppifbc).
Otherwise you can now enable a CORS proxy, which allows you to bypass CORS rules (for this we use https://cors.bridged.cc/). We suggest to only use this service for demo purposes
if you are on the go on mobile devices.

Just click generate and take a look at your network requests in the dev tools.

## Does this really work?

![ezgif-3-f88fc19343d3](https://user-images.githubusercontent.com/82541913/114861089-17f9f800-9ded-11eb-82ce-7845d64a1c91.gif)

## How does this work?

I just rebuilt the cryptography checkin mechanism that can accept any Luca App QR Code and checks it in on your desired location.
The App is written in JS and delivered in an minified version. With some pretty print and debugging, you can simply rebuild
the process of how the request is constructed for checkin.

The random user qr code data is generated by the code from https://wolf128058.gitlab.io/schmudo2go. I just feed the data into
my functions and checkin some fake garbage data. The point here is, that the luca app accepts this data no matter if it is
garbage or actual data. This allows you to create events with thousands of visitors from aynwhere in the world.

Due to this, the public QR code for visitors to check themselves in, needs to be handled like a password.

The code from the luca app in random unsorted notes can be found [here](https://github.com/windyz0re/fcklca/blob/de908d673aa90199db8eb8ca6634fbe2d53b2f73/index.html#L262).

## Why?

I spent a day reversing the luca app and finding some issues. I'm not a security expert, just a student somewhere in the
world that anted to code instead of learning for his exams.

## Why so bad syntax?

I'm no js professional. Additionally, I'm currently really cold and hungry, as I haven't done anything else today. I will just
finish this for today, submit it to some news sources and scream on twitter about it, and then I'll see.

## TODO

- [x] handle cors stuff
- [x] host on gh pages
- [x] built-in qr code scanner
- [x] better interface
- [ ] qr scanner with camera
- [ ] fix final issues with the data field in the checkin data ([line with the issue](https://github.com/windyz0re/fcklca/blob/main/index.html#L406))
- [ ] replace fake qr code generate with "real" possible data from faker (this means replacing the [random faker](https://wolf128058.gitlab.io/schmudo2go) with the one from the luca app to feed the system with faked personal data)

Let us see who is faster. Fixing the bug or finishing theses TODOs.

## What's missing?

Sadly we **currently** cannot access the certain location vists counters anymore. But this is still a goal the get up
and working again, so you can view your fake requests increase the visit counter.

## LICENSE

Just use it as you wish. Modify it. Share it.

#### Libraries

- [qr-scanner](https://github.com/nimiq/qr-scanner)
- [forge](https://github.com/digitalbazaar/forge)
- [elliptic](https://github.com/indutny/elliptic/)
- [sha256](https://github.com/dchest/fast-sha256-js)
