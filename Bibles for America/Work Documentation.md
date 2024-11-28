# Work Documentation

### 6/22/21 T
- Did some research on customer.io to see how it could best be used for the saints to implement
	- Resources
		- https://www.convinceandconvert.com/email/the-12-key-messaging-strategies-for-email-marketing/
		- https://www.youtube.com/watch?v=i_zeYeGt_Xk&ab_channel=customerio
		- https://www.youtube.com/watch?v=B1NIDnCRNbw
	- Takeaways
		- Lifecycle messaging (particularly for email marketing) is to avoid the problems that come with the "one message fits all" approach that can lead to lots of churn (the rate at which people stop doing business) and lack of growth
		- We want to be able to reach people at their particular level/situation/need so that they could be facilitated through the marketing funnel (Acquisition, Activation, Retention, Referral, Revenue) -> so that people will be attracted and kept and led to take various actions
		- Customer.io is the potential replacement for Mailchimp (which is what BfA currently uses for their email marketing campaigns)


### 6/23/21 W
- More research on why email marketing (done properly) is super critical (https://www.youtube.com/watch?v=P4LzwX31Egg&ab_channel=HubSpot)
	- How to maximize ROI for email marketing campaigns -> three important principles
		- The significance of segmentation
			- Segmentation is simply delivering the right message to the right person at the right time
			- Combining two inbound concepts together -> the buyer persona and the buyer's journey -> who is the person you're reaching and where are they at on the buyer's journey?
				- Buyer's journey is the active research process someone goes through in leading up to a purchase -> three stages of awareness, consider, and decision (simplification of marketing funnel)
		- The power of personalization
			- Personalization is when you use subscriber data to make your messages more intimate (contextualized and individualized experience)
			- Behavioral email -> the practice of sending automated, targeted emails to your contacts based on their history with your company
		- The impact of data-driven analysis	
			- Analysis helps you evolve with your users
			- Data-driven analysis framework:
				- Track the metrics that matter
				- Learn what those metrics indicate about success of your emails
				- Apply what you have learned to optimize and improve each email that you send
	- Why email marketing is still important and one of the best channels for digital marketing (https://www.lonefircreative.com/blog/why-email-marketing-is-still-important-for-2021#:~:text=More%20importantly%2C%20email%20marketing%20allows,your%20most%20impactful%20marketing%20channels.)
	- What are the top email marketing platforms? (https://blog.hubstaff.com/changing-email-marketing-platforms/)
		- Convertkit (not good for SaaS or anything remotely technical but is mostly for bloggers and non-technical creators)
		- Intercom
		- Customer.io (very good for creating highly targeted segments based on user behavior but isn't built with content marketing in mind)
		- Active Campaign
		- Drip
- Actually playing around with customer.io and studying the docs
	- Your System and Customer.io system
	- Customer activity in the form of attributes, events, page views, and devices
	- People data used to populate Segments and to build Campaigns and Broadcasts
	- Segments (data-driven and manual)
	- Campaigns, Broadcasts, and Transactional Emails
		- Campaigns are ideal for dripping content to individual People as they become eligible to receive it
			- password reset emails
			- payment receipts
			- welcome messages
			- re-engagement series
			- abandoned cart notices
		- Broadcasts are for announcements and bulk sending of messages (manually sending newsletters)
			- traditional, newsletter-style messages
			- pre-scheduled announcements
			- periodic release notes
			- community alerts
			- event change notifications
		- Transactional emails are for responding directly to audience's actions within app
			- Purchase receipts
			- Registration confirmations
			- Password resets
			- Event reminders
			- Shipping updates
- Got the 14-day free trial for customer.io to play around with it -> John set up a different account
- Received some templates for the various emails we can send to different segments from John Peng
- Had call with John Peng 3pm
	- Questions:
		- Where is the data stored?
			- Bible orders are stored on separate database -> multiple databases
		- How is 500 life studies related to bfa?
			- 500 life studies is a separate project (led by brother Minoru) -> we'll be using customer.io to test on this site and then consider how we can use it for bfa.org
- Credential info for customer.io account:
	- Microsoft 365 email: jere@500lifestudies.org
	- Hop37901
	- customer.io password: biblesforamerica
- Staging site for 500 life studies: https://lifestudies500.wpengine.com/
- Established daily time to update on progress with John at 9am EST
		
		
		
## 6/24/21 R
- Call in the morning with John to go over more things in customer.io 
	- We're going to try to finish the basic functionality of the email actions and triggers (campaigns) by next week (there will be a meeting with brother Minoru next Thursday 7/1)
- Studying up on liquid templating (the template language for writing dynamic content -> especially for emails that can be programmatically and dynamically written)
	- https://customer.io/docs/using-liquid/
	- Generally three types of variables to use for personalizing messages for audience: attributes, event properties, and trigger properties
	- attributes use the `customer` scope - `{{customer.<attribute_name>}}`
	- event properties from the `data` object in an event that triggers a campaign use the `event` scope - `{{event.<data.property>}}`
	- trigger properties from the `data` object in a transactional message or API-triggered broadcast use the `trigger`scope - `{{trigger.<data.property>}}`
	- You can reference attributes in any message but you can only use event properties in a campaign that uses a trigger event and trigger properties in an API-triggered broadcast or transactional message
- Gained more clarity regarding the actual goal (and subsequently, the process) for this project
	- Fully leveraging customer.io and its programmatic/dynamic email marketing capabilities to help all of the saints who interact with and sign up for the 500 life-studies site program -> also to leverage customer.io to maximize ROI for BfA (although ROI is not profit but the increase of Christ in all the saints)
- More research on how REST APIs work -> especially in context of the api endpoints for customer.io to pull data from 500 life-studies site
- Compiling all of the potential email messages and campaigns to create
	- Basic:
		- sign up email (after user signs up for email updates)
		- signed up for book (encourage people to track)
	- Extra:
		- those who are inactive for a while (didn't sign up for book after signing up for emails)
		- Those who didn't track for a while 
		- potentially grouping people who are on the same book progress
- Found some resources (YouTube videos on customer.io tutorials) for getting inspiration on how to actually carry out the email campaigns on customer.io
- Planned out tasks for Friday and Saturday morning
	- Actually setting up the basic campaigns (pipelines and messages) and testing them out with John
	- Planning out further campaigns that could be made 



## 6/25/21 F
- **Task: Actually set up the basic campaigns (pipelines and messages) and test them out with John**
- Email message workflows to create:
	- Basic email campaigns:
		- Sign up email (after user signs up for email updates)
		- Book sign up email 
		- Those who are inactive
		- Those who didn't track
	- Advanced:
		- Grouping similar people (book progress)
	- Transactional:
		- password resets
- Testing out the sign up email 
	- We still need to further develop the People attributes, the Segments, and the Campaigns
	- There is an automatic confirmation email after signing up on 500 Life-studies (seems to be directly from Wordpress)
- Had call with John Peng
	- Asked to have access to the backend of the Wordpress site (admin account) so I can actually see the api calls and the data that's being sent to customer.io
	- Clarified the attributes, segments, and campaign info 
		- Important attribute that must be sent is the `created_at` attribute that shows whether or not people actually signed up for the reading program so that there can be the initial sign-up campaign



## 6/28/21 M
- Started 1:30 and stopped 5:30pm and 7-9pm
- Orientation meeting with Ileana Pagan and Iris Cheung 
- Found a good email testing tool -> ~~SendGrid~~ -> switched to Emailfake
- Assignment:
	- figure out making a dashboard to track statistics for people
- Had call with John at 3pm
- Finished up making the campaigns (only the basic ones)
	- Basic campaigns regarding email sign-ups
	- Custom campaign for updating attributes everytime someone updates their progress for LS reading
		- Struggled in trying to figure out why the trigger didn't change anything
		- The issue is not the trigger itself but the action of the "attribute update" -> the event data is able to be used but the action itself just isn't working

## 6/29/21 T
- Had call with John Peng 9am and updated on the issue of the attribute change problem
- New tasks:
	- Contact customer.io regarding potential bug of attribute change
	- Prettify the emails
	- Research how to calculate the aggregate stats of the progress of the saints -> make a dashboard?
	- Research using SMS to remind the saints (Twilio)
	- Research using SMTP to send emails on Microsoft 365 instead of Customer.io itself
- From 9:30-12:30 I worked on:
	- contacting customer.io regarding the change attribute issue
	- researching sms reminders with Twilio (https://customer.io/docs/twilio/#compose-your-twilio-sms)
		- Twilio helps to bridge the gap between web-based applications and telephones
		- It's not easy to build custom functionality on top of the connection that we have (cell phone or home internet connection)
		- The Internet doesn't have nearly the same complexities found in the telephony network but there is a huge barrier in that the internet was not connected to the telephony network -> so Twilio bridges the worlds of internet and telephony using dedicated connections to the carriers
		- A Twilio phone number provides a virtual presence on the physical telephony network
	- researching SMTP 
		- SMTP stands for "simple mail transfer protocol"
			- E-mail clients use SMTP to send a message to the mail server, and the mail server uses SMTP to relay that message to the correct receiving server
- Customer.io got back to me regarding the attribute change issue
- From 1:30-4pm I worked on:
	- Researching calculating aggregate statistics and having a dashboard
		- So far it seems that the capabilities of customer.io itself for data tracking and analytics is good enough
		- There is the potential for using a data warehouse (if there is the need to scale much higher) -> https://customer.io/blog/customerio-email-data-segment-sources/
	- Did some research on webhooks (there is a lot of learning I need to do regarding the world of the web -> like HTTP and its methods, client/server, APIs, webhooks, browsers)
	- Research on creating a progress bar in the emails
		- https://stackoverflow.com/questions/57167122/creating-a-progress-bar-for-an-email
		- https://stackoverflow.com/questions/31072134/progress-bar-email
		- Found that the main issue is that most email clients/servers don't support the latest html5 elements (like \<progress>) -> either need to code from scratch or just hope that they'll update eventually 


## 6/30/21 W
- Tasks for today:
	- Do more research into progress bar issue (because html5 is not universally supported on email servers)
	- Plan further actions for when the attribute change issue is resolved (what campaigns can you immediately work on?)
- Progress bar
	- Got the html and css to work to show up on email (had to use inline styles instead of tags because style tags are not supported in all email servers)
	- Need to work on having the progress level be programmatically changed based on the attributes (and this is directly related to the change attribute issue) (might not be possible)
- Planned out potential further actions once the attribute change issue is resolved and found some potential issues
	- Further actions:
		- attribute for calculating total messages read (sum from previous total plus number read) -> can be used for congratulations emails and calculating progress
		- can have attribute with list of all books read and all messages read (ever expanding)
		- current_book attribute
	- Potential issues:
		- get rid of the initial wordpress sign-up email 
		- people can de-select their reading progress (accidental loophole?)
		- what if someone is reading multiple books? (how would we do current_book attribute?)
- Had call with John and Iris 12pm to update on things (getting overall burden and general timeline) 

## 7/1/21 R
- Had call with John Peng 9am and we went over some things and we figured out how to use liquid to dynamically edit the CSS for the progress bar component
- Tasks for today:
	- Progress bar component and emails that showcase the goals of 50, 100, 200, etc. and show total number of messages read
	- SMS functionality
- Progress bar component
	- Took a while to figure out how to use the liquid tags (the math stuff) -> learned from John that it's actually quite easy to just inject liquid into the css -> this makes things a lot easier
	- Took a while to debug the issue, but used a simple hack to get the numbers (which were integers and defaulted to 0 instead of a percentage) we want (multiplied by 1.00000001 to get a floating point instead of integer)
	- Set up functionality for showcasing updating goals (50, 100, 200, etc.) 
- SMS functionality
	- Testing out sending sms messages to my number in response to the update_progress event
	- Found that all of the numbers that are inputted by users should be in E.164 format
	- The SMS functionality works like a charm!
- Prettified the basic email campaigns 
	- There are three options for the email formatting and templating on customer.io
		- Drag-on-drop -> very easy but very limited in functionality
		- Rich text
		- Code (rich text and code can be switched back and forth)

## 7/12/21 M
- On July 8 (last Thursday), Caitlin Boatright (the contact person for customer.io) got back to me and John regarding the attribute update issue and it turns out that there was indeed a bug that the engineers needed to look at and get fixed
- "Hi John + Jere,  
  Great news! Our engineers were able to push out a fix for this issue. It looks like our attribute update action was misconfigured and wasn't able to process any attribute updates for customers using email address as ID. This was an oversight in our initial implementation of our new multiple identifier workspaces feature, and the bug has now been fixed. We've manually re-triggered the impacted customers in your account to continue in your campaign.  
  
  Thanks again for your patience while we investigated this. Please let me know if you see anything while continuing to test out this action or if you have any additional questions."
  
 - Tasks for today:
	 - Fixing the attribute update issue and using the attribute update action to actually change the people attributes and use those updated attributes to make new segments and campaigns (current book and progress in current book)
	 - Clean up the emails (prettify) and make functionality smooth
	 - Segments:
		 - feel like there's no need to have a segment for those who "haven't signed up for book" because that is already included in the segment that haven't started tracking -> probably should remove that segment and only have segment for those who haven't tracked in book (either ever or for a period of time)
		 - Getting rid of campaign for reminder to sign up for book and only having campaign for reminder to start tracking books
 - Took some time to get a general overview of the world of web development (understanding basic concepts regarding the web so that I can advance in growth engineering)
	 - https://www.youtube.com/watch?v=i0nxESR9sFs&ab_channel=StartCon
	 - https://levelup.gitconnected.com/what-does-a-growth-engineer-do-8ee5445d4d87
	 - https://www.growthdrivendesign.com/
	 - https://snipcart.com/blog/jamstack 	
	 - https://developer.mozilla.org/en-US/docs/Learn
	 - https://www.ycombinator.com/library/59-how-to-set-up-hire-and-scale-a-growth-strategy-and-team
	 - Web Demystified
 - Called John Peng 11:40am
 - Staff prayer 12:30
 - More studying up on overview of the web and web development
 - Worked on putting status bars on all the 500 life studies emails
	 - Discovered the wonderful functionality of having Layouts -> you can put all of the fancy code into the layouts and made it all look pretty good
	 - I'll need to fix up all of the emails to look good this way 


## 7/13/21 T
- Tasks to work on:
	- Morning
		- Creating universal layout for the 500 life-studies emails and putting the progress bar in every email
		- Setup a drip campaign for putting in testimonies of the saints (A/B testing?)
	- Afternoon
		- Do research into implementing the email marketing campaigns on BfA
- Discovered the common dilemma when it comes to email marketing (writing html emails and putting in CSS) -> found some awesome tools that automatically convert html emails into emails with inline CSS so it can be rendered in any email client
	- HTML email
	- CSS inliner
- Call with John Peng 10am
- Tried to find some more good tools that help to automatically make all emails responsive and functional in all email servers and browsers
- Found MJML (great framework for writing responsive emails) and used it to make a pretty effective responsive email template for the layout for the 500 lifestudies emails -> need to set up a better workflow and system for writing html emails (downloading MJML and integrating with Atom) and I need to include this toolstack and group of resources for future reference for when I have to work in email marketing
- Setup MJML and integrated with Atom and documented my learnings regarding all of these important tools and principles for email marketing 
- Worked on simple drip campaign functionality (learned that there is such a thing as behavioral drip campaigns which sound really cool) for the testimonies drip campaign
- Setup simple layout plan for email campaigns (using mjml to quickly edit the layout to look nice)
- Tried figuring out customer.io collections to set up the Goals object/array instead of having the hard-coded numbers for the progress bar logic


## 7/14/21 W
- Did some research on cool resources for email marketing and digital marketing campaigns in general
- Tasks for today:
	- Morning
		- ~~Put the same layout for every email in 500 life-studies (you can receive feedback on the layout from the design team)~~
		- ~~Do research on implementing the email marketing campaigns on BfA~~
	- Afternoon
- Call with John and Iris 1pm
	- John told me it is best to keep the layout editing of the emails to drag-and-drop for the sake of the design team (don't put in so much crazy coding stuff)
	- If I ever run a business and hire people I would want them to have some level of front-end design and development or at least the willingness to learn how to code at a basic level
- Adjusted the emails to make them simple drag-and-drop

## 7/15/21 R 
- Tasks:
	- Research on using JAMstack framework for BfA instead of wordpress (deliverable)
	- Compile everything related to using marketing automation (customer.io) for BfA (presenting to the staff to present the idea)
- Did some research on potentially using the JAMstack framework for BfA 
- Called John Peng 10am
- Created "reminder to log in campaign" 
	- Trigger is simply that someone has signed up -> with filters of not logging in recently
	- Created new segment "have not logged in recently" (within last 3 days)
- Created campaign for updating/creating "login" attribute
- Created "reminder to sign up for prize" campaign
- Setup automating the Goals collection so that the displayed message for current_goal would be programmatic and not hard-coded directly into the message text (allows for adding of more values to the Goals collection)
	- Encountered very strange yet seemingly elementary bug regarding logical operator not working
	- Sent email to John regarding this strange issue and moved on to other tasks
- Did more research on JAMstack
- Talked to John over the phone 3pm and he gave me a good idea to deal with the goals situation
	- Instead of trying to bring in an outside variable, just have the "current_goal" be an attribute that just changes when users reach a certain threshold (send congratulation message everytime the goal is reached) 


## 7/16/21 F 
- Finished up the current_goal attribute for the goals functionality using the attributes instead of the hard coding
- Call with John Peng 10am
- Came up with good idea to have the congratulations messages when the milestones have been reached or crossed
	- have attribute change for "goal-reached" (boolean) before current-goal attribute change (if all_read >= current_goal)  
	- send congrats email if goal_reached is true  
	- in current_goal attribute change set it to >= instead of >  
	- set goal_reached to false right away


## 7/19/21 M
- Tasks:
	- Compile everything related to using marketing automation (customer.io) for BfA and prepare for presentation
	- Test all of the campaigns with a new user
		- PCA!^ENuX9xOT%Qk
		- hellotheremy123
	- Put the webpages (getting started and recommended study) into emails (with same layout) and put into drip campaign
- Call with John Peng 10am



## 7/20/21 T
- Tasks:
	- Compile everything related to using marketing automation (customer.io) for BfA and prepare for presentation
	- Put the webpages (getting started and recommended study) into emails (with same layout) and put into drip campaign
- Need to figure out how to recreate the webpages in a responsive email
	- Customer.io already has good responsive design for drag-and-drop templates
	- When you hard-code the emails, you need to be careful (use mjml when using layouts)
	- Convert the Wordpress assets (svg) to png images (use Wordpress admin)
	- Monserrat and knockout font
- Call with John Peng 10am
- ~~New task~~
	- Report Progress Event (new)
	- list out completed goals (if someone didn't login for a long time) -> complement of "remaining_goals"
	- In collections -> change "amount" to "milestone" and add descriptions to replace "count" (50 is pen, and 100-500 is magnets)
- Important conclusion that we came to regarding customer.io and marketing automation
	- it's best to not try to do so much of the computational logic within the frontend (especially with a limited template language like liquid) -> do more of the logic outside (like in the backend)
- Worked on the recreation of the webpages in customer.io

## 7/21/21 W
- Tasks:
	- Finish up the webpage emails
	- Figure out how to copy elements from drag-and-drop emails into other emails
	- Finish up customer.io presentation
- Call with John Peng 10am
	- We went through a good number of things (the goals issue, the website itself, the drip campaign emails)
- The issue with the reward_goals was caused because the attribute change/creation doesn't allow for an array datatype -> this makes it impossible to actually access the data within the nested array which ruins the point of everything
	- liquid (and templating languages in general) and customer.io are just so so limited when it comes to programming logic
	- it really is better to just have everything that takes place in frontend be communicated to the backend for any serious programming logic 
- Finished the webpage emails
- Is it possible to copy elements from drag-and-drop into other emails?
	- Seems like it's not -> among many other extreme limitations when it comes to programming for email servers
- Called John again 11:40pm -> he figured out the array issue
	- [{% for obj in customer.object %}{% if obj.weight < 130 %}{"name":"{{obj.name}}","age":{{obj.age}},"weight":{{obj.weight}}}{%unless forloop.last %},{% endunless %}{% endif %}{% endfor %}]
	- Finally got the functionality for the reward_goals to work!
	- JU9i*Lwe46g2Tm%D
- Had to rework on the workflow for the report progress event -> fixing up some bugs after testing with new user
	- Found annoying bug regarding the formatting of the array (extra comma at the end ruining everything)
	- Fixed the issue with some string manipulation


## 7/22/21 R
- Tasks:
	- Compile everything related to using marketing automation ([customer.io](http://customer.io/)) for BfA and prepare for presentation (How to effectively roll out a new tool/process to company)
- Called John Peng 10am
- Tested all of the functionality of the emails again
	- yika@keyfood-lb.net
	- 6cdoFbAE)ML%imRr
- Made very basic shell of presentation for rolling out customer.io for BfA


## 7/23/21 F
- Called John Peng 10am
- Tasks:
	- Finish up content for customer.io BfA presentation
- Finished up customer.io BfA presentation