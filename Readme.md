Certainly! Let's expand the GitHub description to make it more SEO-friendly and add additional content:

---

# YouTube Mass Unsubscribe Script

## Overview

Are you overwhelmed with a cluttered YouTube subscription list? Do you wish there was a faster way to clean up your subscriptions? Look no further! Introducing the YouTube Mass Unsubscribe Script – an innovative JavaScript tool designed to simplify the process of unsubscribing from YouTube channels in bulk. Declutter your subscription feed and regain control over your content consumption with this efficient and user-friendly script.

## Features

- **Bulk Unsubscribe:** Unsubscribe from all your YouTube channels with just one click.
- **Time-Saving:** No more manual unsubscribing; let the script handle the heavy lifting.
- **User-Friendly:** Simple and intuitive script suitable for users of all experience levels.

## How to Use

1. **Open Your YouTube Subscription Section:**
   - Visit YouTube and log in to your account.
   - Navigate to the 'Subscription' section to view your subscribed channels.

2. **Access the Console:**
   - Right-click anywhere on the page.
   - Select 'Inspect' to open the browser's Developer Tools.
   - Go to the 'Console' tab.

3. **Paste the Script:**
   - Copy the script provided in the repository.
   - Paste it into the console and hit 'Enter'.

4. **Sit Back and Relax:**
   - Witness the script efficiently unsubscribing you from all channels.
   - The process duration may vary based on your subscription count.

## Script Details

This powerful script is crafted with the latest JavaScript technologies, ensuring compatibility across various browsers for a seamless user experience. Take advantage of automation to simplify your YouTube channel management and start fresh with a more tailored content feed.

// Via: https://www.thewindowsclub.com/how-to-unsubscribe-from-all-your-youtube-channels-at-once

// ⚡ Change language to English before run

/**
* YouTube bulk unsubscribe fn.
* Wrapping this in an IIFE for browser compatibility.

*/<code>
(async function iife() {
    // This is the time delay after which the "unsubscribe" button is "clicked"; Change it as per your need!
    var UNSUBSCRIBE_DELAY_TIME = 2000
    /**
    
    * Delay runner. Wraps `setTimeout` so it can be `await`ed on.
    
    * @param {Function} fn
    
    * @param {number} delay
    
    */
    var runAfterDelay = (fn, delay) => new Promise((resolve, reject) => {
      setTimeout(() => {
        fn()
        resolve()
      }, delay)
    })
    // Get the channel list; this can be considered a row in the page.
    var channels = Array.from(document.getElementsByTagName(`ytd-channel-renderer`))
    console.log(`${channels.length} channels found.`)
    var ctr = 0
    for (const channel of channels) {
      // Get the subscribe button and trigger a "click"
      channel.querySelector(`[aria-label^='Unsubscribe from']`).click()
      await runAfterDelay(() => {
        // Get the dialog container...
        document.getElementsByTagName(`yt-confirm-dialog-renderer`)[0]
          // and find the confirm button...
          .querySelector(`[aria-label^='Unsubscribe']`).click()
        console.log(`Unsubsribed ${ctr + 1}/${channels.length}`)
        ctr++
      }, UNSUBSCRIBE_DELAY_TIME)
    }
  })()
  </code>

## Important Note

- **Use Responsibly:** Exercise caution and responsibility when utilizing this script, as mass unsubscribing may have irreversible effects.
- **Backup Recommendations:** Consider creating a backup of channels you wish to retain before using the script.

## Contributions

We welcome contributions to enhance the script's functionality and address any potential concerns. Feel free to submit pull requests or report issues on our [GitHub repository](link to the repository).

## Disclaimer

This script is provided on an as-is basis, without any warranties. Use it at your own risk, and the developers are not liable for any unintended consequences.



YouTube Unsubscribe Script, Mass Unsubscribe, YouTube Channel Management, JavaScript Automation, Unsubscribe All Channels, YouTube Tools, Browser Script, YouTube Cleanup, Declutter Subscriptions, Optimize YouTube Feed, Open Source.

## Support

For issue resolution or feature suggestions, please [open an issue](link to the issues section) on GitHub. Engage in general discussions and connect with our community on our [forum](link to forum).

---

Feel free to modify the content further based on your preferences and any additional details you'd like to include.
