## 需要在index.html，做一點小小的手腳，才會呈現數學式

```bash
sed "s/mathjax\: \'static\/mathjax\/MathJax.js\',//g" output/index.html > index.html; mv index.html output/index.html

```
