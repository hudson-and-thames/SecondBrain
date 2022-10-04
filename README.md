# Mary's Setup
<div align="center">
   <img src="https://github.com/Hudson-and-Thames-Clients/SecondBrain/blob/master/Marys%20Room/_attachments/red_pill.png?raw=true" width="75%" 
   style="margin-left: auto; margin-left: auto; display:block;">
  </br>
</div>

We need to set you up so that we are all in sync. The following needs to be done:
1. [Download](https://obsidian.md/download) and install Obsidian
2. Clone this repo to your local machine and set the branch to develop. (All Pull Requests must be to develop, only the bran maintainer may push to master.)
3. Open Obsidian and Open folder as vault, head over to the Marys Room folder inside the SecondBrain repo and select it. 
4. Accept all the plugins and community plugins that we have added. 
5. Head over to the Marys Room node and you can explore the system from there.

After going through the setup note, please check out the Team Conventions and Tips.

## Basic tools
- All the notes use the *Markdown* markup language.
- Use `ctrl + N` to open a new note, type in the title and then use `ctrl + T` to insert a new template. The title and date will automatically be filled in. There are many different templates that you can choose from, depending on what you want to do.
- Use [[]] with the note that you want to link inside, to link the current note you are using.  

## Note structure
You can structure the note as fits the purpose. What is important to include is the relevant metadata. The metadata allows us to organise the data and tag each other in relevant material. The metadata is organised as Key :: Value. For example Creator :: Michael, since Michael is the creator of this note.  
The possible metadata that is included in a note is:
- Topics :: 
- Reference ::
- Type :: #intro 
- Creator ::
- Rating ::
- TAF ::
- Discussion ::
- Dis_Topic :: 
- Resolved ::
- Date :: {{date:YYYY-MM-DD}}{{time: HH:mm}}

All the metadata keys will explained in the [[Team Conventions]] node.

## Folder system
There are folders for atoms, molecules, particle, topics, sources and tables. After you have created a new note, simply drag it into the appropriate folder.  All the different templates can be viewed in the _templates_ folder.

If you add any images or other _attachments_, please move them to the attachments folder.

## Topics
Topics are the overarching concept that connects similar concepts to each other. As the graph and connections grow subtopics could emerge. You should link only the **most** relevant or closets topics by adding any other related topics. For example if you are working on a concept with meta-labelling is should look like this:
Topic :: [[Marys Room]], Machine Learning

Therefore you **only** link the subtopic or closets topic but also reference or tag the main topic.

## Tables
Tables are way to see content that you are tagged, need to discuss or see recent activity. Tables use `dataview` which is similar to SQL. If would like to make your own table please check the [dataview](https://blacksmithgu.github.io/obsidian-dataview/) website to learn how to use it. If open up Obsidian, please check the [[Discussion]] and [[Tagged Content]] tables to see if someone needs you to look at something. You can explore the other tables as well to see interesting ideas or track progress.   

## Problems
If you encounter any problems with the initial setup, please tag Michael in a discussion Michael in a discussion.

Alternatively if there is something wrong, it probably has to do with the syncing. Please make sure to check the following.

- Your Sync plugin is turned on and all the options under the Sync plugins are toggled on.
- Make sure the following setting are correct.
	Core Plugins installed
	- Sync
	- Templates
	- Publish
	
	 Community Plugins
	 - Admonition
	 - Dataview
	 - Sliding Pans

Setting -> Options -> Files & Links -> Excluded files :
_attachments_
_scripts_
_templates_
Tables

Everything should be setup now and your journey to start contributing to the room is ready to go! Please make sure to go through [[Team Conventions]] and [[Tips]].

<div align="center">
   <img src="https://github.com/Hudson-and-Thames-Clients/SecondBrain/blob/master/Marys%20Room/_attachments/neo-plugging-to-matrix.gif?raw=true" width="75%" 
   style="margin-left: auto; margin-left: auto; display:block;">
  </br>
</div>

---
Topics:: [[Marys Room]]
Reference::
Type:: #intro 
Creator :: Michael
Date:: 2022-07-04 09:17
