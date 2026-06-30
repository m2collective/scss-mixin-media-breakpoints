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

```scss
@use "@m2collective/scss-mixin-media-breakpoints" as *;
```

### Media Breakpoint Min

```scss
.demo {
    @include media-breakpoint-min(xxs) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-min(480px) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-min-xxs {
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

* media-breakpoint-min-xxs: 480px
* media-breakpoint-min-xs: 640px
* media-breakpoint-min-sm: 768px
* media-breakpoint-min-md: 1024px
* media-breakpoint-min-lg: 1280px
* media-breakpoint-min-xl: 1440px
* media-breakpoint-min-xxl: 1536px

### Media Breakpoint Max

```scss
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

or

.demo {
    @include media-breakpoint-max-xxs {
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

* media-breakpoint-max-xxs: 479px
* media-breakpoint-max-xs: 639px
* media-breakpoint-max-sm: 767px
* media-breakpoint-max-md: 1023px
* media-breakpoint-max-lg: 1279px
* media-breakpoint-max-xl: 1439px
* media-breakpoint-max-xxl: 1535px

### Media Breakpoint Min Max

```scss
.demo {
    @include media-breakpoint-min-max(xxs, xs) {
        background-color: #000
    };
}

or

.demo {
    @include media-breakpoint-min-max(480px, 640px) {
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
);
```

## License

The MIT License (MIT). Please see the [License file](LICENSE.txt) for more information.
