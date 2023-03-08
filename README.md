# TabOverride - [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=for-the-badge)](https://github.com/TheDanniCraft/NewTab-Override/issues) 
Some browsers like OperaGX block overwriting the default "New Tab" page. With a little trick, you can bypass this restriction. This repo contains instructions that make it relatively easy to implement it in your own extension.

If the repo helps you, I would appreciate a star on GitHub. If you use the script in your extension, I would appreciate an attribution or a [donation](https://www.tipeeestream.com/thedannicraft/).

## How to implement it?

1. Drag the [`newTab-override.js`](https://github.com/TheDanniCraft/NewTab-Override/blob/main/newTab-override.js) file into your project. 
2. Modify the [`tabURL`](https://github.com/TheDanniCraft/NewTab-Override/blob/main/newTab-override.js#L4) variable (line 4) to your needs.

3. Inside your extensions `manifest.json` add the following line to the `background` property:
```json
"service_worker":  "background.js"
```
4. Inside your extensions `manifest.json` add the following line to the `permissions` array:
```json
"tabs"
```


It should now look similar to this:
```json
...
"background": {
  "service_worker": "background.js"
},
  "permissions": ["tabs"]
...
```
> ❗Don't forget to reload your extension❗

**That's it!**
When you now open a new tab 

## Contribute

Feel free to open a pull requests if you feel that you made useful changes to the repo.
Whether it's fixing typos, implementing new features, or anything else.

I appreciate all contributions!

## Roadmap

 - [x] Override new tab page
 - [x] Tested on manifest v2 & v3
 - [ ] Add browser check (script will not execute on browsers that don't need it)

Many more coming soon...

![HitCount](https://hits.dwyl.com/TheDanniCraft/NewTab-Override.svg)
