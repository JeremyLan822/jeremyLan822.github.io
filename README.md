# jeremyLan822.github.io
<!DOCTYPE html>
<html>
<head>
	<title>heihei</title>
	<meta charset="utf-8">
	<style type="text/css">
		*{margin: 0;padding: 0;}
		#move{
			cursor: move;
			padding: 10px;
			width: 300px;
			background-color: #f4f4f4;
			margin: 10px auto;
			border: 1px solid #ccc;
		}
		#move a{
			display: inline-block;
			width: 58px;
			height: 25px;
			border: 1px solid #ddd;
			border-radius: 3px;
			background-color: #fff;
			text-align: center;
			margin: 10px 17px;
			position: relative;
			padding-top: 40px;
			color: #9c9c9c;
			font-size: 12px;
			text-decoration: none;
			line-height: 25px;
			overflow: hidden;
		}
		#move i{
			position: absolute;
			top: 20px;
			left: 0;
			display: inline-block;
			width: 100%;
			text-align: center;
			filter: alpha(opacity=100);
			opacity: 1;
		}
		#move a:hover{
			color: #f00;
		}
		#move img{
			border: none;
			width: 40px;
			height: 40px;
			position: absolute;
			top:-15px;
			left: 10px;
		}
	</style>
	<script type="text/javascript" src="js/move.js"></script>
	<script type="text/javascript">
		window.onload=function () {
			var box=document.getElementById('move');
			var List=box.getElementsByTagName('a');
			for (var i = 0; i < List.length; i++) {
				List[i].onmouseenter=function(){
					var _this=this.getElementsByTagName('i')[0];
                    startMove(_this,{top:0,opacity:0},function(){
                    	_this.style.top=30+'px';
                    	startMove(_this,{top:15,opacity:100})
                    })
				}
			}
		}
	</script>
</head>
<body>
	<div id="move">
	   	<a href="#"><i><img src="images/game.png"/></i><p>彩票</p></a>
	   	<a href="#"><i><img src="images/insurance.png"/></i><p>电影</p></a>
	   	<a href="#"><i><img src="images/lottery.png"/></i><p>音乐</p></a>
	   	<a href="#"><i><img src="images/money.png"/></i><p>缴费</p></a>
	   	<a href="#"><i><img src="images/movie.png"/></i><p>理财</p></a>
	   	<a href="#"><i><img src="images/telephone.png"/></i><p>外卖</p></a>
    </div> 
</body>
</html>
