# Creating and maintaining license keys for customers

Sourcegraph requires site administrators to input a license key to have access to various [paid features](https://about.sourcegraph.com/pricing). This page explains how to create, use, and maintain license keys for prospects and customers.

Valid license keys can only be generated by site administrators on Sourcegraph.com.

License keys are created and managed on Sourcegraph.com in the **Site-admin > Subscriptions** page. Once a license key has been created for a user, they can sign in to Sourcegraph.com to access it from their user profile.

## How to create a license key for a renewal or upgrade

If an existing company or customer needs a new license key for any reason (e.g., they purchase more seats, they upgrade product tiers, or they simply renew), you can add a new license key to an existing subscription.

Visit the **Site-admin > Subscriptions** page, find the existing subscription, click into it, and follow the steps below (from the "Click **Generate new license manually**" step onwards).

## How to create a license key for a new prospect or new customer

> NOTE: CEs should always consult with Sales before creating license keys for prospects (i.e., companies that have not yet officially become customers).

First, the company's Sourcegraph administrator must create a Sourcegraph.com user account and provide their username. Once that is available,follow the steps below.

- Sign in to Sourcegraph.com and visit the **Site-admin > Subscriptions** page and click **Create product subscription**.
- Find the username and click the **Create product subscription** button.
- Click **Generate new license manually**.
- Add the appropriate tags to the input box (separated by commas, with no spaces). Commonly used tags include:
  - `true-up` to allow the company to go over the user limit on the license.
  - `mau` to indicate that the company is on a monthly usage-based billing model.
  - `trial` to show an indicate in Sourcegraph that the company is on a trial.
  - `enterprise-plus` or `elite` to indicate that the company is on a product tier above Enterprise (which is the default).
  - And the company's name (with dashes instead of spaces), to make it easy to search for a given license key in the future.
- Set the licensed number of users (note that if you added the `true-up` tag above, the company will be able to exceed this count, but administrators will see a warning) and the number of days that the license should be valid, and click **Generate license**.
- Finally, click on the **View as user** link, and share the resulting URL with the company.

A typical email to send to a company is:

>Hi,
>I just created a new license key for you that you can find at ___! Just click **Reveal license key**, copy the key, and then save it to your Sourcegraph's site configuration in the `licenseKey` field.

## How to delete a license key

Unfortunately, once a license key is created, it cannot be disabled or deleted.

If the company hasn't yet received or seen the license key, it's easy to hide it. Users can only ever see the latest key associated with their subscription. So just re-follow the steps above (from the "Click **Generate new license key manually**" step onwards) and they will never be able to see the previous key.

However, if a company has already accessed and copied the key, there is nothing we can do to change it. As a result, try to minimize the duration and user count on keys to only that which is actually necessary. As an example, if you want to create an "unlimited" license for a company that has 100 employees, don't create a key that allows 999,999,999 to achieve that. This minimizes any risks of the key becoming exposed. Instead, create one that is close to the actual total, as we can always [create a new, larger key](#how-to-create-a-license-key-for-a-renewal-or-upgrade) for them in the future.

## Viewing current license keys

All license keys can be found in a [complete list](https://sourcegraph.looker.com/looks/635) or in the individual [instance views](https://sourcegraph.looker.com/dashboards/94).