# test1

<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="content-type" content="text/html;charset=utf-8">
	<title>福袋模拟卡池</title>
</head>
<body>
	<div id="title_link"></div>
	<div>
		<input type="button" value="上三骑+尺" onclick="pickUP(upList)" >
		<input type="button" value="下四骑" onclick="pickUP(downList)" >
	</div>
	<br/>
	<div id="result"></div>
	
	<script type="text/javascript" src="js/title-link.js"></script>
	<script type="text/javascript">
	var upList=[2,8,59,60,76,77,84,85,119];
	var downList=[37,52,62,65,75,97,98,99,113,118];
	function pickUP(pickList){
		document.getElementById("result").innerHTML+="<br/>";
		var result=[];
		for(var i=0;i<10;i++){
			var n=parseInt(Math.random()*100);
			if(n==0){
				result.push(pickList[parseInt(Math.random()*pickList.length)]);
			}
		}
		if(result.length==0){
			result.push(pickList[parseInt(Math.random()*pickList.length)]);
			console.log('保底');
		}
		console.log(result);
		for(var i in result){
			document.getElementById("result").innerHTML+='<img src="http://file.fgowiki.fgowiki.com/fgo/head/' + ("000" + result[i]).slice(-3) + '.jpg" style="width:60px ;height:auto">';
		}
	}
	</script>
</body>
