# SCCS

### Function for adding alfa-channel (opacity) to your existing colors

Define the next function in "mixins.scss" or "functions.scss"

```scss
@function colorWithAlfa($color, $opacity: 1, $important: '') {
  $rgba-color: rgba(color, $opacity);

  @if $important == '!important' {
    @return $rgba-color !important;
  } @else {
    @return $rgba-color;
  }
}
``` 

Use it in the next way in your styles file, like "Header.module.scss"
```scss
@import '../../styles/variables.scss';
@import '../../styles/mixins.scss';  // or import 'functions.scss'; 

elementSelector {
	background: colorWithAlfa($Neutral-Grey-blue, 0.5, '!important');
}
```