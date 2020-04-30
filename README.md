1、安装
npm install font-spider -g

2、使用
首先需要在css文件中引入WebFont， font.css
```
@font-face {
    font-family: "ST_HUPO";
    src: url('STHUPO.ttf');
    /*font-weight: normal;
    font-style: normal;*/
}
```

3、font.html中包含需要压缩的中文
```
<p class="title">宏源饭店 玉溪饭店</p>
```

4、样式 font.css中
```
.title {
    font-family: 'ST_HUPO';
    font-size: 15px;
}
```

5、压缩 ,在当前目命令行中执行：
```
font-spider font.html
```

6、查看结果 STHUPO.TFT 从3.54MB 压缩到 7KB (仅支持 "宏源饭店 玉溪饭店"  这八个字，其余的中文不支持：华文琥珀)

7、要想支持新增的中文，比如"美好"两个字，需要把中文写到font.html中再次压缩一下
```
font-spider font.html
```

8、重新打开页面就能看到效果了


ps: 字体源文件压缩后被放在 .font-spider目录中
