The app is an interactive daily planner which uses local storage to store user to-do list inputs and hold those items in storage until the user marks them complete. The app is linked to the moment.js API in order to keep the time and date accurate, and uses the API to colour code the segments of the day, with green segments in the future, grey in the past and red highlighting the current segment of the day. 

The app uses the same logic for all nine segments of the day. It has the following functions:
1.	init(number of segment).  This function pulls the to-do items from local storage and parses them to a new variable, and then into the array relevant for that segment. 

2.	Render(number of segment). This function renders to the to-do list by looping over the array relevant to that segment.

3.	Store(number of segment).  The function takes user input (stringifying the input as local storage can only accept strings) and stores it in local storage when the “save” button is pressed.
Each to-do item is rendered with a “complete” button that has an event listener. When clicked, the event listener looks to the relevant data index and removes it from the list. The store and render functions are called again to re-render the updated list. The stored to-do lists should remain even when the browser is refreshed, as they remain in local storage unless they are removed by clicking the “complete” button.  

In order to colour-code the segments, I have created a loop over all “a” elements in the document, checking for an element IDs which match the current hour (from moment.js). Each segment has been allocated an ID which matches it’s hour (09,10,11,12,13,14,15,16,17). Background colour are changed depending on whether they are in the past, present or future.

https://andrewmiddleton1.github.io/Bootcamp-Homework-Week-5/
