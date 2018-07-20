# JavaScript
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<script>
	function validation(a){
		var id = a.id;
		var name = a.value;
		if(name.trim().length == 0){
			if(id=='userName'){
				document.getElementById("msg1").innerHTML = "账号名不能为空";
			}else if(id=='userPwd'){
				document.getElementById("msg2").innerHTML = "密码不能为空";
			}
		}else if(name.trim().length > 0 ){
			if(id=='userName'){
				document.getElementById("msg1").innerHTML = "";
			}else if(id=='userPwd'){
				document.getElementById("msg2").innerHTML = "";
			}
		}
	}
</script>
</head>
<body style="background-color:#edf5ef;">
	<div style="border:2px solid #ccc; width:250px;height:200px; margin:auto; margin-top:15%;background:rgba(244,244,244,0.4);" >
		<form method="post" action="testLog.jsp">
			<div style="margin-left:20px;margin-top:40px;">
			<span style="font-size:14px;">账号：<input id="userName" type="text" name="userName" placeholder="账号" onblur="validation(this)"></input></span></br>
			<span style="font-size:11px; margin-left:40px;;color:red;" id="msg1"></span></br>
			<span style="font-size:14px;">密码：<input id="userPwd" type="password" name="userPwd" placeholder="密码" onblur="validation(this)"></input></span></br>
			<span style="font-size:11px;margin-left:40px;color:red;" id="msg2"></span></br>
			<input style="margin-left:70px; margin-top:8px"type="submit" value="登录" ></input>
			</div>
		</form>
	</div>
</body>
</html>
