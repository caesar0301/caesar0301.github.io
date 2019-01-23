---
title: Top tricks to make your Zotero more powerful
date: 2015-01-08
comments: true
tags:
    - Tools
---


[Zotero](http://www.zotero.org) is *a free, easy-to-use tool to help you collect, organize, cite, and share your research sources*. It support a wide range of documentation types from papers to presentations, from web pages to notes and drafts. A SQLite database and online storage (yet with limited space) are used to store and index the citation information of each resource item. Here I wanna share some usage experience or tricks to make this tool to be a more powerful assistant in your researches. Feel free to post your own trick while using Zotero.

<!-- more -->

## Extend cloud space incorporating with Dropbox

One of attractive features of Zotero against [Mendeley](http://www.mendeley.com) is allowing relative indexing path of resouces. Under the "Preference -> Advanced" tab, you can change the profile path and data path relative to your local folders. This brings about convenience in:

- Syncing the library among multiple devices
- Extending the cloud storage space with 3rd party services, e.g., Dropbox

Enabling this feature is quite easy without any side effects:

1. Copy your **entire** Zotero profile folder into arbitrary folders of Dropbox;
2. Change both the profile and data path under the advanced tab;
3. Restart the client.


## Use your own tags without auto-generated ones

By default, Zotero can extract and import tags from paper keywords. It sometimes makes your organization a mess with thousands of tags classified with varying considerations. The best manner is setting up personalized tagging system after tidying the whole tag database. Two steps are required to be followed:

1. Disable auto tag importing in "Preference -> General";
2. Clear existing auto-imported tags in your database (skip if you are using Zotero from the scratch);
3. Manually add tags to items while adding new stuff.

As Zotero manages resources with a SQLite database, some manual operations are required to finish the task in Step 2. Here I give a successful way with reference to [discusses in Zotero forum](https://forums.zotero.org/discussion/4051/remove-all-tags/) (thanks to @Jackliu008).


(i) Install SQLite browser to modify the Zotero database. A fast success is achieved by installing a firefox add-on like [SQLite Manager](https://addons.mozilla.org/en-US/firefox/addon/5817/);
(ii) Open SQLite Manager and connect to Zotero database (``zotero.sqlite`` under the data folder);
(iii) Excute two lines of SQL commands to clear auto-imported tags:

```sql
delete from itemTags where itemTags.tagID in (select tags.TagID from tags where type = 1);
delete from tags where type = 1;
```

**Note:** `type = 0` encodes your manually-added tags and `type = 1` represents
the auto-imported ones.

(iv) Disconnect the database.


## Integrating citation management with Emacs/Latex

One of nontrival tasks in researches is organizing the citation stuff while writing papers. If you are using Latex with the Emacs editor, you are lucky to introduce Zotero efficiency into the writing. [Zotelo](https://github.com/vspinu/zotelo) is a Emacs extension contributed by
@vspinu to export and synchronize local bib database and Zotero library. Installation details introduced by the project contains three main requirements:

- Manage Zotero library with firefox-based client;
- Install [MozRepl](https://addons.mozilla.org/en-US/firefox/addon/mozrepl/) firefox add-one to enable console communication used by Zotelo.
- Integrating Zotelo extension into Emacs.

Voila! You can enjoy efficient citation management in your writing.
