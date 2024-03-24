# Adding FbkStickers to Matrix on Element
1. Enter command `/devtools` in the chat box.
2. Look for the `Custom` tab. Click `Explore account data`.
3. Search for `m.widgets` and click on it to edit.
4. Paste the following code and click `Send`.
```json
{
  "stickerpicker": {
    "content": {
      "type": "m.stickerpicker",
      "url": "https://m-stickers.fbk.moe/?theme=$theme",
      "name": "FbkStickers",
      "creatorUserId": "@<YOUR_NAME>:<YOUR_HOMESERVER>",
      "data": {}
    },
    "sender": "@<YOUR_NAME>:<YOUR_HOMESERVER>",
    "state_key": "fbkstickers",
    "type": "m.widget",
    "id": "stickers-fbkmoe"
  }
}
```

Where as `<YOUR_NAME>` is your username and `<YOUR_HOMESERVER>` is your homeserver url.

# Maunium sticker picker
A fast and simple Matrix sticker picker widget. Tested on Element Web, Android & iOS.

## Discussion
Matrix room: [`#stickerpicker:maunium.net`](https://matrix.to/#/#stickerpicker:maunium.net)

## Instructions
For setup and usage instructions, please visit the [wiki](https://github.com/maunium/stickerpicker/wiki):

* [Creating packs](https://github.com/maunium/stickerpicker/wiki/Creating-packs)
* [Enabling the widget](https://github.com/maunium/stickerpicker/wiki/Enabling-the-widget)
* [Hosting on GitHub pages](https://github.com/maunium/stickerpicker/wiki/Hosting-on-GitHub-pages)

If you prefer video tutorials, [Brodie Robertson](https://www.youtube.com/c/BrodieRobertson) has made a great video on setting up the picker and creating some packs: https://youtu.be/Yz3H6KJTEI0.

## Comparison with other sticker pickers

* Scalar is the default integration manager in Element, which can't be self-hosted and only supports predefined sticker packs.
* [Dimension](https://github.com/turt2live/matrix-dimension) is an alternate integration manager. It can be self-hosted, but it's more difficult than Maunium sticker picker.
* Maunium sticker picker is just a sticker picker rather than a full integration manager. It's much simpler than integration managers, but currently has to be set up manually per-user.

| Feature                         | Scalar | Dimension | Maunium sticker picker |
|---------------------------------|--------|-----------|------------------------|
| Free software                   | ❌     | ✔️        | ✔️                     |
| Custom sticker packs            | ❌     | ✔️        | ✔️                     |
| Telegram import                 | ❌     | ✔️        | ✔️                     |
| Works on Element mobiles        | ✔️     | ❌        | ✔️                     |
| Easy multi-user setup           | ✔️     | ✔️        | ❌<sup>[#7][#7]</sup>  |
| Frequently used stickers at top | ❌     | ❌        | ✔️                     |

[#7]: https://github.com/maunium/stickerpicker/issues/7

## Preview
### Element Web
![Element Web](preview-element-web.png)

### Element Android
![Element Android](preview-element-android.png)

### Element iOS (dark theme)
![Element iOS](preview-element-ios.png)
