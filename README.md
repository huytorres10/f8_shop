1. Dụng source base
   base.css: config chung css cho dự án.
   main.css: Code riêng css cho dự án, sau này mỗi component sẽ chứa các file css khác nhau

2. Reset CSS
   key search: normalizer css cdn
   web: https://cdnjs.com/libraries/normalize

- Dùng cdn = link <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css" />
- Hoặc tải file xuống rồi nhét vào thư mục assets/css

3. Dựng base CSS
   box-sizing: inherit; : Kế thừa thằng cha có box-sizing
   key search: google roboto font
   web: https://fonts.google.com/specimen/Roboto

- Select type font mong muốn

* Copy link dán vào file html
* Copy font-family: 'Roboto', sans-serif; vào file CSS
  .grid {
  width: 1200px;
  max-width: 100%;
  }

- Đối với màn hình từ 1200px trở lên thì khung web sẽ hiển thị là 1200px.
- Đối với màn hình nhỏ hơn 1200px thì nó sẽ luôn hiện 100% thao giao diện trình duyệt.

4. Dựng source web

- Tạo 1 thẻ chứa toàn bộ website
- Làm từng thành phần của website 1. Ex: Header, container, footer.

5. Navbar CSS

- display: block : có thể đặt chiều cao, chiều rộng cho Element

7. Css cho icons.

- Nếu nó là text thì nên cho vào thẻ span
- Trỏ chuột vào không có hiện tượng thì để cursor: text hay default.
- Khi display flex center cho đối tượng cha khi cha height là lẻ thì thêm
  thuộc tính min-height = height + 1 cho chẵn.

8. QR code

- Khi cha position: relateive;
- Con position: Absolute thì con để top: 100% sẽ sát bottom cha.
- Khi dùng các lớp giả ::before thì để display:block để nhìn thasy đc trên màn hình để test.

11. Header Notify Css

- Cách làm mũi tên lên = css, dùng 1 thẻ k có width height, set border cho nó.
  border-style: solid;
  border-width: 20px 30px;
  border-color: transparent transparent var(--white-color) transparent;

13. Dựng base modal

- Tạo ra 1 class modal phủ toàn trang web (fixed để auto đứng 1 chỗ)
  -- Tạo ra lớp model overlay cũng phủ toàn trang web
  -- Tạo ra lớp modal body, auto đứng giữa trang web (margin: auto để auto đứng giữa trang web)

16. Css Register form p2
    overflow: hidden

- Viết vào thằng cha: mục đích: Nếu thằng con to hơn cha thì ẩn phần lòi ra của thằng con.

21. Setup git rebase hiện tab git-rebase-todo
    git config --global core.editor "code --wait"

setting json

{
"git.autofetch": true,
"workbench.editor.wrapTabs": true,
"workbench.editorAssociations": {
"git-rebase-todo": "default"
},
"zenMode.hideTabs": false,
"[json]": {
"editor.quickSuggestions": {
"strings": true
},
"editor.suggest.insertMode": "replace",
"gitlens.codeLens.scopes": ["document"]
},
"gitlens.advanced.messages": {
"suppressCommitHasNoPreviousCommitWarning": true,
"suppressCommitNotFoundWarning": false,
"suppressCreatePullRequestPrompt": false,
"suppressDebugLoggingWarning": false,
"suppressFileNotUnderSourceControlWarning": false,
"suppressGitDisabledWarning": false,
"suppressGitMissingWarning": false,
"suppressGitVersionWarning": false,
"suppressImproperWorkspaceCasingWarning": false,
"suppressLineUncommittedWarning": false,
"suppressNoRepositoryWarning": false,
"suppressRebaseSwitchToTextWarning": true
},
"prettier.printWidth": 120,
"prettier.useTabs": true,
"prettier.vueIndentScriptAndStyle": true,
"prettier.withNodeModules": true,
"[vue]": {
"editor.defaultFormatter": "esbenp.prettier-vscode"
},
"editor.suggestSelection": "first",
"vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
"settingsSync.ignoredExtensions": ["chris-noring.node-snippets"],
"liveServer.settings.donotShowInfoMsg": true,
"files.autoSave": "afterDelay",
"window.zoomLevel": 1,
"editor.formatOnPaste": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnSave": true
}

30. Cha: display: flex, con margin: auto --> con căn giữa

31. <div class="home-product-item__img"
                		style="background-image: url(https://cf.shopee.vn/file/f03a91132ed1fd13bd36e704f4a52b6e_tn)"
                										></div>
            => Muốn ảnh thành hình vuông thì set padding-top: 0;
            => Không cho ảnh lặp lại: background-repeat: no-repeat;
            => Cho ảnh nhỏ lại: background-size: contain;
            => Show ảnh đúng trọng tâm: background-position: center;

            Ẩn chữ và tạo dấu ... cho dòng 2.

        line-height: 1.8rem;
        height: 3.6rem;
        overflow: hidden;
        display: block;
        display: -webkit-box;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;

    => Set line-height => Chiều cao 1 dòng.
    => Set height = line-hight\*2

32. Cách thu nhỏ phần tử khi dùng font-size không được.

- Dùng zoom: 0.1 -> hên xui.
- Dùng transform: scale(0.1) và transform-origin: right; để lấy tâm thu nhỏ bên phải.

33. Tạo 1 nửa hình vuông => Tam giác vuông.

- 2 đáy top và right thì:
  border-top: 3px solid currentColor;
  border-left: 3px solid transparent;

- để con ăn theo tông màu cha.
  Cha để color: var(--primary-color); background-color: currentColor;
  con để: background-color: currentColor;
  muốn con tối màu hơn thì con để: filter: brightness(60%);
