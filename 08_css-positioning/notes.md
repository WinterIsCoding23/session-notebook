position: relative;
--> element relative to its position on the page
--> allows to determine more options, e.g. "left: 20px" (also: top, right, bottom) 
    --> meaning: moving element 20px TO the left
--> no effect on the other elements on the page

position: absolute;
--> outside of the flow of the page/container
--> positioning according to the page

To move an element INSIDE a parent-container to a specific position make the container relative (the absolute element always "searches" for the next relative parent)
If there is none, it orientates itself on the page

position: fixed;
--> element taken out of the flow (similar to "absolute")
--> positioning possible with top, right, bottom, left (e.g. "top: 10px"; right: 10px;), also possible with "%" (adapts to window-size)

Example:
position: fixed;
left: 10px;
right: 10px;
--> element is stretched to to 10px to left and right

href="#"
--> anchors element to the top

href="#[id]"
--> anchors element to the id (only works with id)

z-index
--> indicates position of an element on the z-axis (depth)
--> only works when a position is indicated (NOT with static objects)
--> bring image/element to the back-/fore-ground

position: sticky
top: 0;
-> when scrolling down the element sticks to the top (when top:50px -> stops when at 50px from the top)

[copy code-lines in VC Code: alt + shift + arrow up/down -> copies on top/bottom of the marked lines]

Github-Trick:
Press "." when looking at any code -> VC Code opens