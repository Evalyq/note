	var getname = localStorage.getItem("name");
	var blog_id = window.location.search.split("=")[1];
	$(".cmt-list-box").append(commit);
	localStorage.setItem("user_id",res.data.id);
	localStorage.setItem("name",res.data.name);