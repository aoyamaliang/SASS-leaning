# SASS-leaning
#### SASS
```SCSS
顏色管理：
使用範例：background-color: color(primary);

$colors: (
    primary:#005DFF,
    primary-light: lighten(#005DFF, 40%),
    primary-dark: darken(#005DFF, 40%),
    accent: #FFF6BB
);

@function color($color-name) {
    @return map-get($colors, $color-name)
}

$padding:15px;
$borders: 15px;


ＲＷＤ設定：
使用範例：
@include desktop{
  display: grid;
  ..
  ..
  }
  
$desktop: 840px;

@mixin desktop {
    @media (min-width: #{$desktop}){
        @content;
    }
}
