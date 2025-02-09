---
title: Trusted data access and transfer, in many contexts
tags: trust
author: Lisa Dusseault
excerpt: Our focus is on data portability between cloud-based services, which has technical differences from other kinds of access. Consistency is valuable.
thumbnail: /images/blog/electronics.jpg
---

At DTI, our focus is on data portability, but it’s even more specific than that: DTI was launched out of an open source collaboration, the *Data Transfer Project (DTP)*, that service providers run to allow them to host user-initiated personal data transfers with other DTP participants over the Internet.

Because of this origin story, we’ve focused mostly on how data sharing works in the cloud. But we also think that how data sharing works on devices is both instructive and is part of a system that should be considered holistically. To be able to deliver on our mission, it’s critical for us to understand the context in which it operates. That’s perhaps most visible when we work on [public policy](https://dtinit.org/blog/2024/10/08/global-policy-round-up), but it’s true in all our efforts. For example, we looked at other kinds of registries when beginning to develop [our own trust work](https://dtinit.org/blog/2024/07/30/trust-work-updates).

This article considers how DTI’s focus, cloud-based portability, relates to device-based portability - focusing on technologies for access and authentication, and on the nature and mechanisms of trust.

## In the Cloud

The technology context for accessing personal data in the cloud is mostly HTTP-based:

* Data requests are almost always HTTP requests.
* Authenticating the user happens with a login Web page.
* Ideally, any time sensitive personal data is involved and login happens by username/password, the password page is followed by a two-factor verification or one-time password confirmation (again sent via HTTP requests)
* Every single HTTP data request by the user after login needs to be securely associated with a session, through a session token that links to the user, because HTTP is technically a “stateless” protocol. 
* Data access requests from other parties also happen over stateless HTTP. It’s challenging to associate one session key with another session’s authorization choices in a stateless protocol that does nothing to link these individual HTTP requests.

Cloud services don’t always offer the ability to share personal data with 3rd parties. Sometimes when users really want to share data between services, they share their service password (and sometimes even a one-time-password configuration!) with a 3rd party. Now the 3rd party is authorized as the user, using a session token that isn’t really distinguishable from one of the user’s normal session tokens that keep them logged in. Because the 3rd party is not distinguishable from the real user in any reliable way, we don’t consider this data access - it is really *identity access*, and leaves the user open to many possible abuses.

When there are systems in place to allow 3rd-party access *authorized by* the user but not *authenticating as* the user, this is occasionally solved with [OAuth](https://oauth.net/2/) but often solved by the service using a non-standard process (including, for example, a developer program with statically issued API keys, and configuration/settings data to know if each user authorized the 3rd party). Solutions for consent UX and consent management are not widely standardized, interoperable or reusable.

## On the Device

Modern device platforms went through an early, fast and comprehensive process of designing data access Application Programming Interfaces (APIs) in order to enable many exciting applications to be installed and make the devices more useful. Personal data access is much more ubiquitous and consistent on devices, as compared to the diverse access offerings of independent online services (some very small) which hold personal data.

The most commonly used APIs today are the Swift and Objective-C APIs on iOS, and the [Android Platform APIs](https://developer.android.com/reference/) on Android devices. Data requests through these APIs are always local to the device: there needs to be an installed app on the device to request the data from the OS on the device. Thus: 

* The user unlocks their device using a passcode, facial recognition or fingerprint. Once the device is unlocked, almost all choices are considered authorized. Some sensitive operations might prompt another identity check, returning to the unlocked state.
* While the phone is unlocked, application data requests happen inside the user’s “session.” There’s no need to re-login the user.
* Data access requests to the platform API either come from apps that were developed by the platform company, or from apps which the user decided to install - another mark of trust.
* For security, apps are prevented from full access to all the data held by the device through sandboxing - limiting access to only data types or collections that have been granted.
* When a data request is made from an application through the API to the part of the OS holding data, it’s good modern practice to prompt the user for consent. Many data access requests are made while the user is actively interacting with the app, and the user can consent or deny immediately when a popup asks them to.
* Consent can later be reviewed and revoked by the user.

None of these device-context data access requests involve HTTP or OAuth. So among other distinctions, authentication, authorization and revocation solutions all must be completely different technology compared to cloud solutions.

## Consistency of Trust Criteria

Both device and cloud environments limit nearly all platform-mediated user-requested transfer of personal data to 3rd parties that the platform has “verified” or given an API key to. Such limitations can be an important part of protecting users from legitimate-seeming data requests that aren’t really legitimate, or of protecting the cloud platform from Denial-of-Service attacks and other Internet abuses (or both reasons, or more reasons). Whatever the reason for establishing these verification or access programs, the result is that only approved 3rd parties get meaningful access.

These are all *Trust Lists*, and they all involve *Trust Criteria*,** **even if different companies use different terms such as telling 3rd parties to apply to a “developer program” or “add-on marketplace.” Although they may serve several purposes, including explicitly limiting some uses of data received via the APIs, one avowed purpose is to protect the user from granting access to a 3rd party that is likely to put personal data at risk.

In part because of the conflicting needs being served by these lists, some of these trust lists are run in very arbitrary ways. In 2023, both [Twitter](https://techcrunch.com/2023/03/29/twitter-announces-new-api-with-only-free-basic-and-enterprise-levels/) (now X) and [Reddit](https://techcrunch.com/2023/07/04/reddit-braces-for-life-after-api-changes/) drastically cut back on API access. In both cases, they at least initially cut off apps used to help individuals with accessibility needs, to moderate harmful content, and to do public-interest research.

Platforms with broad functionality may evaluate the same 3rd party in different ways internally. The same startup with an app in a mobile app marketplace may also apply for access to the same company’s cloud data APIs. Should we expect a 3rd party to be approved across the board, or must they apply in each context? How should trust renewal in the cloud impact consent given on devices?

As an example of a poor outcome due to inconsistency: a startup gets their app approved for installation on my device, and I choose to install it and consent to data access. The same startup applies for cloud data API access (to the same large platform OR to another platform I’ve synched the same data to), in a process that requires them to provide their updated SOC2 report annually. One day, that startup gets bought by another company and stops providing their SOC2 report. Without a holistic view of the system, that startup is likely to continue getting my data via the app I installed on my phone, even as their access to cloud data is cut off.

It’s not a fun system from the perspective of the startup, either. A startup can work hard on its business plan and software, but still have severe “unknowns” in getting approval for data access. The risk and effort required increase with the number of inconsistent trust lists and trust criteria, making the startup have to painfully choose which things to cut from their plan.

Managing our privacy and data access authorizations can only work smoothly if we are able to apply consistent choices.

* If I trust a “FamilyShare” service with my photos on the device, I should be able to consent to their access to the same data in the cloud.
* If my consent for “FamilyShare” access expires in 6 months in the cloud or I’m prompted to renew, the same expiration should be the default on my device.
* If “FamilyShare” loses its trusted status due to violation of its own terms or repeated data breaches, that organization should lose trust and access on devices as well as in the cloud.

## Summary

Sharing best-practices between device and cloud environments makes sense even when they’re completely independent. UX researchers who look at both environments can spread those best practices. However, to maximally benefit the user’s experience, we need to go further than just best practices and look at consistency.

People don’t divide up their technology use into the clean boxes that programmers and protocol designers might prefer to have. Consent and trust are issues that cut across the technology silos, as they must.
