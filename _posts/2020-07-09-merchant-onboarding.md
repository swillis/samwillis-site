---
layout: post
title:  "Designing a B2B onboarding flow"
date:   2020-07-09
number: "03"
company: "GoCardless"
year: "2018"
role: "Product Designer"
link-visible: "gocardless.com"
link-actual: "https://gocardless.com"
team: "2x Engineers, Product Designer"
---

<div class="case-study--image"><img src="/assets/img/case-studies/gocardless-header.jpg" alt="Android builds ready for testing, including RTL version for Arabic."></div>

## Background

GoCardless is a payments company aiming to create a new payments network for the internet. We focus on bank-to-bank transactions to make taking recurring payments super fast and easy for our merchants.

My role at GoCardless as a Product Designer is to take problems presented to me by the product management team and solve them through research, applied UX methodologies and ultimately design & deliver solutions, usually in the form of a UI.

<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494442814350_file.png&hmac=KPiivWklNBztgRSQ8zYzHtg0nYAMwZqZYZZ2lbOWyzg%3D&width=1490" alt="The GoCardless dashboard"></div>


## Discover

Customers can use GoCardless in three ways: integrate with the API, connect via one of our partners, or use us directly via our payments dashboard. We recently decided to de-prioritise the dashboard, as the many small customers using us through that can be served better via our partnered apps. As such, improving the 'partnered merchant' experience has become a core focus for us over the past few months.

Another focus of ours is international expansion. With the previous flow, our partnered merchants had to get verified by logging into a dashboard. We know that internationalising the entire dashboard would be a mammoth undertaking, but if we could take the onboarding/verification process and move it outside of the dashboard it would make it much more manageable.
Moving this flow outside the dashboard into a single purpose, smaller app also opened up the possibility of making it responsive and create a solid UX across more devices.


## Research/ideate

In order to understand the problem further, confirm some of our hypotheses, and uncover the key friction points I went through a number of different UX practices:


### UX review of the current experience

I went through the onboarding process with a bunch of our partnered apps and created a user journey map of the many different touchpoints throughout the process, and started to make a note of the potential friction points.


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494443209432_Connect%2Bto%2BGC%2Bjourney%2Bmap.png&hmac=USTJe6s73Fq6tatApgbJ%2FYyTqN6k7RR%2FF1xmE6PXoKA%3D" alt=""></div>


### Gathered internal knowledge

I conducted a series of interviews with various members of the Operations Team to understand the key problems that they were aware of. As they speak to customers all day every day, this is always an invaluable resource in terms of understanding the most common problems faced by users.


### Looking into data

I logged into Tableau and perused the many workbooks that our partnerships team have created around our partner merchants. I looked at the stats for the current onboarding funnel, and applied this data to the process maps I created earlier int he process.


### User research

I conducted a couple of ethnographic observation sessions with our some merchants who were considering GoCardless but hadn't yet connected it to their app of choice. By working with our inbound sales team, I was able to recruit participants who had called in to discuss connecting GoCardless, but were yet to commit.

I then hopped in a taxi (with a couple of other members of the product team) and went out to meet them and observe them connect GC.

For this project we only did a couple of user research sessions like this. Usually I would aim for at least 5, but in this case the problem was very well defined, and the 2 sessions we did do confirmed our hypotheses so much that we figured our time would be better spent creating designs and prototypes that we could then go out and test.


## Define

By this point we'd identified the following key friction points:

**Merchants weren't aware that they needed to get verified.**
When merchants completed the OAuth sign up page, they were redirected back to the partner app, with no mention of verifications. While they were simultaneously sent an email with info on how to get verified, it was not very clear and merchants were clearly missing this email (also, in some companies the person who created and connected the may not have access to the information required to complete the verification process).

**Sending merchants into the dashboard was confusing**
They don't need 99% of what is in there, they just want to activate their account so they can start taking payments.

Identifying these friction points complimented our initial hypothesis that we should move the verification flow outside the dashboard for partner merchants. We could then create a streamlined, focus flow for verifications that was internationalised and responsive.


## Develop
### Pen & paper and mapping out flows

As usual, I started out by outlining the user journeys with pen and paper, trying to identify the quickest ways we could get a user through the process. We serve many many different types of merchant, so there are always tonnes of edge cases to consider, so at this stage I try not to think too much about UI and just focus on jobs to be done and finding the most efficient system that can process these different flows.


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494443435955_IMG_2642.jpg&hmac=XyzeOBjO7zV3LbXC364DXgoAHUIofcKEhZgoOjk1stI%3D&width=1490" alt="Some pen & paper doodles from the early project stages"></div>


### Wireframes

Once I had the flows kind of nailed I started to create wireframes for each screen. This starts out with pen and paper but might eventually move into some lo-fi sketch files.


### Design in Sketch

I created a UI kit at GC shortly after joining, which means it's pretty quick and easy to start mocking up screens on the fly.

That being said, I wasn't completely tied to the visual style of the dashboard for this flow. Although it had to be consistent with the GC brand, I had a certain amount of freedom with how this could look. I opted to go for something very clean and white and not too opinionated. This is meant that with the addition of the partner logo on some screens the user would feel like they were still in vaguely familiar territory, rather than being plunged into a completely alien app. It also left space for white-label solutions in the future.

At this point I had a series of reviews with the product management, engineering and design teams to make sure everyone was aligned. I believe in sharing my work early and often, so by this point most of them would have seen bits of this work in the previous stages, but this is the stage where I would start booking in some slightly more formal sets of reviews.


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494443633265_file.png&hmac=Y%2FdgxDGV9sC%2FM4IqKI8anwU8GpKht4QwZxeqHL3aohg%3D&width=735" alt="Some very early screens"></div>

<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494443708659_Screen%2BShot%2B2017-05-10%2Bat%2B20.14.49.png&hmac=SKiskgrElj79R256VYl2lIHhYQvDFNF8U8gvkgaPkAo%3D&width=735" alt="Some later screens. There were a lot!"></div>


### Prototype in InVision

Once I had a pretty good idea of what each screen will look like and how they would interact with one another, I create an Invision project. This gives stakeholders a relatively hi fidelity prototype that they can click through and get a feel for the user experience of the new flow.

This is also something that I would start to share with the operations teams (as stakeholders likely to be greatly impacted by this project) and the marketing teams (to make sure we are aligned in terms of copy and how we display our pricing packages).

I also ran some usability tests with the prototype. Although ideally these would have been with users external to GC, because of time constraints I had to be a little creative, and opted to use some of the new interns across the company, who hadn't yet been corrupted by the world of Direct Debit, to go through the flow. I recorded these sessions and shared the results with the rest of the product team.


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494443708659_Screen%2BShot%2B2017-05-10%2Bat%2B20.14.49.png&hmac=SKiskgrElj79R256VYl2lIHhYQvDFNF8U8gvkgaPkAo%3D&width=735" alt="Putting together the prototype in InVision"></div>

### Rounding up the design phase

After a few rounds of review with the various different stakeholders, I got to a point where the design was no longer likely to change too much, other than maybe some copy tweaks here and there, and we were ready to assemble a small team to start the implementation.


## Deliver

The development team for this project consisted of 2 front-end devs, 1 back-end dev and myself. Although I am not a super experienced front-end engineer, I know my way around a React app and was able to help out here and there with the build and perform regular design reviews and tweaks as we built this flow over the course of about 3 weeks (and a couple of very late nights thrown in for good measure).


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_8C0C5E444A031F8EF840751AE4811396C1269B0EF30B54EA4E27A346132EAEC1_1494444045286_file.png&hmac=ZDKJoXspR2gqYHr7G1Y4sRkr7%2F6Jhe2rRWAcChUD5Lw%3D&width=1490" alt="A screen from the live flow"></div>


### Test/iterate

We started by rolling this out to a small percentage of new merchant in the UK, and tracked its performance through a combination of Segment and Mixpanel. This meant we could catch any bugs or issues early, without breaking too much stuff.

We also added FullStory to the flow, which allowed us to playback user sessions and see how they interacted with the feature. This allowed us to spot some minor UX issues and fix them insanely quickly. We probably made 5 minor changes in the first week based off this data.

With no major issues, and conversion outperforming the previous flow, we started to roll this out to more merchants.

As of today, this is still the experience that all new merchants get when signing up to GoCardless.
