
## Chapter 7: “Forms” (pp.144-175)

#### Adding Text:
* Text Input - single line
* Password Input
* Text Area - multi line

#### Making Choices:
* Radio buttons
* Checkboxes
* Drop-down boxes

#### Submit choices
* Submit button
* Image button
* File upload 

Forms need an action to say where the data goes.

Then

`<input type='type - see above' name='name attribute' size='size of box' maxlength='number of characters'/>`

For radio and checkbox you will need one of the above for each selection.

`<fieldset>` can be used to group control elements together.

can use `required='required'` to well ... make filling it out a requirement.

## Chapter 14: “Lists, Tables & Forms” (pp.330-357)
From the Duckett JS book:

`list-style-image` seems fun.

`empty-cells: hide;` will hide the borders of empty cells.

## Chapter 6: “Events” (pp.243-292)

There are A LOT of different event types.

UI EVENTS

KEYBOARD EVENTS

MOUSE EVENTS

Events trigger a function or a script.

Event Handeling:
1 SELECT ELEMENT - Select the element you want the script to respond to
2 SPECIFY EVENT - Indicate which event on the selected node will trigger the response (referred to as 'binding').
3 CALL CODE - Start the code you want to run when the event occurs.

DOM level 2 event handelers are the way to go.

Event Bubbling vs Event Capturing
https://javascript.info/bubbling-and-capturing



