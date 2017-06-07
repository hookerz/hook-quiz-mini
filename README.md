# \<hook-quiz-mini\>


`<hook-quiz-mini>` is a mini quiz element built with Polymer 2.0. The component features transitions and animations powered by the Web Animations API.

## Demo

[https://hookerz.github.io/hook-quiz-mini/](https://hookerz.github.io/hook-quiz-mini/)

## Installation

`bower install https://github.com/hookerz/hook-quiz-mini`


## Usage

Include the quiz element in your webpage.

```
<link rel="import" href="path/to/hook-quiz-mini.html">

...

<hook-quiz-mini></hook-quiz-mini>
```

Select the quiz element.

```
const el = document.querySelector('hook-quiz-mini');
```

To populate the quiz, create a `questions` property on the quiz element and create an array of question objects. 

Each question object should contain a `text` property and a `choices` property. 

The `choices` property should contain an array of objects specifying the choice `text` and a `correct` property indicating the right answer to the question.

```
el.questions = [
	{
    	"text": "Cat or dog?",
        "choices": [
        	{"text": "Cat", "correct": true},
            {"text": "Dog", "correct": false}
        ]
    },
    {
        "text": "Chicken or fish?",
        "choices": [
          {"text": "Chicken", "correct": false},
          {"text": "Fish", "correct": true}
        ]
     },
    ...
];

```

### Options

You can customize the llook of the quiz by editing the color values in corresponding mixin properties:

**progress bar color**  
Can be any color format

Example:  
```
:host {
	--hook-quiz-progress-bar-color: #ff0050;
}
```

**ripple color**  
Can be any color format

Example:  
```
:host {
	--hook-quiz-ripple-color: rgba(255, 0, 80, .5);
}
```

**radio button color**  
Can be any color format

Example:  
```
:host {
	--hook-quiz-choice-checked-color: #ff0050;
}
```

**reset button color**  
Can be any color format

Example:  
```
:host {
	--hook-quiz-button-color: #ff0050;
}
```

**reset button text color**  
Can be any color format

Example:  
```
:host {
	--hook-quiz-button-text-color: #fff;
}
```


