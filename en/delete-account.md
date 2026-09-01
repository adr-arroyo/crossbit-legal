---
permalink: /en/delete-account.html
---

# Delete your CrossBit account and data

This page is publicly available so that you can request deletion without installing
the app.

**Last updated:** 1 September 2026. To request deletion, email
**crossbitapp@gmail.com** from the address associated with your account with the
subject **“Delete CrossBit account”**. You can also start deletion in the app under
Settings → Account → Delete cloud account.

## 1. Local device data

From the app, use *Settings → My data → Delete local data*. This deletes CrossBit
workouts, meals, metrics, chat history, plans, records, templates, preferences and
settings, together with the native local backup when present. Uninstalling CrossBit
removes the app's local storage, but exported files or backups saved in the device's
documents folder may remain and must be deleted separately.

## 2. Cloud account data

Account deletion reauthenticates the email/password session and starts an idempotent
remote workflow. If the workflow is temporarily in progress or fails, the app shows
the status and lets you retry; local data is not deleted until remote deletion has
completed and you explicitly choose to delete it.

When completed, the workflow deletes the Firebase Authentication account, the
CrossBit subscription profile, RevenueCat customer association where applicable,
usage and idempotency records, purchase webhook receipts, and voluntary AI-content
reports associated with the account. The deletion checkpoint is a minimal technical
record used to complete or verify the workflow; it contains no health or chat content.

Retention limits are:

- usage and idempotency records: no more than 40 days if not deleted earlier;
- voluntary AI-content reports: no more than 30 days if not deleted earlier;
- purchase webhook receipts: no more than 90 days if not deleted earlier;
- billing and purchase records held by Google Play, the App Store or RevenueCat: as
  required by their policies and applicable accounting or tax obligations.

Deleting the account does not cancel an active Google Play or App Store subscription.
Cancel it separately in the subscription settings of the relevant store.
