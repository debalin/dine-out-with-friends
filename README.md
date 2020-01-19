### Motivation

We have had times with friends when we want to dine out, but we are unsure about where to eat. We have a plethora of choices suggested by friends, but choosing one among them is generally riddled with uncertainities and disagreements. The most common platform where we tend to decide this is generic and not really built for **food**, i.e. the common messaging platforms such as WhatsApp, Telegram, SMS groups, etc. We want to provide a solution which will help you choose a restaurant when you are planning with friends, while taking into account cuisines, locations and any specific restaurant preferences that you all might have. We want you stumble upon . discover new restaurants in the process. 

### Surface-level UX

Assume there is a group of friends `G` comprised of users `{ U1, U2, U3, ... Un}`. 

1. `U1` goes to the app website and creates a group link, probably gives it a name. `U1` shares it with everybody in their friend circle using their preferred chat platforms. `U1` is called the **admin**.
2. All in `G` go to the link, provides a user name and join a **food session**. Their location permission is asked for and we can assume that everybody provides that to begin with. Everybody is shown how many people are currently in the session.
3. All in `G` are shown a list of cuisines that they want to eat today. They can select one or more cuisines and proceed. They can also have the software select `n` number of random cuisines for them.
4. All in `G` are shown recommended restaurants which is around the middle of everybody's current location. They are also provided a search bar for restaurants. All in `G` choose one or more restaurants and submit. They can also have the software select `n` number of random restaurants for them.
6. The website takes in everybody's choices and provides a list of 1 - 3 (can be customised by the **admin**) restaurants (core of the selection algorithm). All in `G` are asked to select 1 (if more than 1 choices are given) restaurant. The restaurant with the majority vote wins and all in `G` *hopefully* go there. 

### Challenges

1. What if people join late? The middle-of-everybodys-location algorithm will break. Should we allow to notify people that somebody joined late, and do they want to reconsider their restaurant choices based on location? 
2. What if people don't like the restaurants offered as the final choice? Should we have an option to give more options? 
3. Should we give more genres of restaurants for selection - i.e. coffee shops, full fledged restaurants, fast food centers, etc? 
4. Should we completely remove step 4 and have the users only select cuisines. That way, the algorithm does most of the work, and some of the users aren't stumped after choosing a couple of restaurants (after researching through the app) only to be overriden by other users' choices. Also, if a user already provides a restuarant choice, its very likely that they will choose the same restaurant in step 6 as well, which is something we do not want. 

### Technology

1. This is a web app.
1. Node.js for the backend. 
2. Angular / React for the front-end?
