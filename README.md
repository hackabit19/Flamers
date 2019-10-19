# Flamers

# SAFE INTERNET USAGE
* The internet is a wonderful and informative platform. While we can leverage its potential to gain information about anything and everything, it also brings a lot of potential risk. The vulnarability while exploring the web brings a risk of showcasing us along with the children, with certain information which might bring a feeling of uncomfortability, destruction etc.
* Violent scenes are “scenes one would not let an 8 year old child see because they contain physical violence”. 

This GitHub repository is intended to automatically classify the video content into violent or non-violent using the method of Deep Learning.

The visual and audio dataset information has been collected from Hollywood Movies and YouTube.
The folder [annotations] contain the textual information about the violance annotations of the visual and audio modelarity. It has space-separated text format where each line in the former compiles to the structure:
start-frame end-frame
whereas, each line in the latter compiles to the structure:
start-frame end-frame (concept-detail)       Or
start-second end-second (concept-detail) 

The ipynb file- [DataAnalysis] contains the analysis of textual data or the informative dataset in the form of respective clear graph for the different datils of concept.

The concept detail for each categories can be plotted on the basis of the following counts:
* Violent segment:
    Two different annotations are provided depending on the two definitions of violence. However there are some cases where different actions are overlapping are proposed as a single segment. Thus, the additional tag ‘multiple_action_scene’ has been added.
* Video concept – Presence of blood:
    The additional tags represent the proportion of the screen covered with blood.unnoticeable: there is some blood pixels and their surface represents no more than 5% of the image
low: surface_of_blood_pixels is between 5% and 25%
medium: surface_of_blood_pixels in [25%, 50%[
high: surface_of_blood_pixels > 50%
* Video concept – Fights :
    1vs1: only two people fighting
small: for a small group of people (number of people was not counted, it will roughly correspond to less than 10)
large: for a large group of people (> 10)
distant attack: no real fight but somebody is shot or attacked at distance (gunshot, arrow, car, etc)

* Video concept – Presence of fire
    When the fire is not yellow or orange, an additional tag indicates its color. In case too many extra colors are visible, a ‘multicolor’ tag will be used.
   
* Video concept – Presence of firearms (guns and assimilated) 
       Guns with bayonets were annotated as guns, whenever a part of it is seen, even if it is a part of the bayonet.
* Video concept – Presence of cold arms 
    Same as for firearms but for any kind of cold arms. Guns with bayonets were annotated also as cold arms, only when the bayonet is visible.
* Video concept – Car chases
    Annotations of car chases indicate segments showing a car chase.
* Video concept – Gory scenes 
    Annotations of gory scenes will indicate graphic images of bloodletting and/or tissue damage.Additional tags describing the event/scene were added in this case.
* Audio concept – Gunshots 
    Each gunshot was annotated as a single segment whenever possible, with tag ‘gunshot’ and corresponding starting and ending times in seconds. Tag ‘multiple_actions’ was used when several events happen together. Tag ‘(nothing)’ corresponds to segments with no event. Canon fires were also annotated as gunshots.
* Audio concept – Explosions 
    with tags ‘explosion’, ‘multiple_actions’ and ‘(nothing)’
* Audio concept – Scream 
     with tags ‘scream’, ‘multiple_actions’ and ‘(nothing)’. Effort noises were annotated using tags ‘scream_effort’, or ‘multiple_actions_scream_effort’. Animal screams were not annotated, neither were screams in which one can recognize words.
     
     ______________________________________________________________________________________________________________________
     
