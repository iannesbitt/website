---
title: "gpx2dzg: a tool to convert GPX files to GSSI's proprietary DZG format, and plot comparisons of marks in GPX and DZT/DZX files"
authorlist: Nesbitt, Ian M.
status: published
journal: Zenodo
year: 2019
volume: Software
issue:
pages: Python
doi: 10.5281/zenodo.3261153
link: https://github.com/iannesbitt/gpx2dzg
linktext: iannesbitt/gpx2dzg
linkicon: fab fa-github
abstract: gpx2dzg is a python tool that converts GPS Exchange Format (GPX) files to Geophysical Survey Systems Incorporated (GSSI) DZG format, and can plot time and distance comparisons between user waypoints in GPX versus user marks in GSSI's DZT/DZX files. This is a highly specialized tool for specific survey conditions in which a) radar data is being collected in time-trigger mode, and b) location information is being collected by GPS in endpoint-distance-endpoint mode, with associated user marks at each endpoint and distance mark recorded on the GSSI control unit. Comparison of mark time and distance between the two units is critical for quality assurance, but also for the purposes of mark alignment. DZG files are necessary for distance normalization and other calculations to be made on GPR data, but are not generated when there is no GPS input to the GPR control unit. Once marks are properly aligned, gpx2dzg will write the results to a synthesized DZG file, which allows for further and more advanced processing to take place.
plaintextabstract: gpx2dzg is a software tool that converts files from GPS Exchange Format (GPX; a file that stores GPS information) to DZG, a proprietary format used by Geophysical Survey Systems Incorporated (GSSI) ground-penetrating radar (GPR) systems. This is a specialized tool for specific survey conditions in which a) the user is recording GSSI GPR data in time mode, and b) collecting location information by GPS at each of the endpoints and distance marks along a survey line. Comparison of the time and distance at which each mark is made between the two methods is important for quality assurance, but also for the purposes of proper mark alignment. DZG files are necessary for advanced processing of GPR profiles, but are not generated when there is no GPS plugged in and sending data to the GSSI control box, so must be generated manually in these survey conditions. Once the marks are aligned correctly, gpx2dzg will write the results to a new DZG file.
tags: software
banner: assets/banners/tarn.jpg
template: ref.html
---

