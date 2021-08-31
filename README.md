# Designware tech test

## Code fixes and suggestions

### CSS (SASS) Fixes:

.btn class

- Replace `flex-flow: row wrap` with `flex-flow: row nowrap` to avoid button svg and span elements from wrapping
- Replace `align-items: middle` with `align-items: center` as middle is not a valid value for the `align-items` css property
- Replace `padding: 5px 15px 10px 10px` with `padding: 10px 15px 10px 10px` to match Target Outcome's spacing requirements
- Add `outline: none` as there is no outline that appears in the Target Outcome when it is in focus
- Add `transition: 0.2s all` to provide a smoother transition on hover that is consistent with all the child elements
- Remove `transition: 0.2s all` from the hover state as it was suggested to be included in the `.btn` class (see above), making it redundant here

svg element

- Add `margin-right: 10px` to match Target Outcome's spacing requirements

### CSS (SASS) Suggestions:

.btn class

- To keep the code DRY, convert `background: #3d3f42`, `background: #515357` and `background: #d1d1d2` into a SASS variable if they will be used multiple times in the larger code base
- Add `focus` states, similar to `hover` states to provide keyboard users with some visual feedback given `outline` property was removed from `.btn`. Although the Target Outcome does not have styles for a focus state, this is highly recommended to ensure keyboard users have a consistent user experience to all other users

### HTML fixes:

button element

- Add a `type="button"` attribute on the button element to inform browsers of the type of button this is. Recommended by W3 schools article [here](https://www.w3schools.com/tags/tag_button.asp).

## Get started for developers

- Run `npm i pug-cli -g` to install pug command line interface globally. Can exclude `-g` flag if you do not wish to install this globally
- Run `pug -w ./ -o ./html -P` to watch for changes made to the .pug file and automatically generate a pretty version of the html file
