##custom-image-drag-response plugin

The custom-image-drag-response plugin allows the user to drag an image and drop it on another image (Mickey or trash). The latter image makes a sound upon drop. Data is recorded based on the image where the drop even occurs. This plugin was developed for the Sorting Task. This plugin is based on jspsych-image-button-response.


###Parameters

The following table lists the parameters associated with this plugin. Parameters with the default value of *undefined* must be specified. 

| Parameter| Type| Default Value| Description|
| ---------|:---:|:------------:|:-----------|
|stimulus|image|*undefined*| Provides a path to the image that can be dragged.
|prompt|string|*empty string*|A prompt for the participant.
|margin_vertical|string|*0px*| The vertical margin of the image button.
|required|boolean|*null*|A boolean value. Indicates if a question is required (true) or not (false), using the HTML5 required attribute.  If this parameter is undefined, all questions will be optional.
|margin_horizontal|string|*8px*| The horizontal margin of the image button.
|mickey_audio|string|*undefined*|'This is the sound played when the Mickey button is pressed!'
|trash_audio|string|*undefined*|'This is the sound played when the trash button is pressed!'
|button_html|string|'<button class="jspsych-btn">%choice%</button>'|The html of the button. Can create own style. We use it to make the buttons look like Mickey and trash.
###Data Generated


| Name| Type|  Value| 
| ---------|:---:|:-----------|
| button_pressed|string|"MICKEY" or "TRASH"

###Example

```
var practice2b = {
		type: 'image-drag-response',
		stimulus: '/static/images/pre-test/pre-test_2.jpg',
		choices: ['MICKEY', 'TRASH'],
		button_html: ['<button class="jspsych-btn"><img src="/static/images/mickey.jpg" style="width:125px;height:175px;"></button>', '<button class="jspsych-btn"><img src="/static/images/trash.jpg" style="width:125px;height:175px;"></button>'],
		margin_vertical: '0px',
		margin_horizontal: '75px',
		prompt: '<p>Give Mickey all of the triangles!</p>',
		mickey_audio: '/static/audio/mickey.wav',
		trash_audio: '/static/audio/trash.wav'
	}


```
