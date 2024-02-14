## 需要在index.html，做一點小小的手腳，才會呈現數學式

```bash!
sed "s/mathjax\: \'static\/mathjax\/MathJax.js\',//g" output/index.html > index.html; mv index.html output/index.html

```

## 輸出pdf

1. 直接在URL 後加上pdf-print 就可以變成輸出模式
2. 然後直接用chrome 列印輸出成 pdf
3. 如果想要讓輸出更符合原始畫面大小，可以在 `output/static/revealjs/dist/reveal.js`修改
    - 找到
      ```
      a=Math.floor(s.width*(1+e.margin)),o=Math.floor(s.height*(1+e.margin))
      ```
    - 修改成
      ```
      a=Math.floor( 1250 * ( 1 + e.margin ) ),o=Math.floor( (s.height + 40) * ( 1 + e.margin )
      ```
