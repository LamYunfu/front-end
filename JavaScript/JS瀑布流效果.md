# JS瀑布流效果

```javascript
/**
 * onload函数窗口变化时就会加载
 */
window.onload = function () {
    imgLocation("container", "box");
    var imgData={
        "data":[
            {"src":"image/2.jpg"},
            {"src":"image/3.jpg"},
            {"src":"image/4.jpg"},
            {"src":"image/5.jpg"},
            {"src":"image/6.jpg"}
            ]
    }
    //监听滚动条，在加载到当前的最后一张图片的时候，继续向下加载数据
    window.onscroll = function () {
        if(checkFlag()){
            var cparent = document.getElementById("container");
            for(var i = 0;i < imgData.data.length;i++){
                var ccontent = document.createElement("div");
                ccontent.className = "box";
                cparent.appendChild(ccontent);
                var box_image = document.createElement("div");
                box_image.className = "box_img";
                ccontent.appendChild(box_image);
                var img = document.createElement("img");
                img.src = imgData.data[i].src;
                box_image.appendChild(img);
            }
            imgLocation("container", "box");
        }
    }
}

/**
 * 判断当前是否允许加载数据
 */
function checkFlag() {
    var cparent = document.getElementById("container");
    var ccontent = getChildElement(cparent, "box");
    var lastContentHeight = ccontent[ccontent.length - 1].offsetTop;   //获得最后一张图片的高度
    //获得超出当前页面承载部分的高度，即当前页面顶部距离初始页面顶部的高度
    var scollTop = document.documentElement.scrollTop||document.documentElement.scrollTop;
    //获得当前页面的高度
    var pageHeight = document.documentElement.clientHeight||document.body.clientHeight;
    //如果出现空白了，也就是最后一张图片的高度小于屏幕整体的高度，需要开始加载
    if(lastContentHeight < scollTop + pageHeight){
        return true;
    }
}

/**
 * 设置每一张图片的位置，实现真正的浮动效果
 * @param parent
 * @param content
 */
function imgLocation(parent, content){
    //将parent下的内容全部取出
    var cparent = document.getElementById(parent);
    var ccontent = getChildElement(cparent, content);
    //console.log(ccontent);
    var imgWidth = ccontent[0].offsetWidth; //获得图片宽度
    var cols = Math.floor(document.documentElement.clientWidth/imgWidth);   //知道一行可以放多少个
    cparent.style.cssText = "width:" + imgWidth*cols + "px;margin:0px auto";       //设置container css样式

    var BoxHeightArr = [];
    for(var i = 0;i < ccontent.length;i++){
        if(i < cols){                                         //第一列图片直接填充
            BoxHeightArr[i] = ccontent[i].offsetHeight;
            //console.log(BoxHeightArr[i]);
        }else{
            var minHeight = Math.min.apply(null, BoxHeightArr);         //获得当前的最矮的列
            var minIndex = getminHeightLocation(BoxHeightArr, minHeight);       //获得当前最矮列的下标
            //设置加入图片的位置，把它放到最矮列的下面
            ccontent[i].style.position = "absolute";
            ccontent[i].style.top = minHeight + "px";       //距顶为上面一张图片的距离
            ccontent[i].style.left = ccontent[minIndex].offsetLeft + "px";    //距左为上面一张图片距左的偏移量
            //更新该列的高度，在下一次比较中重新计算。
            BoxHeightArr[minIndex] = BoxHeightArr[minIndex] + ccontent[i].offsetHeight;
        }
    }
}

function getminHeightLocation(BoxHeightArr,minHeight) {
    for(var i in BoxHeightArr){
        if(BoxHeightArr[i] == minHeight){
            return i;
        }
    }
}

function getChildElement(parent, content){
    var contentArr = [];
    var allContent = parent.getElementsByTagName("*");      //通过*匹配获得所有内容
    //将内容中的图片元素提取出来
    for(var i = 0;i < allContent.length;i++){
        if(allContent[i].className == content){     //父级内容中和“box”匹配的元素
            contentArr.push(allContent[i]);
        }
    }
    return contentArr;
}
```



