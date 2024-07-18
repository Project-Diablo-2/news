# Project Diablo 2 News Project
### **Overview**

This repository contains two JSON files:

    - **news.json**: This file holds a collection of news articles with details about various updates and events related to Project Diablo 2. Each entry includes a date, title, summary, content, optional image, and a link for more information.
    
    - **reset.json**: Contains details about the seasonal resets of the game, including the title, summary, time, and a relevant link.
___

### File Structure

  ## **news.json**
  We can have as many entries as we want of these
```json
[
    {
        "date": "Month Day, Year",   <-- This can really be any String
        "title": "Title of the News Item", <-- Title of the News item
        "summary": "A brief summary of the news", <-- This will be the words shown in the launcher
        "content": "Detailed content with Markdown formatting supported",  <-- This will not show in launcher and is for website
        "image": "URL to an image or null if no image is provided", <-- This will not show in launcher and is for website
        "link": "Direct URL to the source or additional information" <-- The URL provided here is for if users select a news item from the launcher
    },
]
```
___
## reset.json
    There can only be one of these the launcher will check the resetTime and see if it's in the future. if its in the future show the news item.  We do the ISO 8691 format so the time will be localized to the users local time
```json
    {
        "resetTitle": "Title of the Reset Event", <-- title for reset announcement
        "resetTime": "DateTime in ISO 8601 format", <-- use the projected reset time and convert it to iso 8601 at this url https://www.timestamp-converter.com/
        "resetSummary": "Summary of the reset event",
        "resetContent": "Detailed content or null if not applicable", <-- this can be null will only be used on website but its not implemented>
        "resetLink": "URL to more details about the event" <-- a url for if player clicks announcement they are taken somewhere
    }
```

