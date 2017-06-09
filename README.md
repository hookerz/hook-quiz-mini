[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)

## hook-quiz-mini

### Description

`hook-quiz-mini` is a quiz element built with Polymer 2.0. The component features transitions and animations powered by the Web Animations API.

### Install
Install the `hook-quiz-mini` element using [Bower](https://bower.io/):

```sh
bower install --save https://github.com/hookerz/hook-quiz-mini
```

**Note**: For full browser compatibility, also add the [Web Animations polyfill](https://cdnjs.com/libraries/web-animations):

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/web-animations/2.2.5/web-animations.min.js"></script>
```

### Example

<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/3.0.3/normalize.min.css" type="text/css">
    <link rel="import" href="hook-quiz-mini.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
 -->

```html
<dom-bind>
  <template>
    <hook-quiz-mini questions="[[questions]]"></hook-quiz-mini>
  </template>
</dom-bind>

<script>
  var domBind = document.querySelector('dom-bind');

  domBind.questions = [
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
    {
      "text": "Six or twenty-seven?",
      "choices": [
        {"text": "Six", "correct": true},
        {"text": "Twenty-seven", "correct": false}
      ]
    }
  ];
</script>    
```

### Styling

The following custom properties and mixins are available for styling in `hook-quiz-mini.html`:

| Custom property                    | Description                           | Default                  |
| ---------------------------------- | ------------------------------------- | ------------------------ |
| `--hook-quiz-progress-bar-color`   | The hook-quiz-mini progress bar color | `#ff0050`                |
| `--hook-quiz-ripple-color`         | The hook-quiz-mini ripple color       | `rgba(255, 0, 80, .5)`   |
| `--hook-quiz-choice-checked-color` | The hook-quiz-mini radio button color | `#ff0050`                |
| `--hook-quiz-button-color`         | The hook-quiz-mini button color       | `#ff0050`                |
| `--hook-quiz-button-text-color`    | The hook-quiz-mini button text color  | `#fff`                   |

### Attributes

| Attribute name      | Description                           | Type   | Default    |
| ------------------- | ------------------------------------- | ------ | ---------- |
| `question`          | Current quiz question                 | Object | {}         |
| `questions`         | All quiz questions                    | Array  | []         |
| `currentQuestion`   | Index of current quiz question        | Number | 0          |
| `totalQuestions`    | Number of questions in the quiz       | Number | null       |
| `answers`           | Correct answers to the quiz questions | Array  | []         |
| `response`          | Answer chosen for current question    | String | ""         |
| `responses`         | All answers chosen                    | Array  | []         |
| `score`             | Quiz score                            | Number | 0          |

### Methods

| Method name            | Description                        |
| ---------------------- | ---------------------------------- |
| getNextQuestion        | Gets the next quiz question        |  
