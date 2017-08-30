---
title: Gallery
layout: post
---

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en-us">
    <head>
        <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
        <meta name="author" content="tzungtzu" />
        <title>TZUNGTZU</title>
        <link rel="shortcut icon" href="/favicon.ico">
        <link href="/atom.xml" rel="alternate" title="setImpl" type="application/atom+xml" />
        <link rel="stylesheet" href="/media/css/style.css">
        <link rel="stylesheet" href="/media/css/github.css">
        <link rel="stylesheet" href="/media/css/scrollright.css">
        <style>
        *{
            margin:5px;
            padding:0;
            list-style:none;
        }
        .menu{
            float:left;
            margin-right:-30000px;
        }
        .menu li{
            float:left;
            width:200px;border:1px solid #ccc;
        }
        </style>
        
    </head>

<body onload="showTime()">

<script language="JavaScript">   
        function showTime(){     
        var thetime=new Date();   //   初始化日期对象 
        var h = thetime.getHours();
        var m = thetime.getMinutes();
        var s = thetime.getSeconds();
        var mm = thetime.getMilliseconds();
        var d = thetime.getDate();
        var mon = thetime.getMonth();
        var y = thetime.getFullYear();
        var z = thetime.getTimezoneOffset();
        var day = (mm/1000+s+m*60+(h+z/60-8)*60*60)/(24*60*60);
        var MyAge = (y-1990)+(mon+1-5)/12+(d+day-11)/30/12;
        //MyAge = Myage.toFixed(2);
        var FixedAge = MyAge.toFixed(11);

        
            document.getElementById( "timeArea").innerText   =  'It is now ' + thetime.toLocaleString(); 
            document.getElementById('age').innerHTML = "I am "+ FixedAge +' years old.'
     
            window.setTimeout( "showTime()",1);   //setTimeout (表达式,延时时间)其中延时时间以豪秒为单位(1000ms=1s)
        } 

</script>


<script type="text/javascript">
    $.getJSON("https://api.douban.com/v2/book/1220562?alt=xd&callback=?", function(book) {
        var title = book.title ? book.title : "";
        var tmp = "<img src="+book.image+" style='margin:10px;float:left'>";
        tmp += "<div>Tiktle : <a href="+book.alt+" target='_blank'>"+title+"</a></div>";
        if (book.author) 
            tmp += "<div>Authors : "+book.author+"</div>";
        if (book.pubdate) 
            tmp += "<div>Pubdate : "+book.pubdate+"</div>";
        if (book.isbn13) 
            tmp += "<div>ISBN : "+book.isbn13+"</div>";
        if (book.price) 
            tmp += "<div>Price : "+book.price+"</div>";
        if (book.pages) 
            tmp += "<div>Pages : "+book.pages+"</div>";
        if (book.publisher) 
            tmp += "<div>Publisher : "+book.publisher+"</div>";
        if (book.rating.average) 
            tmp +="<div>Rating: "+book.rating.average+" / "+book.rating.numRaters+decodeURI("%E4%BA%BA")+ "</div>"
        tmp += "<p>"+(book.summary ? book.summary : "")+"</p>";
        document.getElementById('bookinfo')..innerHTML = tmp;
    });
</script>

<div id="timeArea" align="center">

</div>

<div id="age" align="center">

</div>


<div id="bookinfo" align="center">

</div>


</body>
</html>

