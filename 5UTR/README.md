Zur Bewertung von Varianten, die in der 5'UTR lokalisiert sind, ist die Annotation ihres Effekts auf potentielle Initiationsstellen der Translation entscheidend. 

Standard-Tools zur Varianten-Annotation sind nicht darauf spezialisiert, Varianten zu identifizieren, die Start-Codons zerstören oder erzeugen und die resultierenden Leserahmen vorherzusagen. Darüber hinaus wird die Einbettung von Initiationsstellen der Translation in einen Kozak-Kontext nicht bewertet. 

Im Kontext von erblichem Brust- & Eierstockkrebs ist die Identifizierung von 5'UTR-Varianten, die Initiationsstellen erzeugen, entscheidend. Dabei sind folgende Pathomechanismen denkbar (Abbildung aus [Chaldebas et al.](https://doi.org/10.1016/j.ajhg.2026.02.02)): 

<img width="1252" height="576" alt="image" src="https://github.com/user-attachments/assets/f0e2030c-d217-4f63-97cd-04fe872990e5" />


Die Datenbank [VuTR](https://vutr.rarediseasegenomics.org/) visualisiert den Aufbau der 5'UTR in MANE-Transkripten, weiterhin werden die Effekte von Varianten, die in ClinVar und gnomAD v3 gelistet sind, dargestellt. 


Die [hier](https://github.com/GC-HBOC/Recommendations-non-coding-variant-annotation/blob/main/5UTR/5UTR_HBOC.bed) hinterlegte BED-Datei kann zur Filterung nach Varianten, die in den 5'UTRs der MANE-Transkripte der etablierten Brust- & Eierstockkrebsgene lokalisiert sind, genutzt werden. 

Zur Annotation von 5'UTR-Varianten hinsichtlich ihrer potentiellen Effekte auf offene Leserahmen steht das Tool [UTRannotator](https://github.com/ImperialCardioGenetics/UTRannotator) als Plugin in VEP genutzt werden. Darüber hinaus stellt Ensembl ein [Webinterface](https://jun2026.archive.ensembl.org/Homo_sapiens/Tools/VEP) zur Verfügung. Um UTRannotator im Webinterface einzubinden, muss zunächst die Registerkarte *Additional Annotations* geöffnet werden:

<img width="1146" height="1081" alt="image" src="https://github.com/user-attachments/assets/5bde96a4-81ca-4df1-be0c-10164a9e2def" />

... und dann die Checkbox von UTRannotator aktiviert werden:

<img width="861" height="896" alt="image" src="https://github.com/user-attachments/assets/4472cdbf-4d98-41eb-9951-6fb0d9d5fe61" />


Neben UTRannotator steht ebenfalls das Kommandozeilen-Tool [5ULTRA](https://github.com/mchaldebas/5ULTRA) zur Annotation von 5'UTR-Varianten zur Verfügung. Dieses muss lokal installiert werden, bietet jedoch neben Vorhersagen zu Effekten auf die Translation zusätzlich Splice-Prädiktionen.




5'UTR-Varianten, die zu Veränderungen der offenen Leserahmen führen, sind extrem selten. gnomAD v3 listet eine einzige Variante in *BRCA1/2*, und zwar [c.-97C>T](https://gnomad.broadinstitute.org/variant/17-43125348-G-A?dataset=gnomad_r3) in *BRCA1*. 
Entsprechend konnten in einer Analyse der AG Bioinformatik von 462 Genomen von Individuen, die die Einschlusskriterien des DK-FBREK für die genetische Testung erfüllen, sowohl mit UTRannotator wie auch mit 5ULTRA keine Variante mit potentiellen Effekten auf die Translation detektiert werden.  





### Referenzen

