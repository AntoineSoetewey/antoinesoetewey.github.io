---
title: "Thanks"
permalink: /thanks/
author_profile: true
---

<button id="theme-toggle" onclick="modeSwitcher()"></button>

<script>
const theme = localStorage.getItem('theme');
	if (theme === "dark") {
		document.documentElement.setAttribute('data-theme', 'dark');
	}
</script>

Your form has been successfully submitted !

I will get back to you as soon as possible.

Best,

Antoine Soetewey

[Submit another form](https://www.antoinesoetewey.com/contact/)

<script>
const userPrefers = getComputedStyle(document.documentElement).getPropertyValue('content');	

if (theme === "dark") {
	document.getElementById("theme-toggle").innerHTML = "Light Mode";
} else if (theme === "light") {
	document.getElementById("theme-toggle").innerHTML = "Dark Mode";
} else if  (userPrefers === "dark") {
	document.documentElement.setAttribute('data-theme', 'dark');
	window.localStorage.setItem('theme', 'dark');
	document.getElementById("theme-toggle").innerHTML = "Light Mode";
} else {
	document.documentElement.setAttribute('data-theme', 'light');
	window.localStorage.setItem('theme', 'light');
	document.getElementById("theme-toggle").innerHTML = "Dark Mode";
}

function modeSwitcher() {
	let currentMode = document.documentElement.getAttribute('data-theme');
	if (currentMode === "dark") {
		document.documentElement.setAttribute('data-theme', 'light');
		window.localStorage.setItem('theme', 'light');
		document.getElementById("theme-toggle").innerHTML = "Dark Mode";
	} else {
		document.documentElement.setAttribute('data-theme', 'dark');
		window.localStorage.setItem('theme', 'dark');
		document.getElementById("theme-toggle").innerHTML = "Light Mode";
	}
}
</script>