# The Instagram Scrape Pipeline

### Procedure
- Every morning, check the Phantoms and their statuses | if you want you can download the results every few days (because you can always delete duplicates later)
- Every morning, check whether or not you have a bunch of profiles ready to scrape

- **Finding influencers**
	- Continuously compile good influencers (school accounts, finding personal accounts through school websites or personal connections) 
		- According to our historical analysis, the best candidates to look for are those with around 400-700 followers (those who aren't super popular but still have a considerable number of friends around the same age)
		- A very effective way to find good influential accounts is to jump from account to account and go through the comments to quickly find public/private and follower account -> especially among girls there is a lot of activity (take advantage of the fact that they love to compliment each other)
	- Use the follower collector to scrape all of the followers and populate the FOIHS base
		- Proper scraping procedure: 5000-9000 followers every 15 minutes (maximum of 20 times a day for scraping)
			- To be safe, run twice per working hour and have 9 profiles with up to 1000 followers scraped per profile
	- Create the field "HS Query Source"
		- Filter based off the query (because you know where the influential student went to) to then fill in every follower 
	- Using autonumber and filtering, create 20 extra views for each of the new csv files to then profile scrape
- **Finding DM candidates**
	- Profile scrape all of the data compiled from the follower collector
		- (important - be sure to delete and re-create the phantoms in order to reset and avoid bringing in old data) -> or you can delete the data in the file browser option
		- Profile scrape in batches (20 batches for the 20 phantoms) 
			- Run 20 busters with 672 profiles per buster -> (12 profiles/hour for 8 hours a day for 7 days in the week) -> 13,440 profiles per week you can scrape
			- Use the Session Cookies Google Sheet to be very clear which Phantom is doing what and which batches are being scraped 
		- Append the necessary fields
			- Add some of the data from FOIHS base (for each batch) and combine with the output data from the profile scrapes
			- Fields to keep from profile scrape output: publicEmail, contactPhoneNumber, bio, followersCount, followingCount, isBusinessAccount, postsCount, website, mailFound, snapchat 
		- Dedupe the data by deleting duplicates
		- Formula for finding the good bios (DM'able) 
			- ```IF(FIND("22", LOWER({bio})), "22") & IF( OR( FIND("✝️", LOWER({bio})), FIND("🙏🏾", LOWER({bio})), FIND("bible", LOWER({bio})), FIND("christian", LOWER({bio})), FIND("🙏", LOWER({bio})), FIND("jesus", LOWER({bio})), FIND("lord", LOWER({bio})), FIND("✟", LOWER({bio})), FIND("god", LOWER({bio})) ), "believer")```
		- Formula for finding the college that they are committing to:
			- ```IF( OR( FIND("baylor", LOWER({bio}))), "Baylor") & IF( OR( FIND("shsu", LOWER({bio}))), "Sam Houston State University") & IF( OR( FIND("vanderbilt", LOWER({bio}))), "Vanderbilt") & IF( OR( FIND("cornell", LOWER({bio}))), "Cornell") & IF( OR( FIND("dartmouth", LOWER({bio}))), "Dartmouth") & IF( OR( FIND("ju", LOWER({bio}))), "Jacksonville University") & IF( OR( FIND("ut", LOWER({bio})), FIND("mccombs", LOWER({bio}))),"UT Austin") & IF( OR( FIND("texas a&m", LOWER({bio})), FIND("tamu", LOWER({bio}))),"Texas A&M") & IF( OR( FIND("wooster", LOWER({bio}))),"Wooster") & IF( OR( FIND("duke", LOWER({bio}))),"Duke") & IF( OR( FIND("college university", LOWER({bio})), FIND("texas college university", LOWER({bio}))),"Texas College University") & IF( OR( FIND("smu", LOWER({bio}))),"SMU") & IF( OR( FIND("columbia", LOWER({bio}))),"Columbia") & IF( OR( FIND("ole miss", LOWER({bio}))),"University of Mississippi") & IF( OR( FIND("emory", LOWER({bio}))),"Emory")```
			- Top colleges:
				- UT Austin
				- Texas State
				- Texas A&M
				- Baylor University
				- Southwestern
		- Formula for finding out if someone is a believer:
			- ```LEN( IF(FIND("0:", LOWER({bio}),0), 1) & IF(FIND("1:", LOWER({bio}),0), 1) & IF(FIND("2:", {bio},0), 1) & IF(FIND("3:", {bio},0), 1) & IF(FIND("4:", {bio},0), 1) & IF(FIND("5:", {bio},0), 1) & IF(FIND("6:", {bio},0), 1) & IF(FIND("7:", {bio},0), 1) & IF(FIND("8:", {bio},0), 1) & IF(FIND("9:", {bio},0), 1) & IF(FIND("jesus", LOWER({bio}),0), 2) & IF(FIND("christ", LOWER({bio}),0), 2) & IF(FIND("god", LOWER({bio}),0), 2) & IF(FIND("seek Him", {bio},0), 2) & IF(FIND("count it all joy", LOWER({bio}),0), 2) & IF(FIND("His", {bio},0), 1) & IF(FIND("✝️", {bio},0), 2) & IF(FIND("✞", {bio},0), 2) & IF(FIND("saved", LOWER({bio}),0), 2) & IF(FIND("grace", LOWER({bio}),0), 1) & IF(FIND("He is", {bio},0), 1) )```



### "Material" to Product
- Start with some influencers who have lots of followers (good amount of HS students)
- End with an Airtable base with a number of good candidates for DMing with a lot of information on each Instagram account



