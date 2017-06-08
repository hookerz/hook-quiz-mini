[*Demo*](https://hookerz.github.io/hook-quiz-mini/)

## \<hook-quiz-mini\>


`hook-quiz-mini` is a quiz element built with Polymer 2.0. The component features transitions and animations powered by the Web Animations API.


Install the `hook-quiz-mini` element using [Bower](https://bower.io/):

`bower install https://github.com/hookerz/hook-quiz-mini`

Import the `hook-quiz-mini` element into your project.

**Note**: For full browser compatibility, also add the [Web Animations polyfill](https://cdnjs.com/libraries/web-animations):

Example:

```
<link rel="import" href="path/to/hook-quiz-mini.html">

<script src="https://cdnjs.cloudflare.com/ajax/libs/web-animations/2.2.5/web-animations.min.js"></script>
```
Include the `hook-quiz-mini` element in your project. Wrap the quiz element in `dom-bind` and `template` tags. On the quiz element, add a `questions` attribute.

Example:

```
<dom-bind>
  <template>
  <hook-quiz-mini questions="[[questions]]"></hook-quiz-mini>
  </template>
</dom-bind>
```

Select the `dom-bind` element.

Create a `questions` property on the `dom-bind` element populated with an array of question objects. 

Each question object should contain a `text` property and a `choices` property. 

The `choices` property should contain an array of objects specifying the choice `text` and a `correct` property indicating the right answer:

Example:

```
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
  ...
];

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


