# CSS

毛哥EM

---

## CSS 簡介

主要功能:美觀網站

![](img/CSS/骨架、外觀、行為.png) <!-- .element: height="400px" -->

---
<!-- .slide: data-auto-animate -->
## 範例 <!-- .element: style="color:red;" -->

```css
h1 {
    color: red;
}
```

---
<!-- .slide: data-auto-animate -->
## 一個 CSS 宣告包含


```css
h1 {
    color: red;
}
```

-   selector: 選擇器 (對象)
-   declaration: 宣告
-   property: 屬性 (要改的東西)
-   value: 屬性值

---

## 寫在哪裡?

-   在 HTML 建立 `<style>` 裡面 (通常放在 `<head>` 裡面)
-   創一個 CSS 檔案，並連結到 HTML(link)

```html
<link rel="stylesheet" type="text/css" href="style.css" />
```

---

```html" data-line-numbers="3,12|7-11|14
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        h1{
            color: red;
        }
    </style>
</head>
<body>
    <h1>標題</h1>
</body>
</html>
```

---

## 選取器

1. `.` - class 選擇器
2. `#` - id 選擇器
3. `*` - 全部選擇器

---

## 文字

<div style="display:flex;">
<div style="font-size:1.5rem;flex:1;">

-   `color`:顏色
-   `font-size`:字體大小
-   `letter-spacing`:字距
-   `line-height`:行高
-   `font-weight`:字體粗細
-   `text-decoration`: 文字裝飾
-   `font-style`:字型
-   `opacity`:透明度
-   `text-align`:文字位置
-   `font-family`:字體

</div>
<div style="flex:1;">

```css
color: #fff;
font-size: 10px;
letter-spacing: 2;
line-height: 20px;
font-weight: 500;
text-decoration: none;
font-style: italic;
opacity: 0.5;
text-align: left;
font-family: 微軟正黑體;
```

</div>
</div>

--

## 文字粗細 font-weight

### 關鍵字

```css" data-line-numbers="|1,2
font-weight: normal; /* 正常 */
font-weight: bold; /* 粗 */
font-weight: lighter; /* 細一點 */
font-weight: bolder; /* 粗一點 */
```

### 絕對的數值

```css data-line-numbers="|2,3
font-weight: 100;
font-weight: 400; /* 正常 */
font-weight: 700; /* 粗體 */
font-weight: 900;
```

--

## text-decoration

常用於消除[超連結]()的藍色底線

```css" data-line-numbers="|3
text-decoration: underline; /* 底線 */
text-decoration: overline red; /* 劃過的線 */
text-decoration: none; /* 不要 */
text-decoration-color: #ff00ff; /* 線顏色 */
```

---

## 背景圖片

```css
background-image: url(./image/cloud.png); /* 背景圖片 */
background-repeat: no-repeat; /* 背景重複 */
background-size: cover; /* 不管有沒有全部進去，反正就是塞滿 */
background-size: contain; /* 全部塞進去 */
```

```css
background-position: top left;
background-position: 20% 40%; /*從左上開始算*/
```

--

<div style="display: flex;">
<div style="flex:1;font-size:1rem">

`background-size: contain;`

<video style="width:100%;height:300px;border:2px solid #FFF" data-autoplay loop src="img/CSS/long.webp"></video></div>

<div style="flex:1;font-size:1rem">

`background-size: cover;`

<video style="width:100%;height:300px;border:2px solid #FFF;object-fit: cover;object-position: top;" data-autoplay loop src="img/CSS/long.webp"></video></div>

</div>

---

## 色色

-   顏色名稱 - `red`
-   RGB/RGBA - `rgb(255,0,0)`, `rgba(255,0,0,0.5)`
-   HEX - `#ff0000`
-   HSL - `hsl(0,100%,50%)`

--

### RGB/RGBA

<span style=color:red>R</span>,<span style=color:green>G</span>,<span style=color:blue>R</span> 參數範圍為 0 ~ 255  
alpha 不透明介於 0 ~ 1 之間

```css
範例: 半透明紫色 rgba(160, 32, 240, 0.5);
```

--

### HEX

十六進位（hexadecimal

# #<span style=color:red>XX</span><span style=color:green>XX</span><span style=color:blue>XX</span>

-   黑色: `#000000`
-   白色: `#ffffff`

--

### HSL

<!-- .slide: data-auto-animate -->

-   H : hue 色相 (0 是紅色 120 是綠色 240 是藍色)
-   S : saturation 飽和度
-   L : lightness 明度

```css
color: hsl(0, 100%, 50%);
```

--

<!-- .slide: data-auto-animate -->

### HSL

hue 色相 (0 是紅色 120 是綠色 240 是藍色) <!-- .element: style="color:hsl(var(--hhh), 100%, 50%)!important;" -->

<div data-id="hsl" style="background:linear-gradient(90deg,red,orange,yellow,green,blue,indigo,violet);height:100px"></div>
<input type="range" min="1" max="360" value="0" oninput="document.documentElement.style.setProperty('--hhh', this.value)" />

--

<!-- .slide: data-auto-animate -->

### HSL

S : saturation 飽和度

<div  data-id="hsl" style="background:linear-gradient(90deg,hsl(0,100%,50%),hsl(0,50%,50%),hsl(0,0%,50%));height:100px"></div>

--

### HSL

<!-- .slide: data-auto-animate data-transition="zoom" -->

L : lightness 明度

<div  data-id="hsl" style="background:linear-gradient(90deg,hsl(0,100%,100%),hsl(0,100%,50%),hsl(0,100%,0%));height:100px"></div>

--

#### 套用到文字

```css
color: hsl(0, 100%, 50%);
```

#### 套用到背景

```css
background-color: hsl(0, 100%, 50%);
```

---

## 單位

-   px
-   em
-   rem
-   vw/vh
-   %

--

<!-- .slide: data-transition="convex" -->

### px

相對顯示器的解析度，為絕對單位(pixel)

--

<!-- .slide: data-transition="convex" -->

### em

相對父元素的 m 寬度(預設 16px)

--

<!-- .slide: data-transition="convex" -->

### rem

相對根元素的 m 寬度(預設 16px)

--

<!-- .slide: data-transition="convex" -->

### vw/vh

viewport（視口）寬/長度

--

<!-- .slide: data-transition="convex" -->

### %

1. width 跟 height 的%基準是父層
2. line-height 以本身文字行高為基準

---

## 間距

<!-- .slide: data-background-image="img/CSS/toilet.webp" data-background-opacity="0.4" -->

--

<!-- .slide: data-auto-animate -->

<div style="display:flex;">
<div style="flex:1;">

### margin

margin 是指物件與物件之間的距離，通常用來調整物件之間的間距。

</div>
<div style="flex:1;">

<div data-id="box1" style="background-color:#40a3e7;width:300px;height:100px;margin:0px auto;"></div>
<div data-id="box2" style="background-color:#40a3e7;width:300px;height:100px;margin:0px auto;"></div>

```html
<div></div>
<div></div>
```

</div>
</div>

--

<!-- .slide: data-auto-animate -->
<div style="display:flex;">
<div style="flex:1;">

### margin

margin 是指物件與物件之間的距離，通常用來調整物件之間的間距。

</div>
<div style="flex:1;">

<div data-id="box1" style="background-color:#40a3e7;width:300px;height:100px;margin:10px auto;font-size:1rem;box-sizing:border-box;"></div>
<div data-id="box2" style="background-color:#40a3e7;width:300px;height:100px;margin:10px auto;font-size:1rem;box-sizing:border-box;"></div>

```css
margin: 10px; /* 四邊 */
margin: 10px 20px; /* 上下 左右 */
margin: 10px 20px 30px 40px; /* 上右下左 */
```

</div>
</div>

--

<!-- .slide: data-auto-animate -->
<div style="display:flex;">
<div style="flex:1;">

### padding

padding 是指物件內容與邊框之間的距離，通常用來調整物件內容與邊框之間的間距。

</div>

<div style="flex:1;">

<div data-id="box1" style="background-color:#40a3e7;width:300px;height:100px;margin:10px auto;font-size:1rem;box-sizing:border-box;">
開淺色主題的都是邪教
</div>
<div data-id="box2" style="background-color:#40a3e7;width:300px;height:100px;margin:10px auto;font-size:1rem;padding:1rem;box-sizing:border-box;">
開淺色主題的都是邪教
</div>

```css
padding: 10px; /* 四邊 */
padding: 10px 20px; /* 上下 左右 */
padding: 10px 20px 30px 40px; /* 上右下左 */
```

</div>
</div>

---

## box-sizing

<!-- .slide: data-background-image="img/CSS/box-sizing.webp" data-background-opacity="0.4" data-auto-animate -->

--

<!-- .slide: data-background-image="img/CSS/box-sizing.webp" data-background-opacity="1" data-auto-animate -->

--

<!-- .slide: data-background-image="img/CSS/box-sizing.webp" data-background-opacity="0.4" data-auto-animate -->

### box 是什麼?

html 的每個元素都可被視作為一個盒子，然後可以針對這個盒子去做調整。

--

### box-sizing

<!-- .slide: data-auto-animate -->

```css" data-line-numbers="1-3
width: 300px;
padding: 30px;
box-sizing: content-box; /* 預設值 */
box-sizing: border-box; /* padding 跟 border 會包含在內 */
```

## <div data-id="box1" style="background-color:#40a3e7;width:360px;height:100px;margin:2rem auto;font-size:1rem;">

--
### box-sizing

<!-- .slide: data-auto-animate -->

```css" data-line-numbers="1-2,4
width: 300px;
padding: 30px;
box-sizing: content-box; /* 預設值 */
box-sizing: border-box; /* padding 跟 border 會包含在內 */
```

<div data-id="box1" style="background-color:#40a3e7;width:300px;height:100px;margin:2rem auto;font-size:1rem;">

---

## 漸層

1. 漸層需要顏色跟角度
2. 最常見的漸層為**線性漸層**跟**放射漸層**
3. 可以指定每個顏色的比例
4. 可以決定漸層位置跟大小

--

### 線性漸層 linear-gradient

<!-- .slide: data-auto-animate -->

```css
background: linear-gradient(方向, 顏色1 位置, 顏色2 位置);
```

--

### 線性漸層 linear-gradient

<!-- .slide: data-auto-animate -->

```css
background: linear-gradient(90deg, red, blue);
```

<div data-id="box1"  style="background:linear-gradient(90deg,red,blue);height:100px"></div>

--

<!-- .slide: data-auto-animate -->

#### 顏色位置重疊

```css
background: linear-gradient(45deg, red 50%, blue 50%);
```

<div data-id="box1" style="background:linear-gradient(45deg, red 50%, blue 50%);height:100px"></div>

--

### 放射漸層 Radial Gradient

```css
background: radial-gradient(顏色1 位置, 顏色2 位置);
```

--

### 放射漸層 Radial Gradient

```css
background: radial-gradient(red, blue);
```

<div data-id="box1" style="background:radial-gradient(red,blue);height:200px;width:200px;margin:auto"></div>

--

#### 指定形狀、範圍、中心位置

```css
background: radial-gradient(
    形狀 範圍 at 中 心位置,
    顏色 色彩位置,
    顏色 色彩位置,
    ...
);
```

圓形

```css
background: radial-gradient(circle at center, 顏色1, 顏色2);
```

橢圓形

```css
background: radial-gradient(ellipse at center, 顏色1, 顏色2);
```

--

<!-- .slide: data-background-image="https://user-images.githubusercontent.com/115127388/230543074-7827cfe7-5992-47cb-b54f-3baeb380b614.png" data-background-size="contain" -->

---

<!-- .slide: data-transition="zoom" -->

玩得開心 (:

學習更多：<https://emtech.cc/p/webpallet-3>

Flex：<https://emtech.cc/p/2023ironman-3>

<!-- .slide: data-transition="fade-out" -->
---


<!-- .slide: data-transition="fade-in" -->

本投影片由 [毛哥EM](https://elvismao.com/) 製作  
採用創用 CC「[姓名標示 4.0 國際](https://creativecommons.org/licenses/by/4.0/deed.zh-hant)」授權

![CC](cc.svg)

[毛哥EM資訊密技](https://emtech.cc/)・[毛哥EM公開簡報](https://g.elvismao.com/slides)