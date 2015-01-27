Pipewatch "Groups" Package

This package is meant to manage group pages.

- Protector list and pages are blocked depending if you have permission or not (Public, Selected Members Only, Logged In, Private)
- You can only access Editing options if you are the creator of the page (or an Admin)
- You can only Create or Edit a page if you are logged in

- All child pages have ID of parent, all parent pages have ID of child. For now they are listed only in one array but this is flexible with a bit.
- Textareas can be ordered manually through arrows on the right hand side (moves around and re-stores in array)
- Upload objects are put into directory, then also attached as a full object onto the parentGroupPage
- Ability to upload to Google Bucket included (60 days free?)
- Members can be added to page object via dropdown menu (easily removed,listed in a similar fashion)
- Editing is mostly inline, reloads page, main textarea not inline at all

Pipewatch "Map" Area

This sits on top of group pages and plots out certain post types.

- Made in Angular Map so it safely reloads every time
- Arrays and objects of overlays set up as Factories
- First Nations Land (direct Google Maps objects), Languages (JSON), municipal maps (overlays)
- Update simply adds location with title and content into map
- Proposed project allows ability to add sources
- Spills choice, many options to add more information
- Icons:
    -- Should basically have NEWS, UPDATES, SPILLS
    -- #49bf37 (UPDATES):
        -- Protest (protest)
        -- General information (information)
        -- Special urgent information (regroup)
    -- #c03639 (SPILLS):
        -- Car accident (spill for road accidents) (caraccident)
        -- Shipwreck (spill for ocean accidents) (shipwreck)
        -- Offshore oil rig available 
        -- Train spill (steamtrain)
        -- Random pipeline oil spill (blast)
    -- #22849c (PROPOSED PROJECTS):
        -- Upcoming mine project (mine)
        -- Upcoming dam project (dam)
        -- Upcoming LNG or Oil pump (oilpumpjack)
        -- Upcoming factory project (factory)
        -- Upcoming random industry related project (museum_industry)
        
Parent Pipewatch

This controls the overall appearances, adding and removing modules from the page.

- Paths to all page types are under "groupPages" slug (not that great for SEO but easier to keep organized)

====

TO DO
- Move it to live
- Functionality
    - Media uploads page attaches to what parent?
    - Ensure functionality of updates from map, including icon selection, storage in DB, multiple of each object, etc
    - Viewing news pages and their information
- Start loading in information

//Bugs
- Child page saving isn't perfect, have maximum of 3-4
- Better button arrangement when reordering
- Private doesnt seem to work on textareas
- Fix problem with reload when editing content
- Double check over form submissions to make sure required stuff is actually required

Improvements:
- Fix up GCS buckets once uploaded into
- Admin page can update live, be more nicely styled, etc
    - Also, this should hide private pages from non-admin
- Add a really simple global point game system
- Protectors
    - Have recently updated sort up to top, etc
