# Parallax Scrolling Website

## **星號標誌**
```CSS
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300,400,500,600,700,800,900&display=swap");
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    scroll-behavior: smooth;
}
```
* 星號標誌會指向頁面上所有的元素。 很多程序員都會用這個訣竅來將margin和padding歸零。
>參閱：[星號標誌](https://code.tutsplus.com/zh-hant/tutorials/the-30-css-selectors-you-must-memorize--net-16048)

## **視差效果**
```javascript
   <script>
        let stars = document.getElementById('stars');
        let moon = document.getElementById('moon');
        let mountains_behind = document.getElementById('mountains_behind');
        let mountains_front = document.getElementById('mountains_front');
        let text = document.getElementById('text');
        let btn = document.getElementById('btn');
        let header = document.querySelector('header');

        window.addEventListener('scroll', () => {
            //透過抓視窗的scroolY值，作為其他element位移的參數
            let value = window.scrollY;
            stars.style.left = `${value * 0.25}px`;
            moon.style.top = `${value * 1.05}px`;
            mountains_behind.style.top = `${value * 0.5}px`;
            mountains_front.style.top = `${value * 0}px`;
            text.style.marginRight = `${value * 4}px`;
            text.style.marginTop = `${value * 1.5}px`;
            btn.style.marginTop = `${value * 1.5}px`;

        });
    </script>
```



