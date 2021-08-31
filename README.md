# Designware tech test

## Code fixes and suggestions

### CSS (SASS) fixes:

btn class selector

- Replace `flex-flow: row wrap` with `flex-flow: row nowrap` to prevent child elements from wrapping
- Replace `align-items: middle` with `align-items: center` as middle is not a valid value
- Replace `padding: 5px 15px 10px 10px` with `padding: 10px 15px 10px 10px` to match Target Outcome's spacing requirements
- Add `outline: none` as there is no outline that appears in the Target Outcome when it is in focus
- Add `transition: 0.2s all` to provide a transition consistent with all child elements
- Remove `transition: 0.2s all` from the hover state as it is suggested to be included in the `btn` class (see above), making it redundant here

svg element selector

- Add `margin-right: 10px` to match Target Outcome's spacing requirements

### CSS (SASS) suggestions:

btn class selector

- To keep the code DRY, convert `background: #3d3f42`, `background: #515357` and `background: #d1d1d2` into SASS variables if they are expected to be used elsewhere in the code base
- Although the Target Outcome does not have styles for a `focus` state, it is highly recommended to have styles for this state given `outline: none` was added to the `btn` class. This is so keyboard users have a consistent user experience to all other users.

### HTML fixes:

button element

- As recommended by the W3 schools article [here](https://www.w3schools.com/tags/tag_button.asp), add the `type="button"` attribute to inform browsers of the type of button this is.

## Get started for developers

- Run `npm i pug-cli -g` to install pug command line interface globally. Can exclude `-g` flag if you do not wish to install this globally
- Run `pug -w ./ -o ./html -P` to watch for changes made to the .pug file and automatically generate a pretty version of the html file
