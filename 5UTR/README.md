Zur Bewertung von Varianten, die in der 5'UTR lokalisiert sind, ist die Annotation ihres Effekts auf potentielle Initiationsstellen der Translation entscheidend. 

Standard-Tools zur Varianten-Annotation sind nicht darauf spezialisiert, Varianten zu identifizieren, die Start-Codons zerstören oder erzeugen und die resultierenden Leserahmen vorherzusagen. Darüber hinaus wird die Einbettung von Initiationsstellen der Translation in einen Kozak-Kontext nicht bewertet. 

Im Kontext von erblichem Brust- & Eierstockkrebs ist die Identifizierung von 5'UTR-Varianten, die Initiationsstellen erzeugen, entscheidend. Dabei sind folgende Pathomechanismen denkbar (Abbildung aus [Chaldebas et al.](https://doi.org/10.1016/j.ajhg.2026.02.02)): 

<img width="1252" height="576" alt="image" src="https://github.com/user-attachments/assets/f0e2030c-d217-4f63-97cd-04fe872990e5" />


Die Datenbank [VuTR](https://vutr.rarediseasegenomics.org/) visualisiert den Aufbau der 5'UTR in MANE-Transkripten, weiterhin werden die Effekte von Varianten, die in ClinVar und gnomAD v3 gelistet sind, dargestellt. 


Die [hier](https://github.com/GC-HBOC/Recommendations-non-coding-variant-annotation/blob/main/5UTR/5UTR_HBOC.bed) hinterlegte BED-Datei kann zur Filterung nach Varianten, die in den 5'UTRs der MANE-Transkripte der etablierten Brust- & Eierstockkrebsgene lokalisiert sind, genutzt werden. Die Spezifikation der 5'UTRs folgt der Annotation von [GENCODE](https://www.gencodegenes.org/human/) (Basic Gene Annotation). 

Zur Annotation von 5'UTR-Varianten hinsichtlich ihrer potentiellen Effekte auf offene Leserahmen steht das Tool [UTRannotator](https://github.com/ImperialCardioGenetics/UTRannotator) als Plugin in VEP genutzt werden. Darüber hinaus stellt Ensembl ein [Webinterface](https://jun2026.archive.ensembl.org/Homo_sapiens/Tools/VEP) zur Verfügung. Um UTRannotator im Webinterface einzubinden, muss zunächst die Registerkarte *Additional Annotations* geöffnet werden:

<img width="1146" height="1081" alt="image" src="https://github.com/user-attachments/assets/5bde96a4-81ca-4df1-be0c-10164a9e2def" />

... und dann die Checkbox von UTRannotator aktiviert werden:

<img width="861" height="896" alt="image" src="https://github.com/user-attachments/assets/4472cdbf-4d98-41eb-9951-6fb0d9d5fe61" />


Neben UTRannotator steht ebenfalls das Kommandozeilen-Tool [5ULTRA](https://github.com/mchaldebas/5ULTRA) zur Annotation von 5'UTR-Varianten zur Verfügung. Dieses muss lokal installiert werden, bietet jedoch neben Vorhersagen zu Effekten auf die Translation zusätzlich Splice-Prädiktionen.




5'UTR-Varianten, die zu Veränderungen der offenen Leserahmen führen, sind extrem selten. gnomAD v3 listet eine einzige Variante in *BRCA1/2*, und zwar [c.-97C>T](https://gnomad.broadinstitute.org/variant/17-43125348-G-A?dataset=gnomad_r3) in *BRCA1*. 
Entsprechend konnten in einer Analyse der AG Bioinformatik von 462 Genomen von Individuen, die die Einschlusskriterien des DK-FBREK für die genetische Testung erfüllen, sowohl mit UTRannotator wie auch mit 5ULTRA keine Variante mit potentiellen Effekten auf die Translation detektiert werden.  





### Referenzen
[Chaldebas M, Ponsin K, Bohlen J, Conil C, Mourelatos H, Stenson PD, Cooper DN, Abel L, Casanova JL, Cobat A, Zhang P. Genome-wide detection of human 5' UTR variants that impact protein translation. Am J Hum Genet. 2026 Apr 2;113(4):809-827.](https://doi.org/10.1016/j.ajhg.2026.02.020) (Paper zu 5ULTRA)

[Wieder N, D'Souza EN, Dawes R, Chan A, Martin-Geary A, Whiffin N. The role of untranslated region variants in Mendelian disease: a review. Eur J Hum Genet. 2025 Sep;33(9):1096-1105.](https://doi.org/10.1038/s41431-025-01905-x) (Review zu Pathomechanismen von Varianten in den 5'- und den 3'-UTRs)

[Zhang X, Wakeling M, Ware J, Whiffin N. Annotating high-impact 5'untranslated region variants with the UTRannotator. Bioinformatics. 2021 May 23;37(8):1171-1173.](https://doi.org/10.1093/bioinformatics/btaa783) (Paper zu UTRannotator)


