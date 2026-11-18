# Privacy Policy for Payment Validator

- **Effective date:** 18 November 2026
- **Last updated:** 18 November 2026
- **Publisher:** Josh Thompson
- **Contact:** josh@eastern-web.com
- **Website:** https://eastern-web.github.io/payment-validator-site/

Payment Validator is a browser extension for Google Chrome and Microsoft Edge. It looks at checkout pages in your browser and shows how well the card details on the page are isolated. This policy explains what the extension reads, what it stores, and when it connects to the internet.

In short: the extension works inside your browser. It never reads what you type, never sends the pages you visit anywhere, and connects to the internet only for its licence, through ExtensionPay.

## 1. What the extension reads on a page

To calculate a score, the extension reads the structure of the page in your browser's memory:

- element types and attributes, such as `type`, `name`, `id`, `autocomplete` and `inputmode`;
- the addresses that the page's frames and scripts load from;
- whether the page is served over HTTPS.

It never reads the values of form fields. That means it never sees card numbers, security codes, expiry dates, names, addresses or passwords. Nothing it reads from a page is stored or sent anywhere. The score is calculated entirely in your browser.

## 2. What the extension stores

### On your device only (`chrome.storage.local`)

- **Trusted sites.** If you choose "I trust this site" (on the toast) or "Trust this site" (in the popup), the site's domain and the score it had at that moment are saved, so its toast stays quiet. Only sites you choose are saved.
- **Licence cache.** Your Pro licence, if you have one, so paid features keep working when you're offline.
- **Trial state.** A copy of the time your 7-day trial started, and a flag recording that installation has finished, so the extension can work out your trial without connecting to the internet.

### Synced with your browser profile (`chrome.storage.sync`)

If browser sync is turned on, your browser copies this data to your Google or Microsoft account so it can follow you between devices. If sync is off, it stays on your device.

- **Trial start time** (`trialStartedAt`). An anonymous timestamp, so the trial isn't restarted by reinstalling the extension. It contains no account, name or email.
- **ExtensionPay data**, written by ExtensionPay's licence library:
  - `extensionpay_installed_at`: when the extension was installed. Stored at install for every user.
  - `extensionpay_api_key`: a key that identifies this installation to ExtensionPay. Created the first time you open ExtensionPay's purchase page or its "Restore purchase" login.
  - `extensionpay_user`: your licence record from ExtensionPay, saved after each licence check. If you have bought Pro or logged in to restore it, this includes the email address you used.

## 3. When the extension connects to the internet

The extension makes no network requests until you first open ExtensionPay's purchase page or choose "Restore purchase". From then on, it checks your licence with ExtensionPay (extensionpay.com) when the browser starts, when the extension is installed or updated, and after a payment or a restore login.

Pro is sold through ExtensionPay, and card payments are taken by Stripe on ExtensionPay's checkout. You enter your card details on their pages, never in the extension, and the extension never receives them. How they handle your data is set out by them, not by this policy:

- ExtensionPay: https://extensionpay.com/
- Stripe: https://stripe.com/gb/privacy

The extension sends no analytics, uses no tracking and loads no remote code.

## 4. Permissions

- **`storage`**: saves the data described in section 2.
- **`activeTab`**: when you click the toolbar icon, lets the popup read the current tab's address, to tell a browser page that can't be scanned from a tab that just needs reloading.
- **Content script on all `http://` and `https://` pages**: finds checkout card forms on any shop and shows the score. Plain `http://` is included so the extension can warn you when a checkout isn't encrypted.
- **Content script on `https://extensionpay.com/*`**: tells the extension when a purchase or restore on ExtensionPay's pages has finished.

## 5. Deleting your data

- **Uninstalling** the extension removes the data on your device. In testing with browser sync turned off, it also removed the synced data.
- **With browser sync turned on**, your browser may keep the synced data in your account and restore it if you reinstall the extension. To delete it:
  - **Chrome:** go to https://chrome.google.com/data and select "Delete data". This deletes all of your Chrome sync data, not only this extension's.
  - **Edge:** open Settings, then Profiles, then Sync. Turn off the data types you want removed, then select "Still having sync problems? Try another option" and "Reset sync". Keep the browser open until it finishes.
- **ExtensionPay** holds its own record of your licence and, if you bought Pro, your email address. Contact ExtensionPay through https://extensionpay.com/ about the data it holds.

## 6. Children

The extension is not directed at children under 13 and doesn't knowingly collect their data.

## 7. Changes to this policy

If the extension's handling of data changes, this policy will be updated in the same release, with a new "Last updated" date.

## 8. Contact

Questions about this policy or the extension: Josh Thompson, josh@eastern-web.com.
