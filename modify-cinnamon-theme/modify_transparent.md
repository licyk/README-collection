##  Cinnamon桌面主题修改教程：[Cinnamon theme beginner's tutorial](https://forums.linuxmint.com/viewtopic.php?t=156948)

---

以下为对 Linux mint 官方主题的`cinnamon.css`文件的修改部分
> 修改了部分组件的透明度和颜色

- 开始菜单上搜索框的背景
```css
#menu-search-entry, .popup-menu #notification StEntry {
  padding: 7px;
  caret-size: 1px;
  selection-background-color: #1f9ede;
  selected-color: #ffffff;
  transition-duration: 300ms;
  border-radius: 3px;
  color: #303030;
  background-color: #f4f4f4;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.2);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.2);     /* 结束颜色和透明度 */
  border: 1px solid #cfd6e6;
  box-shadow: inset 0 2px 4px rgba(244, 244, 244, 0.05); }
  #menu-search-entry:focus, .popup-menu #notification StEntry:focus, #menu-search-entry:hover, .popup-menu #notification StEntry:hover {
    color: #303030;
    background-color: #f4f4f4;
    border: 1px solid #1f9ede;
    box-shadow: inset 0 2px 4px rgba(244, 244, 244, 0.05); }
  #menu-search-entry:insensitive, .popup-menu #notification StEntry:insensitive {
    color: rgba(48, 48, 48, 0.55);
    background-color: #efefef;
    border-color: 1px solid #dadee7;
    box-shadow: inset 0 2px 4px rgba(239, 239, 239, 0.05); }
  #menu-search-entry StIcon.capslock-warning, .popup-menu #notification StEntry StIcon.capslock-warning {
    icon-size: 16px;
    warning-color: #F27835;
    padding: 0 4px; }
```


- 调整一级菜单的参数，`background-color`第四个参数用来调整透明度
```css
.menu {
  color: #303030;
  border: 1px solid #b5b5b5;
  border-radius: 3px;
  background-color: rgba(232, 232, 232, 0.7); }
  .menu.top {
    border-radius: 0 0 3px 3px; }
  .menu.bottom {
    border-radius: 3px 3px 0 0; }
  .menu.left {
    border-radius: 0 3px 3px 0; }
  .menu.right {
    border-radius: 3px 0 0 3px; }
```


- 调整二级菜单的参数
```css
.popup-sub-menu {
  background-color: #f4f4f4;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.4);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.4);     /* 结束颜色和透明度 */
  box-shadow: none; }
  .popup-sub-menu .popup-menu-item:ltr {
    padding-right: 1.75em; }
  .popup-sub-menu .popup-menu-item:rtl {
    padding-left: 1.75em; }
  .popup-sub-menu StScrollBar {
    padding: 4px; }
    .popup-sub-menu StScrollBar StBin#trough, .popup-sub-menu StScrollBar StBin#vhandle {
      border-width: 0; }
```


- 任务栏右键菜单选中项目背景颜色
```css
  .popup-menu-item:active {
    color: #303030;
    background-color: rgba(31,158,222,0.99); }
  .popup-menu-item:insensitive {
    color: rgba(48, 48, 48, 0.3);
    background: none; }
```


- 调整任务栏的参数，`background-color`第四个参数用来调整透明度
```css
.panel-top, .panel-bottom, .panel-left, .panel-right {
  color: #ffffff;
  border: none;
  background-color: rgba(232, 232, 232, 0.4);
  font-size: 1em;
  padding: 0px; }
```


- 日历事件菜单的背景
```css
.calendar-events-main-box {
  height: 300px;
  margin-right: .5em;
  padding: .5em;
  min-width: 350px;
  border: 1px solid #b5b5b5;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.1);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.1);     /* 结束颜色和透明度 */
  background-color: #f4f4f4; }
```


- 通知的背景
```css
#notification {
  border: 1px solid #b5b5b5;
  border-radius: 3px;
  background-color: #e8e8e8;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.8);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.8);     /* 结束颜色和透明度 */
  padding: 13px;
  spacing-rows: 10px;
  spacing-columns: 10px;
  margin-from-right-edge-of-screen: 20px;
  width: 34em;
  color: #303030; }
  .popup-menu #notification {
    color: #303030;
    border-image: url("light-assets/misc/message.svg") 9 9 9 9; }
    .popup-menu #notification .notification-button, .popup-menu #notification .notification-icon-button {
      padding: 5px; }
  #notification.multi-line-notification {
    padding-bottom: 13px;
    color: #303030; }
  #notification-scrollview {
    max-height: 10em; }
    #notification-scrollview > .top-shadow, #notification-scrollview > .bottom-shadow {
      height: 1em; }
    #notification-scrollview:ltr > StScrollBar {
      padding-left: 6px; }
    #notification-scrollview:rtl > StScrollBar {
      padding-right: 6px; }
  #notification-body {
    spacing: 5px; }
  #notification-actions {
    spacing: 10px; }
```

- 通知菜单上按钮的背景
```css
.notification-button, .notification-icon-button {
  padding: 5px;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.3);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.3);     /* 结束颜色和透明度 */
  }
```


- Alt+Tab 菜单的背景
```css
.switcher-list {
  color: #303030;
  border: 1px solid #b5b5b5;
  background-color: #e8e8e8;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.6);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.6);     /* 结束颜色和透明度 */
  border-radius: 3px;
  padding: 20px; }
  .switcher-list > StBoxLayout {
    padding: 4px; }
  .switcher-list-item-container {
    spacing: 8px; }
  .switcher-list .item-box {
    padding: 8px;
    border-radius: 2px; }
    .switcher-list .item-box:outlined {
      padding: 8px;
      border: 1px solid #1f9ede; }
    .switcher-list .item-box:selected {
      color: #ffffff;
      background-color: #1f9ede;
      border: 0px solid #1f9ede; }
  .switcher-list .thumbnail {
    width: 256px; }
  .switcher-list .thumbnail-box {
    padding: 2px;
    spacing: 4px; }
  .switcher-list .separator {
    width: 1px;
    background: rgba(255, 255, 255, 0.2); }
```


- Alt + F2 菜单的背景
```css
.modal-dialog {
  background-color: #e8e8e8;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.4);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.4);     /* 结束颜色和透明度 */
  border: 1px solid #b5b5b5;
  border-radius: 3px;
  padding: 5px 10px; }
  .modal-dialog > StBoxLayout:first-child {
    padding: 10px; }
  .modal-dialog-button-box {
    spacing: 0;
    margin: 0px;
    padding: 10px;
    border: none;
    background-color: #e8e8e8; }
    .modal-dialog-button-box .modal-dialog-button {
      padding-top: 0;
      padding-bottom: 0;
      height: 30px; }
  .modal-dialog .confirm-dialog-title {
    text-align: center;
    font-weight: bold;
    font-size: 1.3em;
    padding-bottom: 12px; }
```


- 开始菜单左边功能按钮的背景
```css
.menu-favorites-box {
  padding: 10px;
  transition-duration: 300;
  background-color: #e7e7e7;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.3);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.3);     /* 结束颜色和透明度 */
  border: 1px solid #b5b5b5; }
```


- 开始菜单侧栏选中背景颜色
```css
.menu-favorites-button {
  padding: .9em 1em;
  border: 1px solid rgba(0, 0, 0, 0);
  border-radius: 2px; }
  .menu-favorites-button:hover {
    background-color: #1f9ede; }
```


- 开始菜单应用列表子栏选中背景颜色
```css
  .menu-application-button-selected {
    padding: 7px;
    color: #303030;
    background-color: #1f9ede;
    border: 1px solid #b5b5b5; }
    .menu-application-button-selected:highlighted {
      font-weight: bold; }
  .menu-application-button-label:ltr {
    padding-left: 5px; }
  .menu-application-button-label:rtl {
    padding-right: 5px; }
```


- 开始菜单应用列表选中背景颜色
```css
.menu-category-button {
  padding: 7px;
  border: 1px solid rgba(0, 0, 0, 0); }
  .menu-category-button-selected {
    padding: 7px;
    color: #303030;
    background-color: #1f9ede;
    border: 1px solid #b5b5b5; }
  .menu-category-button-hover {
    background-color: red;
    border-radius: 2px; }
  .menu-category-button-greyed {
    padding: 7px;
    color: rgba(48, 48, 48, 0.55);
    border: 1px solid rgba(0, 0, 0, 0); }
  .menu-category-button-label:ltr {
    padding-left: 5px; }
  .menu-category-button-label:rtl {
    padding-right: 5px; }
```


- OSD提示菜单的背景
```css
.info-osd {
  text-align: center;
  font-weight: bold;
  spacing: 1em;
  padding: 16px;
  color: #303030;
  background-gradient-direction: vertical;            /* 这个应该是颜色排列方向 */
  background-gradient-start: rgba(244,244,244,0.6);   /* 起始颜色和透明度 */
  background-gradient-end: rgba(244,244,244,0.6);     /* 结束颜色和透明度 */
  border: 1px solid #b5b5b5;
  border-radius: 5px;
  background-color: #e8e8e8; }
```


- 任务栏小组件选中背景颜色
```css
  .applet-box:hover, .applet-box:checked {
    color: #303030;
    background-color: rgba(31, 158, 222, 0.99); }
  .applet-box:highlight {
    background-image: none;
    border-image: none;
    background-color: rgba(252, 65, 56, 0.5); }
```
