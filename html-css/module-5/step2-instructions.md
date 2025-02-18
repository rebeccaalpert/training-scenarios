## Override Patternfly variables to achieve a new theme

Now that we have a card on our page, let's customize some of the styles applied to it.

1) <strong>Add a new color variable to use in the card.</strong> In PatternFly, all the css values we use are first assigned to variables. We recommend doing the same when making customizations in your application.

In `myapp.scss` make a new variable name called `--my-app-card-theme--Color` and assign it to be purple: `#6200EE`.

<strong>Hint:</strong> `--my-app-card-theme--Color: #6200EE;`

2) <strong>Override the global link color. </strong> In our current example of the card, the buttons in the card footer use the global link color. We can reassign the global link color variable to use our new custom color variable, so that all properties that use the global link color variable in the card will now use this color.

On line 4 of `myapp.scss` set the global variable `--pf-global--link--Color` to use the value defined in the custom variable `--my-app-card-theme--Color`. 

<strong>Hint:</strong> `--pf-global--link--Color: var(--my-app-card-theme--Color);`

<strong>Note:</strong> Variable definitions declared for a component `.pf-c-` class selector are scoped to that component. So even though we are assigning a new value to the global variable, that value will only apply to the Card component, and not other components.

3) <strong>Change the font-size of the title in the card header.</strong> Not all changes require custom css. Many components include modifier classes that enable you to customize the appearance of a component. For this update, we'll use a modifier class available for the Title component. 

Search in `index.html` for `<div class="pf-c-card__header pf-c-title pf-m-md">`. Replace `pf-m-md` with `pf-m-xl`.

<strong>Hint:</strong> `<div class="pf-c-card__header pf-c-title pf-m-xl">`

Remember to click the <strong>Reload</strong> button above the preview panel to see how the styles change after you make updates.