# read-all-cookies
Read all cookies saved


```javascript

function delete_cookie(name) {
  document.cookie = name + '=; expires=Thu, 01 Jan 1970 00:00:01 GMT;';
}

var allCookies = document.cookie.split(";");
for(var i=0; i<allCookies.length ; i++){
	console.info(allCookies[i]);
	var cookie = allCookies[i].split("=");
	if(cookie[0].trim() === "yourCookieName"){
		delete_cookie(cookie[0]);
	}
}
```
