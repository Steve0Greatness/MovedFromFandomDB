# Forked from Fandom DataBase

This is a general database for wikis that have officially forked from Fandom to another platform.

## Why move from Fandom?

1. **Ads.** Fandom is *full of ads.* There's dropdowns, sidebars, everything.
2. **Fandom branding.** Fandom makes sure you know that a wiki is hosted on it. It's branding is plastered everywhere, almost as much as the ads.
3. **Links outside of dedicated communities.** When you go to a specific Fandom wiki, you expect to see content specifically about that subject, right? Well on Fandom, this doesn't appear to occur to them. You can find links to other communities at the bottoms of pages, as well as when you utilize the search functionality.

These are only a few reasons that wikis may have for moving off of Fandom, however, there are likely more, I'm not an admin of any Fandom wiki.

## What's the point of this?

This provides an easy to reference database for Fandom wikis that have moved to other places. The database itself is within the JSON format, making it easy to parse for machines, while keeping it readable for everyone else. Although it is readable by humans, this database is mostly intended for scripts or extensions.

An example of a script that uses this is [`example.user.js`](example.user.js), feel free to download that user-script using your user-script manager(ex. [Violentmonkey](https://violentmonkey.github.io/)). **Additional installation sources:** [Greasy Fork](https://greasyfork.org/en/scripts/476527-fandom-redirect)

## Where can I find the database?

The entire database is accessible through the [`database.json`](database.json) file. Keep in mind that you need to use the bottom level domain for the Fandom wiki: e.g. in `https://minecraft.fandom.com`, the bottom level domain would be `minecraft`.

## How can I contribute?

You can create an issue about any missing wikis, they'll probably be added very quickly.

On the other hand, if you know how to write JSON files, then feel free to submit PRs that add missing wikis. Make sure to mention any issues that are resolved with your PR(you can reference issues using `#<issue number>`), so that they can be closed as resolved after your PR gets committed.

Other than that, the best you can do is spread the word. Make sure to not go off topic to let people know, though. Maybe just putting it in a forum signature, or politely linking new contributors to the fandom-version of any of these wikis to this repository, and also maybe giving them the URL to the new wiki.

## Usage Documentation

To get information about a Fandom wiki, use it's bottom level domain.

`newURL`: The URL currently used by the wiki
`pathInfo`: General information about the wiki article's paths {

`interchangeable`: this parameter should be used if all pages from the Fandom wiki are on the new one(full fork)
`includeWiki`: if the wiki uses `/wiki/` before every page(possibly excluding the main page)
`pretext`: if a wiki has anything before `/wiki/`(or if `includeWiki` is false, then before the page's _actual_ path)
`searchPretext`: If `interchangeable` is false, then all pages should redirect to a search page. This is the path to the search page.

}
`search`\*: How web searches should be handled {

`homeTitle`: the title of the main page.
`favicon`: URL to to the favicon of the webpage. Can either be found at `favicon.ico`, or whatever the `link[rel=icon]` is.
`subPages`: Info about the titles of articles/sub-pages {
`noChange`: if the title template was changed at all.
`articleTitle`: how to get the article's title {
`splitter`: what is used to split the article name, and the wiki's name.
`index`: once split, what index the title will be at.

}
`titleJoiner`: what the title is joined by
`appendTitle`: text appended after the article's title

}

}

\* Not fully implemented