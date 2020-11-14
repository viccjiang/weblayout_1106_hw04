# 2020秋季六角學院切版直播班Week4
viccjiang/weblayout_1106_hw04

* [頁首頁尾layout](https://viccjiang.github.io/weblayout_1106_hw04/index.html)
* [頁首頁尾layout](https://viccjiang.github.io/weblayout_1106_hw04/layout.html)
* [部落格](https://viccjiang.github.io/weblayout_1106_hw04/blog.html)
* [常見問題](https://viccjiang.github.io/weblayout_1106_hw04/faq.html)

第四週 - 多頁式網頁設計 課程重點
* 多頁式開發 Layout 設計 ([老師範例](https://cacoo.com/diagrams/G4ML24CopC3t8VZX/CD531))
* Gulp JS
* SCSS
* 如何與後端協作網頁版型
* 藉由 Gulp 撰寫樣板語言 (template language)

本週常見遇到的問題 (本週slack筆記)

**Q：GitHub Pages沒有master branch 選項，只有main ?** 
> GitHub計畫從10月1日起，所有新建的儲存庫都會以main為預設branch命名，不再使用master，這項變更並不會影響現有儲存庫的名稱，開發人員也可以選擇不要變更 [資料參考來源](https://www.ithome.com.tw/news/140094)
> 
> 結論：目前的main = 以前的master
> 
**Q：sudo npm i gulp@4 -g 安裝之後出現 location version： unknown 這是正常的嗎 ?**
> location version： unknown 是因為還沒在專案資料夾安裝本地的gulp。但是global的已經裝好囉。
> 
> 結論：正常的！
> 
**Q：使用gulp的目的 ?**

> 直播影片老師有提到，web-layout-training-gulp-master 這整個資料夾，是老師為了讓大家體驗template模板的快速開發，請ray助教寫好gulp資料夾。
> 
> 新專案只需要把檔案「拆解」放進APP資料夾，並利用assets存放其他的images、js、styleCSS等等資料。
> 
> 上述資料就緒後，gulpfile.js資料夾裡的程式會將APP資料夾編譯，編譯結果就是dist資料夾的內容。
> 
> 拆解方式，影片多複習[]()
> 
> 新專案建立，把網頁拆解&存放進app裡面，共同區塊(稱template模板)放入layout.ejs，ex: header、footer。
> 
> 內容content，則做成html，ex: index.html、product.html
> 
**Q：目前的gulp作法有辦法讓一個ejs layout包含另一個layout嗎？**
> 可以但是要都用 ejs 寫， 然後使用這個語法引入
> `<%- include ('{ ejs file path }') %> `
> 
Layout 觀念設計
1. ID 與錨點設計
    *    "#"錨點使用方式
    *    錨點移動時畫面沒有重新整理
    *    回上一頁不會回到首頁
    *    錨點只能有一個ID
    *    CTA call to action ex.導購的區塊
    *    page.html#title 指定到對應位置去
3. 什麼是 [Layout](https://cacoo.com/diagrams/fWdDuMY0WrfI0im7/CD531) ？ 
    *    共通的樣板 layout
    *    每頁都會出現的
    *    呼叫某頁去和樣板做配合 
    *    表頭header 表尾footer
5. EJS 樣板語言介紹
    * layout.html
    * index.html
    * page.html
    * ejs(用在node.js)
    * layout.ejs 樣板 可能有兩三個 ex有滿版或沒滿版
    * 提交作業時 githubpages  dist/index.html
7. Gulp 整合 (講師備註：iterm2重啟 sass rebuild)
    * 記住**Gulp 指令**
        >   gulp -v 查看版本
        >   cd 進入資料夾 把gulp資料夾拉進終端機
        >   sudo npm install
        >   gulp 
    * 關注 **app & dist** 資料夾就好了
    * app編譯Gulp任務工作 >>>dist
    * 在app資料夾寫code
    * 丟上gihubpages是丟上dist資料夾
    * app>assets>style     scss
    * dist>assets>style>all.css
SCSS 結構參考
一個頁面一個scss
```
@import "variable";// 變數  
@import "reset";  // reset.css  
@import "layout"; // 共同框架,第一層
@import "index";     
@import "page1";     

```
作業等級表
* 2. LV2：任選二頁需含RWD
第四週每日任務
* [11/09](https://codepen.io/viccjiang/pen/VwjEKdz) 錨點練習
* [11/10](https://codepen.io/viccjiang/pen/mdEzoYr) @import 引入練習
* [11/11](https://codepen.io/viccjiang/pen/eYzQyGo) SCSS nesting 巢狀結構
* [11/12](https://codepen.io/viccjiang/pen/oNLJxGe) mixin 搭配 include
* [11/13](https://codepen.io/viccjiang/pen/PozXVoO) 使用「＆」

