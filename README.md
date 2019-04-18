# mikrotik-hotspot-external-login-page-none-PHP
Mikrotik External hosted login page

#Instructions
this page is adoptation of full featured hotspot transaction sever (it runs on nodjs):  

1)This page can run on any html server, but you will have to change details within the index.html to match yours

2) in your mikrotik router login.html #add this just before <body> tag
  
  <script type="text/javascript">//checks for internet connection//en if available show external login//if not available show default mikrotik

	if(navigator.onLine){
		window.open('http://EXTERNAL-HOTSPOT-LINK/index.html?login=true&error=$(error)&link-login-only=$(link-login-only)&link-orig=$(link-orig)&chap-id=$(chap-id)&chap-challenge=$(chap-challenge)&link-orig-esc=$(link-orig-esc)&mac-esc=$(mac-esc)&username=$(username)', '_self');//open link where hotspot is at  
	}
	
</script>

change : http://EXTERNAL-HOTSPOT-LINK/index.html to url of were you have index.html at


#bug note

#currently this page does not work with Hotspot authentication method of [ Http-chap ] best use [ http-pap ]
