# SCSS Mixin Media Breakpoints

A package for integrating a mixin for creating media queries.

![npm](https://img.shields.io/npm/v/@m2collective/scss-mixin-media-breakpoints?style=for-the-badge)

___

## Installation

You can install the package automatically using NPM:

```
npm i @m2collective/scss-mixin-media-breakpoints
```

## Usage

To use the package, import it into your project:

### Media Breakpoint Min

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as *;

.demo {
    @include media-breakpoint-min(480px) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-min(480px) {
        background-color: #000
    };
}

// Return

@media (width >= 480px){
    .demo {
        background-color: #000
    }
}
```

### Media Breakpoint Max

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as *;

.demo {
    @include media-breakpoint-max(xxs) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-max(480px) {
        background-color: #000
    };
}

// Return

@media (width <= 479px) {
    .demo {
        background-color: #000;
    }
}
```

### MediaBreakpointMinMax

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as *;

.demo {
    @include media-breakpoint-min(xxs, xs) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-min(480px, 640px) {
        background-color: #000
    };
}

// Return

@media (width >= 480px) and (width <= 639px) {
    .demo {
        background-color: #000
    }
}
```

## Mixins

The package contains the following mixins to use:

| Name                     | Variables                                   |
|--------------------------|---------------------------------------------|
| media-breakpoint-min     | breakpoint-min, rem-default                 |
| media-breakpoint-max     | breakpoint-max, rem-default                 |
| media-breakpoint-min-max | breakpoint-min, breakpoint-max, rem-default |

`brekpoint-min`, `breakpoint-max`: it can take the following values: xxs, xs, sm, md, lg, xl, xxl.

`breakpoint-baseline`: takes the value when converting `px` to `rem`, the default value is set to 16px.

## Changing the namespace

You can change the namespace during mixin import and use the mixin with a different namespace:

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as mixin;
```

## Changing the variables

You can redefine the default values for the specified variables when importing the mixin:

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as * with (
    $breakpoint-xxs: 480px,
    $breakpoint-xs: 640px,
    $breakpoint-sm: 768px,
    $breakpoint-md: 1024px,
    $breakpoint-lg: 1280px,
    $breakpoint-xl: 1440px,
    $breakpoint-xxl: 1536px,
    $rem-default: 16,
);
```

## Dependencies

* [@m2collective/scss-function-rem](https://github.com/m2collective/scss-function-rem)

## License

The MIT License (MIT). Please see the [License file](LICENSE.txt) for more information.
