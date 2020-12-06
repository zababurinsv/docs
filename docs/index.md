#index
## Размеры экранов
  1. Десктоп
    * 1200*2607 px  
  2. Планшет
    * 768*1024 px
  3. Мобильное приложение
    * 320*568 px
## Медиа запросы
    @mixin respond-to($media) {
      @if $media == phones {
        @media only all and (max-width: 479px) { @content; }
      }
      @else if $media == wide-phones {
        @media all and (min-width: 480px) and (max-width: 767px) { @content; }
      }
      @else if $media == tablets {
        @media all and (min-width: 768px) and (max-width: 991px) { @content; }
      }
      @else if $media == small-desktops {
        @media all and (min-width: 992px) and (max-width: 1199px) { @content; }
      }
      @else if $media == lg-desktops {
        @media all and (min-width: 1200px) and (max-width: 1440px) { @content; }
      }
      @else if $media == xlg-desktops {
        @media all and (min-width: 1441px) and (max-width: 1920px) { @content; }
      }
      @else if $media == max {
        @media all and (min-width: 1920px){ @content; }
      }
    }

## Изображения
### Доска
  * Оригинал 2000*2588 px [1.294]
  * Размеры на доске
  * Размеры увеличенных картинок

## Переменные

```
:root {
  --aqua_haze: #F6F8FA
} 
```

## сторонние сервисы
  * [названия цветов](https://chir.ag/projects/name-that-color)


## Android
  * [Footer](https://zababurinsv.github.io/android/apps/footer-demo/index.json)