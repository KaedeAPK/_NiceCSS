# CSS Reference

## Unit of the Char
    px : 1px;
    pt : 1.33px;
    em : 
        default 16px.
        1.2em: x1.2 of parent element.
        same as '%'.
    rem: 
        1 rem is same as root element font-size.
        
## Value
    inherit: 子要素への強制継承. 通常は継承しないborderなどに.

## background
    // 単なる背景色指定
    background: #777;
    // 背景画像を適用。
    background-image: url('m3.png');
    // （繰り返す）拡大縮小を指定.
    background-size:150px;
    // Maximize
    width: 100%; height: 100%

## body
    max-width: 800px;
    margin: N% auto;
    // automaticaly centeralise N% window width.

## bottun
    // id="btn"
    background-color: #4CAF50;
    border: none;
    color: white;
    // Char Color
    padding: 15px 32px;
    // 
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;

## OVER FLOW
    overflow: hidden;
    // can't see anything over the container.
    visible;
    // can see, but out of the border.
    auto;
    // make scroll var!


## a
    a {
        text-decoration: none;
        color: #fff;
    }
    a:hover {
        color: red;
    }
## active or not
    li a {
        display: block;
        color: #000;
        padding: 8px 16px;
        text-decoration: none;
    }

    li a.active {
    background-color: #4CAF50;
    color: white;
    }

    li a:hover:not(.active) {
        background-color: #555;
        color: white;
    }
## flex
.flex-container {
  display: flex;
  flex-direction: row;
  <!-- 1 2 3 4 -->
}
## id selector
    #para1 {
        text-align: center;
        color: red;
    } 
## Box
    <!-- padding 含めてwidthに押さえる -->
    width: 300px;
    padding: 25px;
    box-sizing:border-box;

    <!-- 50px未満には縮まらず、スクロールバーが出る -->
    max-height:50px;
## Grid Layout
    全体を描こう。.wrapperで変換できる
     .wrapper {
            display: grid;
            <!-- 1/4,2/4,1/4で縦に分割 -->
            grid-template-columns: 1fr 2fr 1fr;
            <!-- 最低縦幅100px, 自動で最小縦幅にする -->
            grid-auto-rows: minmax(100px, auto);
            <!-- gridとgridの間を1文字分に -->
            grid-gap: 1em;

            justify-items: stretch;
            align-items: stretch;
        }
    <!-- 縦が1本目のラインから始める -->
    grid-column: 1;
    /横 4本めから2本めまでか？ */
    grid-row: 2/4;
## ul自動シマシマ
    .wrapper > div {
            background: #eee;
            padding: 1em;
        }
        .wrapper > div:nth-child(odd) {
            background: #ddd;
    }

    