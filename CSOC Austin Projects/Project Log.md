# Project Log






## 2/10/22
### Log
- Basic maintenance on the Instagram Phantom scrapers

### Tasks



## 2/9/22

### Log
- Time in service groups to go over our current progress
- Helped Bryan Palm with simple Airtable task

### Tasks
- Helping Bryan Palma with simple Airtable task
	- Going through "Spring 22 DM Base 1 01.07.22 copy" and creating individual views with filter of "Spring DMer" so that each person knows exactly who they are assigned to

## 2/8/22

### Log
- Cleared out the Phantom (uttermostends) that had some trouble earlier
- Did some research on good newsletter designs for the freshmen sign-up 
- Emptied out the Phantoms and put data into Airtable
- Added more of the Instagram followers to Airtable in preparation for the next scrape
- Reset the Phantoms with the next batch

### Tasks
- Create a good email newsletter design for the freshmen sign-up verification
- ~~Quickly use two Phantoms to get the followers for the next batch~~
- ~~Reset the phantoms~~ 

## 2/7/22
### Log
- Zoom call with Reese and Merrill to discuss the work with the high school seniors
- Worked on finding another batch of Instagram accounts (13,000) for another week of scraping
	- Found that it's very effective to find influential accounts through the "culture of vanity" (girls who love to compliment one another regarding their beauty)

### Tasks
- ~~Setup up Zapier between Mailchimp and Airtable for the sign-up verification email (for the freshmen who sign up for the CSOC app) (Reese took care of it)~~
- Create a good email newsletter design for the freshmen sign-up verification
- (Tuesday) Reset the phantoms
- ~~Have an easy way to keep track of which high schools you're "done with"~~ 
- ~~Have another batch of 13,000 Instagram accounts ready for scraping~~





## 2/4/22 

### Log
- Worked on creating a formula for pinpointing which colleges the HS students are going to (among the DM'able Instagram accounts)
- Worked on confirming that the contact@christianstudentsoncampus.com is verified and tested that it actually works -> emails now go straight to inbox and not to spam!
- Did some research on good-looking email templates (through Mailchimp itself and through the integration with Canva)


### Tasks
- ~~document and prepare deliverable reports on scraping stuff and on MailChimp issues~~
- work with Reese on sending out alumni newsletter to 5-10% of alumni to test waters
	- ~~Find some good email templates~~
	- ~~Integrate with Canva?~~
- ~~create formula for pinpointing which colleges the HS students are going to~~


## 2/2/22

### Log
- Got to work on figuring out how to improve the email marketing platform with Mailchimp (getting emails into inbox and not spam, SMS verification and double opt-in for better security and gauging high levels of interest)
- The key is to use custom email domains for the organization (instead of relying on the default email domains from the email providers like Gmail or Yahoo Mail)
	- Ex: jerry@my-company.com instead of jerry@gmail.com
- Things you need to bring up to the saints:
	- There is the need to set up custom email domains in the hosting platform (Directnic) because the free email address (csoc.ut@gmail.com) is very limited in what can be done with it (easy for it to be classified as spam and not viewed as legitimate)
- There is already a custom domain - contact@christianstudentsoncampus.com -> this is the one used for newsletters 
- Got contact@christianstudentsoncampus.com domain verified and tested out whether or not the emails ended up in inbox instead of promotions or spam


### Tasks
- ~~Mailchimp tasks~~
	- ~~figure out website domain authentication stuff for the contact@christianstudentsoncampus.com domain~~
		- ~~double opt-in / sms verification (two factor authentication) / security issues~~


## 2/1/22

### Log
- Worked on the Instagram scrape pipeline stuff
	- Prepared more followers to scrape through Instagram follower collector and populated the HS followers base on Airtable
- Worked with Reese on more tasks
	- We set up another batch of profile scrapes
	- We need to go through the bios manually (those that found the string "22") in order to see how effective our formulas are in finding DM'able candiates (minimize false positives)
	- We did some analysis on how effective the formulas actually are

### Tasks
- ~~Make field for "DM'able" in HS Followers base~~
- ~~Redo set 1 for profile scrape while moving on with every other set~~ 

---

## 1/31/22

### Log
- Call with Tym Seay and Merrill and Reese regarding the strategy for the high school seniors
	- Learning from groups like Younglife in a way to reach the seniors before they go off to college
- Call with Merrill to fully clarify the new Instagram scrape peipeline and planned out further action
	- Have a new batch of 2000 ready for scraping 
- Emptied out all of my phantoms and prepared the csv files for import into Airtable (with dedupe and field appendange and bio scrape)

### Tasks
- Make field for "DM'able" in HS Followers base
- Redo set 1 for profile scrape while moving on with every other set 


## 1/28/22 
### Tasks
- Work on the task assigned yesterday by Merrill
	- Fully sort out the change in the pipeline
	- Compile the entire pipeline of data collection (finding DMable contacts) from "influencer research" to the final Airtable product
	- **Figure out where the final output should land up - in HS followers base or High School Team base -> ask Merrill (also about how to avoid entropy by archiving previous data)**
- Work on the Mailchimp stuff (figuring out the authentication of the domain name for Mailchimp)
	- Regularly check on the Mailchimp stuff (authentication process)
- Work on the Mailchimp newsletter work (especially Canva)
	- Work with Reese directly to consider what to actually do


### Log
- Updated HS Instagram scrape pipeline
	- After you accumulate the data from the profile scrapers, add the data fields from the "Followers of Influential HS students" table like, especially "HS" -> follow the template set in the FOIH table
	- The purpose of this change is to facilitate the DMing process even more to make the process very easy and smooth for those who are serving by helping to DM
- Contacted Tino regarding the domain authentication issue and got access to both Mailchimp and Directnc (the domain and web hosting platform)
- Worked on getting the csoc domain authenticated on Mailchimp
- Filled in the rest of the fields on Airtable (Instagram scrape)
	- Sets 2, 6, 3, 4, 5, 7, 8, 9, 10, 
	- For some reason set 1 doesn't match AT ALL


---


## 1/27/22
### Log
- Worked on tweaking the bio scrape Airtable formula a bit 
	- Not much more you can do in this aspect of the project
- Call with Merrill and Reese 4:35pm
	- Tasks:
		- Add column "HS" on HS followers table and find a way to map it all to High School Team table
		- Populate based off of those whom we scraped (example: high school in Followers of Influential HS Students (new)) and add the columns from the HS followers tables to the bio scrape table
			- Match the fields exactly and then paste all of the new fields into followers of influential HS students
			- Going forward you need to delete the Phantom busters after you use them so that you don't accumulate data from past profile scrape rounds
		- Find the percentage of DM'able people out of the total scrapped profiles
		- How to utilize DMers
			- Create formula that sorts by college? (UT26, college with a club, uncommitted)



## 1/26/22
### Log
- Got all of the Phantom busters to work properly (only one missing was the uttermostends one made by Bryan Palma)
- Considered what is the best way to find the influential accounts to scrape
	- Looking through school news (website, Twitter, Facebook, Instagram, other social media sites) to find well-known students who may/may not be popular (especially in sports or performing arts)
- Wrote brief summary of my experience in 3rd term
	- Intro
		- The training has only gotten more and more intense and more and more sweet and precious because daily I'm falling more in love with the wonderful person of Jesus Christ. Although there is much dealing and adjustment and breaking under the Lord's light, it's very sweet and precious knowing that I'm being conformed into His image (Romans 8:29) and that the day is coming when I will see be like Him when I see Him even as He is (1 John 3:2). The Lord really cared for me in my first two terms in placing me in KPCC with many other fellow trainees to pursue with. Now this term we got to be all together and really blend among all the former clusters around the country and around the world. Whatever transactions and dealings we've experienced in the past year has only been intensified this year. The "highs" are higher and the "lows" are lower but the experience and enjoyment of the Lord just goes from glory to glory!
	- Truth
		- One very big ongoing transaction I had during my third term was that I was severely convicted regarding my lack regarding the study of the truth. I realized that many times I was satisfied with just skating on the surface and that I didn't truly treasure the time that was allocated to me for mining out the truth. I foolishly thought that I could do anything but jealously guard my time with regard to truth study because I thought that I would have much more time during my interims to study "what I wanted to study". I quickly learned that there truly is no better environment to dive into the truth then in the training. Besides this, I've learned to really appreciate just how multifaceted and rich the Bible truly is and how it is critical to have a proper organization of the truth in the form of outlines. What a blessing it is to be under the ministry of the age!
	- Life
	- Character
	- Gospel/Service
		- Meeting with Cerritos and serving with the YP team was unbelievably sweet. All of us on the team unilaterally felt that we had entered into the experience of having a true vital group. Being able to physically be with the saints in Cerritos (with proper safety precautions, of course) and blend with them and care for the YP in a normal way was one of the top highlights of the entire training for me. 
	- Blending
		- There are many other things to say regarding the past term in the training but I felt that this is sufficient for now. After the term ended after the winter training, me and several other trainees embarked on a road trip that cut through the Grand Canyon and New Mexico and a number of cities in Texas, including Amarillo, Lubbock, Denton, Dallas, Liberty, Austin, Houston. To be on a blending trip like this, I feel, was exactly what we all needed to experience. Few things are more enriching and fulfilling to the entire tripartite being than to visit new places and meet new people and blend with many saints in many different localities. Everywhere we went we were met with loving care in the form of meals out, hospitality, and sweet fellowship. I'm currently settled in Austin, Texas, and I'll remain here until the beginning of next term. I've been working on data-related projects with other full-timers and I've been easing my way into the "full-timer schedule". What a blessing! May the Lord continue to bless the work in Austin and in all the localities around the world!



## 1/25/22
### Log
- Worked on optimizing the scraping pipeline
	- Always have a batch of accounts ready to scrape (and archive the previous master view on "Followers of influential HS students" table on the HS followers base) -> delete duplicates and divide into 20 batches for the 20 phantoms to run
	- Every day download the csv files and add to the "HS Insta accounts and bios" and delete duplicates -> keep studying the progressions 
	- Reset the "Followers of influential HS students" table but keep the view filters to automatically (remove autonumber and then dedupe and then put autonumber back on)
- We got the general pipeline down to a science (still figuring out how to actually find the influential accounts)
- Worked on the two critical steps that bookend the process: finding the influential accounts to scrape (who are the best people and what are the best sources?) & how do we utilize the results of the profile scrape (including bios) to actually find the best people to contact?
	- Finding influencers
	- Finding DM candidates
		- Find (or make) a script for pinpointing the key elements in bios
- Zoom call with Sam and Merrill (seeing how to get the genders and profile photos of the Instagram accounts and how to export the data into master list on Airtable)

### Tasks
- Learn how to scrape the gender and profile photos of the Instagram accounts (of those who are deemed "DMable")
- Learn how to find who is "DMable" through a script or formula in Airtable
	- Example of a formula to categorize the bios (from "Master List 2026")

```		
IF( 
	OR( FIND("ut", {biolower}), FIND("hook", {biolower}), FIND("texas", {biolower}), FIND("🤘🏽",{biolower}) ), 
	
	"UT" ) 
	
& IF( OR( FIND("26", {biolower}), FIND("freshmen", {biolower}) ), "26")& IF( OR( FIND(" out", {biolower}), FIND("twu", {biolower}), FIND("boutique", {biolower}), FIND("uark", {biolower}), FIND("jmu", {biolower}), FIND("flute", {biolower}), FIND("alabama", {biolower}), FIND("north texas", {biolower}),FIND("a&m", {biolower}),FIND("utsa", {biolower}),FIND("utd", {biolower})), "not UT" ) & IF(description=BLANK(),"","UT26")
`

biolower => LOWER({bio})

```

### Considerations
- Compile lists of good tools (especially good APIs for marketing activities)
	- APIs
		- https://sheetsformarketers.com/marketing-apis/
		- https://blog.hubspot.com/website/free-open-apis
	- Other
		- https://www.lyfemarketing.com/blog/free-digital-marketing-tools/
		- https://buffer.com/library/free-marketing-tools/



## 1/24/22 
### Log
- Worked with Reese to setup workflow for Instagram profile scraping on Phantom Buster to find as many high school seniors to contact and connect
	- Filled in all 20 of the dummy Instagram accounts
	- Taught him the general workflow for the Instagram scraping
- General daily schedule:
	- Morning coordination
	- Touching base with Reese and Bryan and Merrill
	- Going with Spencer to Foremost or with Bryan to appointments

### Schedule
- 10-12:30pm; 1-6pm

### Goals
- Overview of project (updates)
	- scrape as many high school Instagram accounts as possible (all that matters is that they are seeking and that they are going to college) 
	- no matter where the high schoolers end up going (only 56% actually go to college), they can be connected to sister clubs around the country 
	- research and optimize the pipeline for finding these seeking ones (calculate the "funnel rates": profiles scraped => candidates => DMed => responded => continued contact => etc.)
- Compile a full run-down of the workflow and procedure for the components of the outreach project -> FINDING people and CONTACTING people and CONNECTING people
	- FINDING
		- Compile list of influential high schoolers in Austin and scrape all the followers 
			- Run 20 busters with 672 profiles per buster (using filter on autonumber to easily divide the high school follower data into the 20 separate csv files )
		- Use profile scrape to find the bios of all those followers and dedupe and run through algorithm for finding the promising students (graduating seniors)
		- Can find 13,440 students a week (20 phantom busters and 12 profiles/hour for 8 hours a day) and can find a percentage of those students who are promising for contact 
	- CONTACTING
		- Give list of the promising students to the serving ones and college students for personal contact through direct messages 




## 1/21/22

### Schedule
- 10-12:30pm; 1-6pm 
	- Verse tune and palace, ~~shower and shave P hair~~
	- experiment with Facebook Phantom busters
	- Clear tasks:
		- ~~type out Thanksgiving conference outlines~~
		- ~~Semiannual digestion~~
		- ~~Clear binder entirely~~
		- ~~Spend 5 minutes working on writing truth song~~
		- ~~Spend 10 minutes working on compiling truth from Trello and GitHub~~
	- ~~Prep dinner at 6pm~~
	- ~~Join Bryan's small group meeting~~
	- ~~Prepare to move out to Ezequiel's place~~
- Tasks:
	- ~~Make two more dummy Instagram accounts and add to Google Sheet~~
		- ~~Used TempMail to make temporary email accounts to then make dummy Instagram accounts~~
	- ~~Find good influential HS senior accounts rather than scraping from HS group accounts~~
		- ~~Sam Xiong has a list of them~~
		- ~~Started the follower collector for the influential personal accounts~~
	- Do research into scraping Facebook groups for 25 minutes
		- Finding prospects through Facebook and then scraping for Instagram usernames for DMing
		- You can use the output of one Phantom (Facebook group extractor) for the input of another Phantom (Facebook Profile Scraper) and then find Instagram usernames 
	- **New Assignment:**
		- Do as much research as possible into all sorts of "access points" (Facebook, Snapchat, TikTok, Patio)
			- Facebook
			- TikTok
		- Learn (plunder from Egypt) the best methods and techniques and frameworks for "acquisition" 
			- The key difference is that we are not trying to gain "customers" in a secular way, but we are simply finding potential candidates for us to contact 1-by-1 (the most effective way to establish connections in a meaningful way)
	- ~~Other things to do:~~
		- T~~ype out Thanksgiving conference outlines~~
		- ~~Semiannual digestion ~~
		- ~~Lumosity and icebreaker and story~~
		- ~~Clear binder entirely~~
		- ~~Spend 5 minutes working on memorizing Ephesians~~
		- ~~Spend 10 minutes working on compiling truth from Trello and GitHub~~


## 1/20/22
- What is the point of this project? It is to automate the process of finding open students (current and prospective) to potentially be contacted and built up with
	- The goal is to find as many good candidates for DMs as possible from the HS accounts
- Another project to consider: utilizing Facebook scrape in conjunction with Instagram (because Facebook tends to have more reliable information for contacting students and Instagram has a much better response rate for DMs)
- **Procedure for Instagram scraping**
	-  Use Instagram follower collector on many Texas HS Instagram accounts (group accounts or influential high schoolers)
		- Proper scraping procedure: 5000-9000 followers every 15 minutes (maximum of 20 times a day for scraping)
			- To be safe, run twice per working hour and have 9 profiles with up to 1000 followers scraped per profile
		- Put the results into the HS followers Airtable base 
		- Use "delete duplicates" script to dedupe before putting through profile scraper to save time
		- Use autonumber 
		- Divide up the results in chunks of multiples of 96 so that each of the ten slots can be used for running Instagram profile scraper 
	- Run the de-duplication algorithm (use "delete duplicates" script instead of using dedupe app)
	- Compile the lists of accounts with bios and then run through algorithm to find the good candidates to DM
	- Everyday or every 2 days have a new batch to run the profile scraper on
		- Have a huge table of Instagram accounts that you can divide into badges of 96 or 192
			- Each phantom can scrape 12 profiles an hour for 10 phantoms -> 960 total a day
- **Action points:**
	- ~~Learn how to do the de-duplication~~ (SOLVED: there is the dedupe app on Airtable) 
	- Learn how to scrape the good bios
		- REGEX? Formulas?
	- Do some research into scraping Facebook groups

### Schedule
- ~~3-3:17 -> work on compiling more Instagram accounts~~
- ~~Spend 20 minutes on LS of John 20~~
	- Break for prayer 
- Do research into scraping Facebook groups for 25 minutes
	- Finding prospects through Facebook and then scraping for Instagram usernames for DMing
	- You can use the output of one Phantom (Facebook group extractor) for the input of another Phantom (Facebook Profile Scraper) and then find Instagram usernames 


---

## 1/19/22

### Tasks
- Airtable (HS Followers and High School Team)
- Phantom account (God-man): e-mail: [csoc.ut@gmail.com](mailto:csoc.ut@gmail.com) PWD: befilledeph5:18
- Running 10 phantoms with 10 dummy Instagram accounts (can run 96 a day (12 per hour for 9-5) on 10 phantoms) -> 960 total profiles a day
	- Dummy account: jeretigerxu (password: SUiHVrHe88nZ9cr)
	- Refer to [Dummy Accounts List](https://docs.google.com/spreadsheets/d/1yUc6KS1BDj3ycZ88YpAAquU1ekz_RHxCb1oMx7JEaxA/edit#gid=0) for the other dummy accounts
- Use the profile scrapers on Phantom to scrape many Instagram accounts 
	- Instagram Profile Scraper (so that we can get the bios and other information of the Instagram accounts)
	- Phantom can scrape up to around 96 (max 100) (12 profiles per hour for 8 hours) profiles a day for Instagram Profile Scraper 
- Do this procedure for many high schools (like Westlake High School) to gain more candidates 
- Procedure:
	- Make sure that all the slots (currently 10) are running 
	- Keep them running until the csv files are fully scrapped
	- Append the results into the HS team instagram accounts table (so they can be deduped) -> ultimately you are looking for the best candidates based off of their Insta bios


### Issues
- You have to stay logged in to Instagram on a browser (Chrome, Firefox, Safari) so that the session cookies don't expire (you have to stay logged in for the entire day)
	- Procedure: have a bunch of devices to run one Instagram account (do not sign out)