##jspsych-visualize-results plugin

The visualize-results plugin is useful for creating a visualization of the results from a quiz. It takes in the user's score and the total score and creates a graphic representation of the results.

###Parameters

The following table lists the parameters associated with this plugin. Parameters with the default value of *undefined* must be specified. 

| Parameter| Type| Default Value| Description|
| ---------|:---:|:------------:|:-----------|
|participant_score|integer|*undefined*|The score for the user taking the quiz (can use a function that returns the score). 
|possible_score|integer|*undefined*|The total possible score for the quiz.

###Data Generated
This plugin is used for visualization of the results only. It does not collect any data.

###Example
Code:

```
var participant_score = {
  type:"visualize-results",
  participant_score: 7,
  possible_score: 32

};

```
Visualization:

![logo](https://github.com/marielajennings/jsPsych-visualize-results/raw/master/example.png)