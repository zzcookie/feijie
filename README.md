
<h1>飛捷廣告Feijie</h1>
<html>
<head>
<title>下拉菜單</title>
<meta charset="utf-8">
<style>
.dropbtn {
    background-color: #82b0e8;
    color: white;
    padding: 16px;
    font-size: 16px;
    border: none;
    cursor: pointer;
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {background-color: #f1f1f1}

.dropdown:hover .dropdown-content {
    display: block;
}

.dropdown:hover .dropbtn {
    background-color: #82b0e8;
}
</style>
</head>
<body>

<h2>功能列表</h2>

<div class="dropdown">
  <button class="dropbtn">作業管理</button>
  <div class="dropdown-content">
    <a href="https://zzcookie.github.io/feijie1/">耗材查詢與管理</a>
    <a href="https://zzcookie.github.io/feijie2/">訂購量試算與訂購紀錄</a>
    <a href="https://zzcookie.github.io/feijie3/">員工績效評估</a>
  </div>
</div>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <div class="dropdown">
  <button class="dropbtn">行銷管理</button>
  <div class="dropdown-content">
    <a href="https://zzcookie.github.io/feijie4/">顧客查詢</a>  
    <a href="https://zzcookie.github.io/feijie5/">顧客關係管理</a>
    <a href="https://zzcookie.github.io/feijie6/">行銷分析</a>
      
  </div>
</div>
 
  
    <head>
        <meta http-equiv="Content-type" content="text/html; charset=UTF-8" />
        <script type="text/javascript" src="js/sql.js"></script>
        <script type="text/javascript" src="js/jquery-3.3.1.min.js"></script>
    </head>

    <body>

    </body>
    <script>
        //建立sqllite例項，獲取資料
        $(function() {
            $.ajax({
                type: "GET",
                url: "Feijie.db",
                success: function(data) {
                    console.info("檔案讀取成功了：" + data);
//                  var fr = new FileReader();
                    var uInt8Array = new Uint8Array(data);
                    var db = new SQL.Database(uInt8Array);
                    console.log("------db"+db);
                    var contents = db.exec("SELECT * from test");
                    console.log("------content"+content);
                }
            });
        });
    </script>


