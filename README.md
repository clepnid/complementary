<h1 align="center">Complementary</h1>

<p align="center">Visual Component, Transform your images with dynamic styling and fluid animations</p>

_Live Example Demo: https://complementary-demo.vercel.app/_

## Features

- Dynamic color palette
- Animations
- FPS

## Install

    $ npm i complementaryimage

## Quickstart

#### ComplementaryImage Component

```jsx
import React from 'react'
import ComplementaryImage from 'complementaryimage';

export default () => (
  <>
    <ComplementaryImage
        imageSrc='https://interactive-examples.mdn.mozilla.net/media/cc0-images/grapefruit-slice-332-332.jpg'
        isHorizontal={true}
        colors={[]}
        colorsChange={[]}
        colorScheme={'triadic'}
        opacityColor={false}
        invert={false}
        fps={60}
        boomerang={false}
        cyclic={false}
        isEditable={false}
        maxWidthImage={'100%'}
        maxheightImage={'100'}
        animation={'none'}
    />
  </>
)
```

#### Props

| **Prop**                        | **Type**           | **Default**               | **Description**                                                    |
|---------------------------------|--------------------|---------------------------|--------------------------------------------------------------------|
| imageSrc _(required)_  | `string`          | -                         | Image source. It can be url or base64                                              |
| isHorizontal                  | `boolean`         | true                | Change the symetry orientation                                              |
| colors                | `Array<string>`    | [] | Array of colors, example: ['#ffff00', '#ffffff']         |
| colorsChange                      | `Array<ColorChange>`    | []                 | Array of colors that change the original image, (see [ColorChange](#colorChange))                                 |
| opacityColor                  | `boolean`         | false                | Change the opacity color change                                                     |
| invert                  | `boolean`         | false                | Change the animation start color                                                   |
| boomerang                  | `boolean`         | false                | Change the animation states                                               |
| cyclic                  | `boolean`         | false                | Change the animation cycle                                                   |
| isEditable                  | `boolean`         | false                | Enabled change animation and refresh                                                  |
| animation                  | `string`         | 'none'                | Change the animation: 'none', 'circle', 'rectangle', 'square', 'blinds',  'randomPoligon',  'spiral', 'diagonal'                                 |
| maxWidthImage                 | `string`           | '100%'                         | Width of image                                          |
| maxheightImage                 | `string`           | '100%'                         | Height of image            |


## Types

#### ColorChange

```jsx
interface ColorChange {
  color1?: string;
  color2?: string;
  tolerance?: number; 
}
```

| **Prop**   | **Type**     | **Default** | **Description**                                                                                       |
|------------|--------------|-------------|-------------------------------------------------------------------------------------------------------|
| color1     | `string`     | ''          | hex color of original image                                                               |
| color2     | `string`     | ''          | hex color of change            |
| tolerance | `number`     | 1           | Integer that sets the tolerance of change: 1 to 255 |


## License

This project is licensed under the MIT license, Copyright (c) 2023 <a href="https://effectussoftware.com">Effectus Software</a>. [[License](LICENSE)]

## Author
_Pavon: https://pavon00-port-folio.vercel.app/_
