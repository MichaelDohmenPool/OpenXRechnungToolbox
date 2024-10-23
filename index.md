## OpenXRechnungToolbox

<style>
	* {box-sizing: border-box;}
        body {font-family: Verdana, sans-serif;}
	.mySlides {display: none;}
	img {vertical-align: middle;}
	.slideshow-container {
	text-align: center;
	/*color: #f2f2f2;*/
	  max-width: 1000px;
	  position: relative;
	  margin: auto;
	}
	.numbertext {
	  color: #f2f2f2;
	  font-size: 12px;
	  padding: 8px 12px;
	  position: absolute;
	  top: 0;
	}
	.dot {
	  height: 15px;
	  width: 15px;
	  margin: 0 2px;
	  background-color: #bbb;
	  border-radius: 50%;
	  display: inline-block;
	  transition: background-color 0.6s ease;
	}
	.active {
	  background-color: #717171;
	}
	.fade {
	  -webkit-animation-name: fade;
	  -webkit-animation-duration: 1.5s;
	  animation-name: fade;
	  animation-duration: 1.5s;
	}
	@-webkit-keyframes fade {
	  from {opacity: .4} 
	  to {opacity: 1}
	}
	@keyframes fade {
	  from {opacity: .4} 
	  to {opacity: 1}
	}	
	.btn {
	  background-color: #0090ff;
	  border: none;
	  color: white;
	  padding: 12px 30px;
	  cursor: pointer;
	  font-size: 20px;
	}
	.btn:hover {
	  background-color: RoyalBlue;
	} 	
</style>

<div class="slideshow-container">
			<div class="mySlides fade">
			  <div class="numbertext">1 / 6</div>
			  <img src="resources/help/img/slideshow/Oberflaeche.PNG" style="height:100%">
			  <div class="text">Hauptfenster</div>
			</div>
			<div class="mySlides fade">
			  <div class="numbertext">2 / 6</div>
			  <img src="resources/help/img/slideshow/Pruefbericht.PNG" style="height:100%">
			  <div class="text">Prüfbericht</div>
			</div>
			<div class="mySlides fade">
			  <div class="numbertext">3 / 6</div>
			  <img src="resources/help/img/slideshow/Visualisierung.PNG" style="height:100%">
			  <div class="text">Visualisierung</div>
			</div>
			<div class="mySlides fade">
			  <div class="numbertext">4 / 6</div>
			  <img src="resources/help/img/slideshow/VisualisierungPDF.PNG" style="height:100%">
			  <div class="text">PDF-Visualisierung</div>
			</div>
			<div class="mySlides fade">
			  <div class="numbertext">5 / 6</div>
			  <img src="resources/help/img/slideshow/LWID.PNG" style="height:100%">
			  <div class="text">Leitweg-ID-Rechner/-Prüfer</div>
			</div>
			<div class="mySlides fade">
			  <div class="numbertext">6 / 6</div>
			  <img src="resources/help/img/slideshow/Einstellungen.PNG" style="height:100%">
			  <div class="text">Einstellungen</div>
			</div>
</div>
<br>

<div style="text-align:center">
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
  <span class="dot"></span> 
</div>

<script>
var slideIndex = 0;
showSlides();

function showSlides() {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  slideIndex++;
  if (slideIndex > slides.length) {slideIndex = 1}    
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
  setTimeout(showSlides, 2500); // Change image every 2 seconds
}
</script>

Die OpenXRechnungToolbox (OXT) bietet eine graphische Benutzeroberfläche (und seit Version 3.0.0 auch einen Kommandozeilenzugriff) zu den mit dem Standard XRechnung herausgegebenen Tools (Prüftool, Visualisierung) und fügt ergänzend noch ein paar weitere Funktionalitäten hinzu (Codelistenauflösung für die Visualisierung, Leitweg-ID-Rechner/-Prüfer, Nutzung für Peppol-Rechnungen). Damit macht sie die XRechnungs-Tools für Nicht-Programmierer nutzbar. 

<!-- Add icon library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<!-- Auto width -->
<center><a href="https://github.com/jcthiele/OpenXRechnungToolbox/releases" target="_blank"><button class="btn"><i class="fa fa-download"></i> Download</button></a></center>


### Funktionalitäten auf einen Blick

- **Erzeugung einer menschenlesbaren Visualisierung** von XRechnungs-Dateien, inkl. optionaler Codelisten-Auflösung, inkl. Speicherfunktion als HTML-Datei sowie Erzeugung einer PDF-Visualiserung; auch für andere Rechnungsinstanzen nutzbar, die konform zur Europäischen Norm EN16931 sind (z.B. Peppol BIS 3.0)
- **Technische Validierung** von XRechnungs-Dateien sowie Peppol BIS 3.0 Rechnungen, verfügbar für verschiedene XRechnungs-Versionen, inkl. Speicherfunktion des Prüfberichts als HTML-Datei
- Berechnung und Prüfung von **Leitweg-ID-Prüfziffern**
- **Konvertierung** von UN/CEFACT CII nach UBL 2.1
- Nutzung der Funktionalitäten per **graphischer Benutzeroberfläche** oder per **Kommandozeile** (CLI)

### Vorteile gegenüber vielen anderen Angeboten

- **Sie geben Ihre Daten nicht aus der Hand**: kein Hochladen von Rechnungsdateien auf einen Server; rein lokale Desktop-Anwendung (Datenschutz)
- **Sie bleiben jederzeit anonym**: keine Registrierung oder sonstige Nutzer*inneninformationen erforderlich (Datenschutz)
- **Ihnen rückt kein Vertrieb auf den Leib**: kein kommerzielles Interesse
- **Sie besitzen vollständige digitale Souveränität**: offener Quellcode (Open Source), somit vollständige Nachvollziehbarkeit und Weiterentwicklungsmöglichkeit

### Wer steckt dahinter

Die OpenXRechnungToolbox wurde von Jan C. Thiele entwickelt. Dr. Dr. Jan C. Thiele war hauptberuflich Referent und stv. Referatsleiter beim Senator für Finanzen der Freien Hansestadt Bremen. Er ist einer der Autoren des Standards XRechnung, hat das EU-Projekt "Peppol eInvoicing für Government in Germany" (PeGGy) für Bremen durchgeführt und war Vertreter Bremens im Steuerungskreis von XRechnung.<br /> 
Heute arbeite er als Projektmanager und stv. Stabsstellenleiter für die Bürgerschaftskanzlei Bremen (Landtag der Freien Hansestadt Bremen) und ist nebenberuflich als Lehrbeauftragter an der Hochschule Bremen im Dualen Studiengang für Wirtschafts- und Verwaltungsinformatik tätig.
Zuvor hat er als wissenschaftlicher Mitarbeiter der Universität Göttingen in verschiedenen Projekten (betriebliche) Informationssysteme, insb. Entscheidungsunterstützungssysteme im Umweltbereich, entworfen und entwickelt. Ein Schwerpunkt seiner wissenschaftlichen Tätigkeit war die simulationsbasierte Entscheidungsunterstützung.<br /> 
Die OpenXRechnungToolbox ist ein Freizeitprojekt und steht in keinem direkten Zusammenhang mit dem Senator für Finanzen. 
Als Open Source Software ist jede(r) eingeladen zur Weiterentwicklung der Software beizutragen. 

### Weitere Infos

Das Benutzerhandbuch etc. ist [hier](https://jcthiele.github.io/OpenXRechnungToolbox/resources/help/manual.html "Benutzerhandbuch") zu finden.

### Kontakt

Wenn Sie Kontakt aufnehmen wollen, Lob oder Optimierungshinweise mitteilen möchten, dann wenden Sie sich bitte mit Ihrem Anliegen an: <a href="mailto:openxrechnungtoolbox@gmx.net">openxrechnungtoolbox@gmx.net</a>.

### Download

Das jeweils aktuelle Release ist [hier](https://github.com/jcthiele/OpenXRechnungToolbox/releases) erhältlich.
Der Quellcode wird im [GitHub Repository](https://github.com/jcthiele/OpenXRechnungToolbox) gepflegt. 
<br />
<br />
<small>(Masterbranch)</small>
