
<h1>飛捷廣告Feijie</h1>
<html>
<head>
<title>下拉菜单</title>
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
  <button class="dropbtn">耗材管理</button>
  <div class="dropdown-content">
    <a href="http://">耗材查詢與管理</a>
    <a href="http://">訂購量試算與訂購紀錄</a>
  </div>
</div>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<div class="dropdown">
  <button class="dropbtn">人員管理</button>
  <div class="dropdown-content">
    <a href="http://">員工績效評估</a>
    <a href="http://">自動化排班</a>
 </div>
     </div>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <div class="dropdown">
  <button class="dropbtn">行銷管理</button>
  <div class="dropdown-content">
    <a href="http://">顧客關係管理</a>
    <a href="http://">行銷分析</a>
  </div>
</div>
    
    
// 建立MySQL的資料庫連接 
$link = mysqli_connect("localhost", "root", "1234") 
        or die("無法開啟MySQL資料庫連接!<br/>");
// 指定開啟的資料庫名稱myschool
$dbname = "test";
// 開啟指定的資料庫
if ( !mysqli_select_db($link, $dbname) )
   die("無法開啟 $dbname 資料庫!<br/>");
else
   echo "資料庫: $dbname 開啟成功!<br/>";
mysqli_close($link);  // 關閉資料庫連接
    
// 建立MySQL的資料庫連接 
$link = mysqli_connect("localhost","root",
                       "1234","test")
        or die("無法開啟MySQL資料庫連接!<br/>");
echo "資料庫test開啟成功!<br/>";
$sql = "INSERT INTO `account`(`name`, `tel`, `birthday`, `address`, `id`) VALUES (\"1234\",\"1234\",\"2016-12-22\",\"123\",\"003\")"; // 指定SQL字串
echo "SQL字串: $sql <br/>";
//送出UTF8編碼的MySQL指令
mysqli_query($link, 'SET NAMES utf8'); 
mysqli_query($link, $sql);
