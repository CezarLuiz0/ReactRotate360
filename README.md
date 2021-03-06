# ReactRotate360

ReactRotate360 is a plugin to create 360 degree showcases. Inspired on Apple iPhone 360 showcase.

Made with React and HTML5.

Works with videos or images.

## Examples

To build the examples locally, run:

```
npm install
gulp dev
```

Then open [`localhost:8000`](http://localhost:8000) in a browser.

#### Video GIF Demo
![Video GIF Demo](https://cloud.githubusercontent.com/assets/954889/6597746/620753ee-c7dd-11e4-9817-34163b62f390.gif)

#### Images GIF Demo
![Image GID Demo](https://cloud.githubusercontent.com/assets/954889/6597759/7b916930-c7dd-11e4-8046-e4f5385123d8.gif)


## Usage

The plugin uses `input[type=range]` for the slide. You can check the [support here](http://caniuse.com/#feat=input-range).

#### Videos

You can use this plugin with videos (mp4, ogg or webm).

```
var sources = [
  'path/to/videos/video.mp4',
  'path/to/videos/video.oggtheora.ogv',
  'path/to/videos/video.webmhd.webm'
];

React.render(<Rotate src={sources} />, document.querySelector('#video'));
```


#### Images
```
// Render images
React.render(<Rotate type="image" path="examples/images" ext="png" total="43" />, document.querySelector('#images'));
```

#### CSS Classes
```
.rotate-box { }
.rotate-video { }
.rotate-image { }
.rotate-range { } /* For input[type=range] */
.rotate-range::-webkit-slider-thumb { }
```

## Documentation

Attribute | Type | Use with? | Default | Description
--- | --- | --- | --- | --- |
`src` | `array` | video | - | Pass an array with your videos path. The plugin will create the `<source>` tags.
`type` | `string` | both | video | Use `video` or `image`
`path` | `string` | image | - | Pass the path of your images. The images need follow a sequence. The first image need start with 1. e.g: 1.png, 2.png, 3.png ... 30.png
`ext` | `string` | image | `jpg` | The extension of your images.
`total` | `string` or `int` | image | - | Pass the quantity of your images.

## Browser Support

![IE](https://cloud.githubusercontent.com/assets/398893/3528325/20373e76-078e-11e4-8e3a-1cb86cf506f0.png) | ![Chrome](https://cloud.githubusercontent.com/assets/398893/3528328/23bc7bc4-078e-11e4-8752-ba2809bf5cce.png) | ![Firefox](https://cloud.githubusercontent.com/assets/398893/3528329/26283ab0-078e-11e4-84d4-db2cf1009953.png) | ![Opera](https://cloud.githubusercontent.com/assets/398893/3528330/27ec9fa8-078e-11e4-95cb-709fd11dac16.png) | ![Safari](https://cloud.githubusercontent.com/assets/398893/3528331/29df8618-078e-11e4-8e3e-ed8ac738693f.png)
--- | --- | --- | --- | --- |
IE 10+ ✔ | Latest ✔ | Latest ✔ | Images ✔ Videos :( | Latest ✔ |

#### On mobile, use only images.

### License

No license. Use as you wish.

Copyright (c) 2015 Cezar Luiz.