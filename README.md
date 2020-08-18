## What is it?

xfce4-screenshooter allows you to capture the entire screen, the active 
window or a selected region. You can set the delay that elapses 
before the screenshot is taken and the action that will be done with 
the screenshot: save it to a PNG file, copy it to the clipboard, open 
it using another application, or host it on imgur.com,
a free online image hosting service.

A plugin for the Xfce panel is also available.


## Installation

The file [`INSTALL`](INSTALL) contains generic installation instructions.


## Debugging Support

xfce4-screenshooter currently supports three different levels of debugging support,
which can be setup using the configure flag `--enable-debug` (check the output
of `configure --help`):

| Argument  | Description |
| -------   | ----------- |
|  `yes`    | This is the default for Git snapshot builds. It adds all kinds of checks to the code, and is therefore likely to run slower. Use this for development of xfce4-screenshooter and locating bugs in xfce4-screenshooter. |
| `minimum` | This is the default for release builds. **This is the recommended behaviour.** |
| `no`      | Disables all sanity checks. Don't use this unless you know exactly what you do. |


## How to report bugs?

Bugs should be reported to the [Xfce bug tracking system](https://bugzilla.xfce.org)
against the product xfce4-screenshooter. You will need to create an account for yourself.

## How to upload images to your imgur account?
[Register an Imgur APIv3 application](https://api.imgur.com/oauth2/addclient)

In file `xfce4-screenshoter` located in `$HOME/.config/xfce4` add
```use_imgur_auth=true```

Then obtain an authorization token by sending a request to URL following this pattern
```
https://api.imgur.com/oauth2/authorize?client_id=YOUR_CLIENT_ID&client_secret=YOUR_SECRET&response_type=token
```
More information https://apidocs.imgur.com/?version=latest#authorization-and-oauth

Add obtained data to `xfce4-screenshoter` configuration file:

```
client_id=yourclientid
client_secret=yoursecret
token=yourtoken
```
