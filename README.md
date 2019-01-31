# Plex Wake/Redirect
If you want to run a plex server (or any kind of server, for that matter), but don't want to have your computer awake 24/7, use this lambda function!

## Set up wake-on-lan
Various guides can be found on how to do this, [here's one!](https://www.howtogeek.com/192642/how-to-remotely-turn-on-your-pc-over-the-internet/)

## Lambda function
You can deploy the function however you like, I personally use [Apex](http://apex.run/) and have included an example function.json, just supply the role you'd like your function to take.

You must also supply the following environment variables:
```json
{
    "TARGET_IP": "YOUR.ROUTER.IP",
    "WAKE_PORT": "YOUR.WAKE.PORT",
    "TARGET_URL": "yourplexserver.com",
    "MAC_ADDR": "YOUR:MAC:ADDRESS"
}
```

## Usage
After setting up the lambda function, all you have to do is set up an API gateway for your lambda, and you're on your way!