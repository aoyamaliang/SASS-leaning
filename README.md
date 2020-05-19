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
@mixin 可以把常用的語法蒐集起來，需要該語法時再插入 ＠include + 語法名稱 簡化重複性估作
//建立
@mixin + 名稱 { 語法內容 }
//插入
@include + 名稱 ;
  
$desktop: 840px;

@mixin desktop {
    @media (min-width: #{$desktop}){
        @content;
    }
}
