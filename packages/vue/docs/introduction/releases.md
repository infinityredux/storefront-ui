# Releases

## Current state of the project

Storefront UI is currently in **BETA** which means it is not suitable for production!
The package is stable but some breaking changes may occur.

Currently we are focusing on  API & component polishments and docs.

## Latest version - v0.9.1 🎉

### What is new?

:point_right: Design refreshment adjusting to current style guide [figma](https://www.figma.com/file/N0Ct95cSAoODNv7zYS01ng/Storefront-UI-Design-System?node-id=0%3A1)   

:point_right: Changes of global variables for typography

:point_right: Change of BEM modifiers for component states into seperate classes e.g. `--is-active` to `.is-active`  

:point_right: Script to pull off library components to your project 

:point_right: Two new component SfTextArea and SfAddressPicker 

:point_right: `SfDropdown` with new API - opener button added

:information_source: For more details see our `CHANGELOG.md`

## Dependencies update

### Using NPM/Yarn

You can run the following command to auto update StorefrontUI version:

```bash
yarn add @storefront-ui/vue

#OR
npm i @storefront-ui/vue
```

### Manually

Alternatively, you can also update your `package.json` by manually setting your StorefrontUI version as below:

```json
dependencies: {
    "@storefront-ui/vue": "^0.9.1"
}
```

Then run `yarn` or `npm i` to re-install your local dependencies.

## Changes

### Font family

Before | v0.8.0 | v0.9.1
------------ | ------------- | -------------
--body-font-family-primary: "Roboto", serif |   --font-family-primary: "Roboto", serif |   --font-family--primary: "Roboto", serif
--body-font-family-secondary: "Raleway", sans-serif |   --font-family-secondary: "Raleway", sans-serif |   --font-family--secondary: "Raleway", sans-serif


### Font sizes

Before | v0.6.4 |  v0.7.0 | v0.9.1
------------ | ------------ | ------------- | -------------
$font-size-extra-small-mobile: 0.625rem | undefined | --font-2xs: 0.625rem | undefined
$font-size-extra-small-desktop: 0.75rem<br>$font-size-small-mobile: 0.75rem | --font-size-extra-small: 0.75rem | --font-xs: 0.75rem | --font-size--xs: 0.75rem
$font-size-small-desktop: 0.875rem <br> $font-size-regular-mobile: 0.875rem | --font-size-small: 0.875rem | --font-sm: 0.875rem | --font-size--sm: 0.875rem
$font-size-regular-desktop: 1rem <br> $font-size-big-mobile: 1rem | --font-size-regular: 1rem | --font-base: 1rem | --font-size--base: 1rem
$font-size-big-desktop: 1.125rem <br> $font-size-extra-big-mobile: 1.125rem | --font-size-big: 1.125rem | --font-lg: 1.125rem | --font-size--lg: 1.125rem
$font-size-extra-big-desktop: 1.5rem | --font-size-extra-big: 1.5rem | --font-size--xl: 1.5rem | undefined


### Font weights

Before | v0.6.4 | v0.7.0 | v0.9.1
------------ | ------------ | ------------- | -------------
--body-font-weight-primary: 300 | --font-weight-light: 300 | --font-light: 300 | --font-weight--light: 300
--body-font-weight-secondary: 400 | --font-weight-regular: 400 | --font-normal: 400 | --font-weight--normal: 400
 - | --font-weight-bold: 500 | --font-medium: 500 | --font-weight--medium: 500
 - | --font-weight-extra-bold: 600 | --font-semibold: 600 | --font-weight--semibold: 600
 - | - | --font-bold: 700 | --font-weight--bold: 700
 - | - | --font-extra-bold: 800 | undefined
 - | - | --font-black: 900 | undefined

### Props

Component | Before | v0.9.1
------------ | ------------ | ------------
SfHeading | subtitle | description


### CSS Custom properties

Component | Before | v0.9.1
------------ | ------------ | ------------
SfHeading | --heading-subtitle-margin | --heading-description-margin
SfHeading | --heading-subtitle-color | --heading-description-color
SfHeading | --heading-subtitle-font-size | --heading-description-font-size
SfHeading | --heading-subtitle-font-family | --heading-description-font-family

### Slots

Component | Before | v0.9.1
------------ | ------------ | ------------
SfHeading | subtitle | description

## Breakpoints

v0.7.0 | v0.9.1
------------ | ------------
.mobile-only | .smartphone-only

## State classes

Before | v0.9.1 
------------ | ------------- 
--is-active |  .is-active
--is-disabled | .is-disabled
--is-current | .is-current
--has-error | .has-error
--h2 | .h2 
--h3 | .h3 
--h4 | .h4 
--h5 | .h5 
--h6 | .h6 
--has-size | .has-size
--hidden | .hidden 
--invalid | .invalid 
--has-text | .has-text 
--is-color | .is-color 
--prev | .prev
--next | .next 
--is-open | .is-open 
--is-selected | .is-selected 
--is-required | .is-required 
--open | .is-open 
--has-chevron | .has-chevron 
--has-margin | .has-margin 
--floating | .is-floating
--center | --center 
--without-carousel | .without-carousel
--without-quantity | .without-quantity
--on-wishlist | .on-wishlist 
.is-current | .current

So now we can use it like this: 

```css
.sf-component {
  .is-active {
    /*css stylings*/
  }
}
```

instead of 

```css
.sf-component {
  &--is-active {
    /*css stylings*/
  }
}
```

This change follows [css guideline](https://github.com/chris-pearce/css-guidelines#state-hooks).

## Others

  1. `SfRating` allows fractional rate.
  2. `SfHeading` wrapped in `div`.
  3. `SfSearchbar` button added on loupe icon so it is now active. 
  4. `SfSelect` scrollbar added to the native element.
  5. Add `SfButtons` to `SfStoreLocator` to wrap whole store component and make it clickable.
  6. `SfProductCard` with price range
  7. `SfLink` change default colors to `--c-text`, `--c-primary` (in hover state) and `--c-link` (in active and visited states)

<!-- ### Deletions
 -->

## Additions

### Components

  1. `SfTextArea`
  2. `SfAddressPicker`

### Props

Component | Before | v0.9.1
------------ | ------------ | ------------
SfIcon | - | coverage 
SfRating | - | icon 

### Slots

Component | Before | v0.9.1 | Info
------------ | ------------ | ------------ | ------------
SfDropdown | - | opener

### Components with data-testid

Before | v0.9.1
------------ | ------------
- | SfBreadcrumbs
- | SfBullets
- | SfCheckbox
- | SfColor
- | SfInput
- | SfQuantitySelector
- | SfMenuItem
- | SfHeader

<!-- ## Release notes -->
