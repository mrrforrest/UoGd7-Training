# Live Feeds

* [Live Twitter Feeds](howto-livefeeds.md#to-add-a-live-twitter-feed-to-the-home-page)
* [External Source Live Feed](howto-livefeeds.md#to-display-a-live-feed-from-an-external-source)
* [Multiple Combined Event Feeds](howto-livefeeds.md#to-display-multiple-combined-event-feeds)
* [Multiple Combined Feeds \(All Feeds\)](howto-livefeeds.md#to-display-multiple-combined-feeds-all-feeds)

## To Add a Live Twitter Feed to the Home Page:

1. From the top administration bar, navigate to `Configuration` &gt; `Web Services` &gt; `Twitter`. 
2. At least one authenticated Twitter account is needed to have a live feed work properly. After the authenticated account is set up, you can also pull tweets from non-authenticated accounts, as long as you know the twitter handle \(@username\).
3. Select `Go to Twitter to add an authenticated account`. You will be prompted to sign into your Twitter account. 
4. Enter your username and password, then select `Authorize app`. 
5. Now that your authenticated account has been added, add any required non-authenticated accounts but pasting the handle in the "Twitter account name" field. 
6. Next, return to the home page. Select `Customize this page` at the botton of the screen. 
7. For the appropriate region, select `+` \(plus sign\). 
8. When the Add Content window opens, select `View panes` from the side menu. 
9. Select `View: S5 - Live Feed (Twitter)` from the list. 
10. In the "Num item" field, enter the number of tweets you would like to be displayed at a time. 
11. Select `Finish`. 
12. Select `Save` at the bottom of your screen. 

## To Display a Live Feed from an External Source:

### Step One: Add the Live Feed

1. From the administration bar, navigate to `Configuration` &gt; `Feed aggregator` &gt; `Add feed`. 
2. Enter the title and URL for the feed.
3. Set the update interval and number of news items shown in the block.
4. Categorize the news items if categories are defined.
5. Select `Save`.

### Step Two: Find the Aggregator Feed ID

1. From the Feed aggregator menu, click on the name of the feed. In the URL, you will see the feed ID, at `<site_name>/aggregator/sources/<feed_ID>`.

### Step Three: Add the Live Feed View Pane

1. From the page you would like to add a live feed to, select `Customize this page` at the botton of the screen.
2. For the appropriate region, select `+` \(plus sign\). 
3. When the Add Content window opens, select `View panes` from the side menu. 
4. Select `View: S5 - Live Feed` from the list. 
5. Override the title and add a new one if desired. If it is not overridden, no title will show.
6. Enter the Aggregator Feed ID.
7. Select `Finish`.
8. Select `Save` at the bottom of the page.

## To Display Multiple Combined Event Feeds:

### Step One: Create a Feed Category

1. From the administration bar, navigate to `Configuration` &gt; `Feed aggregator` &gt; `Add category`.
2. Enter a title for the feed category, like "Events."
3. Select `Save`. 

### Step Two: Add Feeds to the Feed Category

1. On the Feed aggregator page, find the name of a feed you would like to add to your new category.
2. Select `edit` beside the feed's name, under "Operations."
3. Under "Categorize news items," select the name of your new category. 
4. Select `Save`. 
5. Repeat steps 1-4 for any additional feeds you would like to add to a category.

### Step Three: Add the `EA1 - Upcoming Events teaser list` View Pane

1. From the page you would like to add a combined live feed to, select `Customize this page` at the botton of the screen.
2. For the appropriate region, select `+` \(plus sign\). 
3. When the Add Content window opens, select `View panes` from the side menu. 
4. Select `View: EA1 - Upcoming Events teaser list` from the list.
5. Change the number of items to display and override the title if desired.
6. Select `Finish`.
7. Select `Save` at the bottom of the page.

## To Display Multiple Combined Feeds \(All Feeds\):

### Step One: Create a Feed Category

1. From the administration bar, navigate to `Configuration` &gt; `Feed aggregator` &gt; `Add category`.
2. Enter a title for the feed category. 
3. Select `Save`. 

### Step Two: Add Feeds to the Feed Category

1. On the Feed aggregator page, find the name of a feed you would like to add to your new category.
2. Select `edit` beside the feed's name, under "Operations."
3. Under "Categorize news items," select the name of your new category. 
4. Select `Save`. 
5. Repeat steps 1-4 for any additional feeds you would like to add to a category.

### Step Three: Find the Aggregator Feed ID

1. On the Feed aggregator page, you will see the category you created appear under "Category overview."
2. Click on the new category. 
3. You will see the Aggregator category ID in the URL, at `<site_name>/aggregator/categories/<category_ID>`.

### Step Four: Add the `S5 - Live Feed (Category)` View Pane

1. From the page you would like to add a combined live feed to, select `Customize this page` at the botton of the screen.
2. For the appropriate region, select `+` \(plus sign\). 
3. When the Add Content window opens, select `View panes` from the side menu. 
4. Select `View: S5 - Live Feed (Category)` from the list. 
5. Override the title and add a new one if desired. If it is not overridden, no title will show.
6. Enter the Aggregator Category ID.
7. Select `Finish`.
8. Select `Save` at the bottom of the page.

