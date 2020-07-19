---
layout: post
title:  "Reducing friction, online and offline"
date:   2020-07-09
number: "02"
company: "Fat Llama"
year: "2019"
role: "Product Designer"
link-visible: "fatllama.com"
link-actual: "https://fatllama.com"
team: "Growth Analyst, Engineer, Product Designer"
---

<div class="case-study--image header"><img src="/assets/img/case-studies/fatllama-header.jpg" alt="Android builds ready for testing, including RTL version for Arabic."></div>

## Background

Fat Llama is a peer-to-peer rental marketplace, comprised of borrowers (those looking for stuff), and lenders (those lending stuff).

I joined as the first full-time Designer in 2018, shortly after they raised a Series A round of around $12.5m.


### The lender team

At the end of Q4, 2018 we were falling short of growth targets, with the effects of seasonality being felt across the business. Emotions were high as our only Product Manager was let go, and the decision was made to split up our product development team into smaller, cross-functional teams.

This was when the lender team formed, and was made responsible for the lending experience across the platform.


<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_6AAF71ED2E443C6D027232B443F80D7F5D9C442D719D16A8C24676865076C5C7_1590998426546_lender+mission.png" alt="Graphic I made to represent the lender team’s mission statement"></div>


### OKRs

The first thing we did in our new cross-functional teams was to set OKRs. As stand-in Product Manager for the Lender team, I was responsible for deciding what these should be.

The organisation OKRs were set simply as:


- Increase conversion
- Increase repeat rentals

And using some great research done by our customer service team (who spoke to 30+ lenders about their issues with the product), we set the following OKRs for our team:


- Reduce messages per rental
- Reduce customer service contacts

The focus for this case study is the former.


## Discovery

From that initial research piece, it was clear lenders were receiving a disproportionate amount of messages per rental. This may not have been a large issue for lower volume lenders, but the majority of Fat Llama’s rentals went through a small number of “Super Lenders”, upon which the platform depended on.

Through analysis of the messages it became clear that they were typically about the same topics, over and over again:


1. Is the item available?
2. When & where can I pick up?
3. When & where can I drop off?
4. How does Fat Llama work?
5. How do I use the item?

It felt clear to us that this was a failing of the product, and that we should be facilitating these queries, taking it off the lender’s plate.


### Interviews

To get a deeper understanding of the problem, we interviewed a handful of our Super Lenders, who confirmed their frustrations around being inundated with messages, and often having to repeat the same information.

These frustrations meant that even the most committed lenders would sometimes ignore messages, leading to poor response times and a poor experience for lots of borrowers.


### Dead listings

Our calculation for messages per rental was fairly rudimental (total messages / total rentals), and from looking at the data it was clear that another big contributor to this metric were messages about dead listings.

These could occur for a few of reasons:


- Item is no longer available (broken, sold, etc.)
- Lender isn’t paying attention to notifications from Fat Llama
- Lender isn’t using Fat Llama anymore


## Define

To figure out how we might solve the messages issue for lenders, we had a little look at how other two-sided marketplaces, such as Airbnb and eBay, handled it. A common solution was for the platform to “intercept” the users message to the lender with a UI that tried to answer questions via FAQs.

Whereas our item pages and been designed to make messaging seamless, placing a “message lender” text box front and centre.

We figured a solution like this could go a long way to reducing questions around how Fat Llama works, and allowing the lender to add their own FAQs could help with questions around the item.

As for whether the item is available, we had a calendar UI on the item page that showed availability, but it seemed users weren’t using this, preferring to message lenders about availability instead.

We’d need the page to push the calendar on our new page too.


### Two-pronged approach

For the dead listings problem, we figured we could set up a simple system for “pruning” them. This would involve emailing potentially inactive lenders, before deactivating the listing on the site. We could start with a large purge, and then check on a regular basis to keep the problem in check.

This would dramatically lower messages per rental straight off the bat, and would also lead to a better experience for a large number of potential borrowers.

As for lender frustrations around being inundated with the same message topics, we wanted to try creating a “message lender” page. This would add an extra step to users wanting to enquire about a product, but would also feature FAQs to try to answer questions on the lender’s behalf. Lender’s also resonated with the idea of being able to add their own FAQs to this page, though we quite quickly agreed this would likely be out of scope for v1.

The scope for the project ended up looking like the following:


- Replace “message lender” input with a button linking to our new page
- Create message lender page, complete with FAQs
- Include availability calendar on the page
- Include the ability to write a custom message
- Web only (for ease and speed, but also where the majority of traffic was at this point)



## Develop

In order to test this idea quickly, we wanted to go with a simple solution that we could build in days rather than weeks. We had a good initial list of questions which could be hardcoded initially. And we could lift the calendar component from the item page and relatively easily.


### Ideation

After white boarding some ideas together, we settled on the following design decisions:


- Two column layout
    - Main column
        - FAQs & message box
            - Availability is the first option
                - Tells user to check availability in the calendar opposite
            - Message box is always available
                - This was a trade off — another option was to hide it behind a final “can’t find what you’re looking for” question. But we felt this might add too much friction (though we were keen to test this later)
    - Second column:
        - Calendar and checkout button
            - Teach borrowers to check availability this way, and also allow them to start check out process from this page.


### Prototyping

We then whipped up a simple Sketch prototype that we could take to some of the Super Lenders we had met with previously. Their feedback was largely positive, with the request to add their own questions coming up a couple of times.


<div class="case-study--image"><img src="assets/img/case-studies/messages.gif" alt=""></div>


### Dead listings

Our growth analyst wrote a script to identify dead listings (where a lender had not replied to a message for more a certain period of time). And we sent an email to these lenders informing them we had detected inactivity, and deactivated their listing temporarily. We gave the reason that it was to protect their lender rating, and improve the quality of service for borrowers. We also added a button that they could press to immediately reactivate their item if they felt this email was sent in error.


## Deliver

As I mentioned, we had a very strong React Engineer on the team who was able to get working on some of these parts in parallel to me finishing the designs. As I started out my life as a (very junior) web dev, I was able to help in parts to get the project live as quickly as possible.

We decided, perhaps hastily, not to phase the rollout but to release 100% straight away. In hindsight I think it may have been better to AB test or phase the rollout, but we were moving pretty fast and I think we were excited to see results.


<div class="case-study--image"><img src="https://paper.dropbox.com/ep/redirect/image?url=https%3A%2F%2Fpaper-attachments.dropbox.com%2Fs_6AAF71ED2E443C6D027232B443F80D7F5D9C442D719D16A8C24676865076C5C7_1590947560885_message%2Blender%2Bscreen.jpg&hmac=PQznAQ6qSXmMw4g93HWPsdXyNuB3P1IMOpkokzLWevg%3D" alt="Live message lender screen"></div>

### Analysis

The work around dead listings worked as expected, and we saw a significant drop in messages per rental as a product of this.

However what happened with the message lender page was more interesting. We had installed FullStory (a means of playing back user sessions) and we monitored user behaviour for the following days after release.

It’s worth noting that we were able to make a series of minor iterations within 24 hours of release, thanks to the FullStory recordings.

What FS revealed was that, while some borrowers did read the questions, the users that were enquiring about availability still did so via the message box at the bottom of the page.

From speaking with borrowers we learnt that this was due to a mix of distrust around how the calendar worked, but also because they were so used to dealing with dead listings. For example, a common behaviour was to message 3 or 4 lenders when looking to borrow an item, and rent from whoever responded first.


### Follow up projects

Because the message lender page was providing value to users not worried about availability, we kept the page in place.

However we knew we still had work on our hands to reduce messages per rental, and improve the experience for borrowers and lenders alike. As such the following projects were started:

**Super Lender Program**
An initiative around rewarding lenders who displayed favourable characteristics, such as response time or customer experience.

**Improve lender tooling**
Improve lenders ability to manage their items and show availability (such as setting “operating hours”)

**Build in times and location**
At the time of writing, rentals work kind of like booking a hotel. You select a start date and a an end date. By adding the ability to set pick up/drop off times and locations, we can have a better picture of what items are where, and use this information to provide a better experience for borrowers and lenders.
