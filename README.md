# memeMaker
udacity FEDN

長輩圖製作(誤)
總之就是可以動態組合圖片和文字的東西(果然就是長輩圖啊)
https://github.com/telsaiori/memeMaker/blob/master/MemeMaker.html

主要就是redrawMeme裡面的code
```
    function redrawMeme(image, topLine, bottomLine) {
      // Get Canvas2DContext
      var canvas = document.querySelector('canvas');
      var ctx = canvas.getContext("2d");
      // Your code here
      if(image != null){
        ctx.drawImage(image, 0, 0, canvas.width, canvas.height);
      }
        //text attributes
      ctx.font = '30pt Impact';
      ctx.textAlign = 'center';
      ctx.strokeStyle = 'black';
      ctx.lineWidth = 3;
      ctx.fillStyle = 'white';
      if (topLine != null) {
        ctx.fillText(topLine, canvas.width / 2, 40);
        ctx.strokeText(topLine, canvas.width / 2, 40);
      }
      if(bottomLine != null){
        ctx.fillText(bottomLine, canvas.width / 2, canvas.height - 20);
        ctx.strokeText(bottomLine, canvas.width / 2, canvas.height - 20);
      }
    }
```
先判斷有沒有圖,有的話就畫出來
設定文字字型和顏色......
topLine有輸入字的話就畫出來
bottomLine同上
其實這部份很短,但我用了很久.......
不知道為什麼寫javascript的時候我的錯字率高到有點可怕(遠目)

然後因為這個題目我才知道
原來javascript的if如果只有一行的話不一定要有{},雖然大家都強烈建議不要省略{}
http://stackoverflow.com/questions/7117873/do-if-statements-in-javascript-require-curly-braces




> Written with [StackEdit](https://stackedit.io/).
