# wlist

A command-line tool for Wunderlist with two goals:
 
1. Provide an easy to use way to explore the API and its output for developers
2. Allow shell scripting of the API for integrations
 
## Requirements

To use this tool, you’ll need the following:

* Ruby, should be on your system
* An client id. You can get one at the [Wunderlist Developer Site](https://developer.wunderlist.com/applications). Once you have it, you’ll want to set it in the `WLIST_CLIENT_ID` environment variable.  
* An access token. You can obtain one by using `wlist login`. Once obtained, set it in the `WLIST_ACCESS_TOKEN` environment variable.

If you try to use `wlist` without a `WLIST_CLIENT_ID` set, you’ll get gently nudged in the right direction:


    bash-3.2$ bin/wlist inbox
    Missing $WLIST_CLIENT_ID in environment
    Visit https://developer.wunderlist.com/applications and create an app!

Likewise with the access token

    bash-3.2$ bin/wlist inbox 
    Missing $WLIST_ACCESS_TOKEN in environment. Please run:
    > wlist login
    
## An example walk through