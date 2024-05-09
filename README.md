# Move/stop SVG objects on any closed path.

## Overview
SVGは、いろいろなサイトで紹介されいるように、SVGの要素だけでスマートなアニメーションを含んだ描画ができます。より細かなアニメーション制御では、CSSも利用できます。
ここは、SVGオブジェクトが、任意に作ったコース上を、動かしたり、スピードを変えたり、止めたりできるように、JavascriptでSVGオブジェクトを動的に制御するHTMLです。

## Features
- マウスで、任意の多角形を作ることができます。
- 出来上がった多角形の頂点を通る滑らかなコースに変換します。
  コースの中に急なコーナーがある場合、多角形の頂点の移動ができます。
- 作ったコース（センターコース）に並走する内側コース、外側コースを設けることができます。
- ３つのコースを走るSVGオブジェクトは、オブジェクト毎に、動く、スピードを変える、止めるの制御ができます。
  走るSVGオブジェクトは円ではなく、走る方向が分かる三角形としました。

## Demo
https://osaka3t2.github.io/moveSVGObject/

## 操作方法
- SVGエリア（四角枠）内で、マウスクリックで、ポイントを入力します。
　　ポイントが１つのとき、その位置を示すドットが表示されます。ポイントが２つのとき、ドットとドットを結ぶ線が表示されます。3点以上になると、多角形が表示されます。
- Drawボタンを選択すると、指定した多角形が、滑らかな閉ループ（コース）が表示されます。
- Editボタンを選択すると、ポイントをドラックして、移動することができます。
　　急なコーナーは、ポイントの位置編集で、滑らかなコーナーに変更することができます。
- 次にPerpendicularボタンを選択すると、コースが３つになります。
- 上のStartボタンを選択すると、３つSVGオブジェクトが動き出します。
　　Startボタンはトグルボタンで、動き出すと、Stopボタンに変わります。
- Stopボタンを選択すると、SVGオブジェクトが止まります。
- スライダーバーを動かすと、SVGオブジェクトの速度が変化します。
- 左のStart/Stopボタンを選択すると、対応するSVGオブジェクトが動いたり、止まったりします。

## Reference
- https://stackoverflow.com/questions/76702965/smoothly-close-an-svg-path-with-javascript
- https://www.npmjs.com/package/svg-segmentize
- https://www5d.biglobe.ne.jp/~noocyte/Programming/Geometry/PolygonMoment-jp.html
