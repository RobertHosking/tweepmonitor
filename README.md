# Monitor Twitter username for availability

NOTE: This is a quick and dirty script. Some prior knowledge of Twitter API, PHP and cronjobs would be helpful.

We search each username via the Twitter API and look for Error CODE 50 = User not found.

I cannot provide assistance with setup, configuration or support. I provide the code "as-is".

### REQUIREMENTS

1. Twitter API https://developer.twitter.com/

2. Server-side PHP and Cron.

### Username Setup

Add your usernames to the file **usernames.txt** and make sure each ends with a comma "," and contains no spaces.

For example, **usernames.txt** contents would look like:

`handle1,handle2,handle3,`

### Twitter API Setup

Add your Twitter API details to the file **config.php**

### Cronjob Setup

Twitter has API rate limit of 1 query per second. Limit the number of usernames to monitor accordingly.

You can set up a cron job to execute the file **bot.php** every x minutes. 

### Notification Setup

Add your email address in the file **bot.php** where you see:

`$recipient_email = "";`
