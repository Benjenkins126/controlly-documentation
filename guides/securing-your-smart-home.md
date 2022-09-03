# Securing Your Smart Home

Having a smart home is great, however if done incorrectly it can cause huge problems. Let's use an example.

Imaging that you have your home CCTV cameras, front-door lock and home alarm linked to your smart home. If an intruder can access your smart home installation they can let themself into your home, disable your alarm, steal valuables and then delete the CCTV footage as if it never happened. Now imaging having to explain that one to the police 👀

The above example is exactly why securing your installation is important, especially if you allow external access to your home. Unfortunately many providers overlook this problem, or do not invest enough time and attention into the issue. This is an advanced guide to ensuring that your Controlly home remains safe and secure.

## Externally Accessible Smart Home

Externally accessible smart homes are specifically vulnerable to attacks, and that's why you should take it seriously. Below are some steps you can do to make your home more safe.

### DEFCON 1

One of our favourite Controlly features is a security setting called DEFCON 1. With the term Derived from the US Defence Ready Condition, it definitely lives up to its name.

When enabling DEFCON 1 a bunch of security features will be enabled on your site to defend against, catch and defeat attacks targeting your home. Whilst not all the security features are public, below you can find some of the main defences used to protect your home.

* Any wrong password attempts to access Controlly will alert Administrators
* Controlly will monitor IP access patterns. If it sees a pattern in access attempts it will block the IP from accessing the site until an Administrator unblocks the IP Address.
* If there are many failed login requests from different IPs, the system may decide to temporarily lockdown the system to prevent further attack attempts.
* In extreme cases you can limit external access to specific mobile carrier networks (Note: this feature is not always accurate and relies on Geo IP to discover carriers).
* You can restrict IP Address' that can access your home.&#x20;

