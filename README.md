# Moved from Fandom DataBase

This is a database that keeps track of wikis that have moved from the Fandom to their new one.

## Why move from Fandom?

1. **Ads.** Fandom is *full of ads.* There's dropdowns, sidebars, everything.
2. **Fandom branding.** Fandom makes sure you know that a wiki is hosted on it. It's branding is plastered everywhere, almost as much as the ads.
3. **Links outside of dedicated communities.** When you go to a specific Fandom wiki, you expect to see content specifically about that subject, right? Well on Fandom, this doesn't appear to occur to them. You can find links to other communities at the bottoms of pages, as well as when you utilize the search functionality.

These are only a few reasons that wikis may have for moving off of Fandom, however, there are likely more, I'm not an admin of any Fandom wiki.

## What's the point of this?

This provides an easy to reference database for Fandom wikis that have moved to other places. The database itself is within the JSON format, making it easy to parse for machines, while keeping it readable for everyone else. Although it is readable by humans, this database is mostly intended for scripts or extensions.

An example of a script that uses this is [`auto-search.user.js`](auto-search.user.js), feel free to download that user-script using your user-script manager(ex. [Violentmonkey](https://violentmonkey.github.io/)).

## Where can I find the database?

The entire database is accessible through the [`database.json`](database.json) file. Keep in mind that you need to use the bottom level domain for the Fandom wiki: e.g. in `https://minecraft.fandom.com`, the bottom level domain would be `minecraft`.

## How can I contribute?

You can create an issue about any missing wikis, they'll probably be added very quickly.

Other than that, the best you can do is spread the word. Make sure to not go off topic to let people know, though. Maybe just putting it in a forum signature, or politely linking new contributors to the fandom-version of any of these wikis to this repository, and also maybe giving them the URL to the new wiki.