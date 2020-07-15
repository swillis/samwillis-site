---
layout: post
title:  "Creating better learning habits"
date:   2020-07-09
number: "01"
company: "Memrise"
year: "2020"
role: "Product Designer"
link-visible: "memrise.com"
link-actual: "https://memrise.com"
team: "Product Manager, iOS Engineer, Android Engineer, Researcher, QA, Product Designer"
---

<div class="case-study--image header"><img src="/assets/img/case-studies/memrise-header.jpg" alt="Android builds ready for testing, including RTL version for Arabic."></div>

## Background

For this project, I was the Senior Product Designer within the Core Team at Memrise. We’re a mobile focused team responsible for the core learning experience, onboarding flows, and application of the business model.

In the beginning of January 2020, we were tasked with improving the retention of our mobile experience.


## Discover

As a language learning app it’s important we help users build a habit around learning. This means getting users to come back to the app regularly, and one of the key metrics we were focusing on was next-day-returning-users (D1 retention). This felt like a good place to start as, in theory, improvements here should cascade down the funnel.

To get a better understanding of why D1 retention was falling, we conducted surveys and user interviews, and reviewed data from previous research efforts. From this work generated a whole database of insights as to why users stopped using Memrise, and a key theme that emerged was a lack of effective and timely prompts for users to come back and learn.


<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_89624307E7F793CC850C5B2F4700A293FF1664ECDE638D6D7789A6E52A17F9DA_1590997767380_airtable.com_tbleU93m20M1Tq7Oa_viwScTYgU83I4ZDIRLaptop+with+HiDPI+screen.png" alt="Our Airtable database of insights"></div>

## Define

We knew that D1 retention was bad, and we knew from our research that users had a need for better learning prompts. So we decided to look at how we might improve our learning reminders feature.

This idea was supported by our understanding of behavioural models like FOGG, and Nir Eyal’s “Hooked”. We also apply the Kano model to roadmap candidates, and believed this to be a basic feature that was, to some degree, expected by our users (a lot of our competitors had similar features in place).

Looking at the existing and previous versions of reminders, we knew that we had a few issues:


- Reminders got sent 7 days a week, at roughly whatever time the user originally signed up.
- Due to some issues in the past, notifications had been turned off, and then not back on for some users, meaning a lot users weren’t getting them at all.
- Users had no control over notification types, meaning if they turned off notifications because they didn’t want t receive alerts for marketing or CRM, then they would be turning off reminders too.
- The primer for requesting notifications (on iOS) used a system alert that didn’t justify why reminders would be useful.

With all that in mind, we defined the following scope for our project:


- Allow users to set what time, and what days of the week, they’d like to be reminded
    - By giving the user autonomy over their learning schedule, we believed we could increase learner motivation (as per self-determination theory)
- Allow users to control what types of notifications they want to receive
    - Users may want to be reminded to learn, but not care for our offers or events.


## Develop

With the project defined and the scope reasonably tight, I set to work generating ideas for how we might create this feature and experience for our users.

I started by identifying the user flows and touchpoints that I needed to design for, and creating them in Whimsical. The feature would initially appear as part of our onboarding flow, allowing new users to set their reminders shortly after sign up. But we also wanted to highlight the feature to existing users (via the home screen), and all users would need a place to go if they wanted to update their notification preferences. Lastly, there was the push notification itself and what that should look like and say.

<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_89624307E7F793CC850C5B2F4700A293FF1664ECDE638D6D7789A6E52A17F9DA_1590942645633_Screenshot+2020-05-31+at+17.30.34.png" alt="Map of our early user journey"></div>


For the onboarding screen where new users set their learning schedule, I started with a series of wireframes, and created clickable prototypes that we could pass round internally and get feedback. We also spent time in our design team critiques going over the functionality and best practices.

<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_89624307E7F793CC850C5B2F4700A293FF1664ECDE638D6D7789A6E52A17F9DA_1590943545777_Screenshot+2020-05-31+at+17.45.32.png" alt="Early concepts for how users could input their learning schedule preferences"></div>


Based on this feedback I honed it down to the standout one or two options, that we then did some quick and dirty usability testing via Maze, just to round off the hard edges.

<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_89624307E7F793CC850C5B2F4700A293FF1664ECDE638D6D7789A6E52A17F9DA_1590943737732_Screenshot+2020-05-31+at+17.48.45.png" alt="Part of a Maze report on our early concepts"></div>


Maze gave us some beautiful looking (if not 100% useful) readouts, and helped me refine the design down further. We were getting close.

Because this feature was to be built on both iOS and Android from the start (sometimes we may test a feature on one platform before the other), I worked closely with engineers for both platforms to choose the right functionality when it came to date and time pickers. Where possible, I wanted to use as much native functionality as possible, to keep it familiar to the user and streamline development time. This was especially true in the notification preferences section, as it lives in a settings view where the majority of elements are from the platform’s design system.

Finally, I piggybacked some usability sessions being run by another team in order to put the final(ish) design in the hands of real users toes how they responded to it.

<video controls>
  <source src="https://www.dropbox.com/s/a9c2c4bh6n7dcsq/learning%20reminders%20demo.mov" type="video/mov">
  Your browser does not support the video tag.
</video>

## Deliver

Despite the reasonably tight scope of the project, we still wanted to reduce the size of the initial release in order to deliver value quickly to our users.

The first version was scoped down to:


- Both platforms
- Notification set up (in onboarding)
- Home screen card (for existing users)
- Settings view (UI for editing reminder schedule)
- Simple, standard reminder notification

We believed most of the value was tied up in allowing users to set their “learning schedule” as it were, so we’d deliver that first and follow up with the notification preference centre later.

<div class="case-study--image"><img src="https://paper-attachments.dropbox.com/s_89624307E7F793CC850C5B2F4700A293FF1664ECDE638D6D7789A6E52A17F9DA_1590945256507_learning+reminders+android.png" alt="Android builds ready for testing, including RTL version for Arabic."></div>



### Results

At time of writing, the learning reminders project is in the final stages of the build so don’t yet have results, but I can talk about our plans for the release.

As with most significant updates, this will be released through an AB test is that we can monitor the impact. We’ll be closely watching the feature’s impact on D1 (and subsequent) retention, and tracking user behaviour throughout the flows. We also have a community forum full of passionate Memrisers, who we’ll also source feedback from.

I hope to follow up with the initial results very soon.


### Future iterations

Assuming there are no major issues with the AB test, we’ll first look to roll this out to all users. After which, we’ll look to follow up with the other milestones (more control over notification types, dynamic push notifications) that we descoped in v1.

Looking further ahead, I’d like to experiment with integrating the learning schedule users set for their reminders with our streaks functionality. A lot of users don’t want to learn every single day, and the most common cause for a streak to end is the weekend. I know from experience that a broken streak can be very demotivating, so allowing more flexibility here could help users maintain streaks, and us improve retention.
