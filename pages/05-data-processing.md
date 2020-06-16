---
layout: home
permalink: /data-processing
title: "Data Processing"
excerpt: "<br>"
image:
  feature: /banners/multibeam-banner.jpg
---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}

    25. 
Data processing considerations


        31. 
During survey
Processing during a survey should at a minimum be done to QC the data, both bathymetry and backscatter data. QC includes:



*   checking for artefacts
*   consistency of seabed backscatter
*   meeting the required specifications, e.g. data density

A processing log should be kept.



        32. Post-survey

Post-survey processing should include:



*   reduction of soundings to appropriate vertical datum (observed or post-processed GNSS tides).
*   application of SVPs and refraction correction applied (where allowed).
*   data cleaning, which may vary depending on the purpose of the survey.
*   data QA using crosslines (if collected). If specific crosslines are not collected, consider using transit lines that cross main survey lines (e.g. data acquired while going to a sampling location).
*   TPU calculation for each sounding (

<p id="gdcalert48" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "section 5.2"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert49">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[section 5.2](#heading=h.36ei31r)).

See also section 10 of AHO, 2018 for more information on processing.



        33. Backscatter processing requirements 

Please keep a processing log that records what processing software and settings are used to prepare the backscatter mosaic. When you process, it is important to specify the imagery type (Beam Average/Time Series); Beam Pattern Correction (yes/no); and Anti-aliasing (yes/no) selection.

Mandatory information to record for the backscatter data processing is:

•	the AVG window size 

•	AVG method

•	beam Pattern Correction (yes/no – if yes, please provide the beam pattern file)

•	the imagery type (Beam Average/Time Series)

•	gain (yes/no)

•	time varying gain (yes/no)

Other image processing information that is useful but not mandatory:

•	the speckle option (to remove noise)

•	anti-aliasing (yes/no) 

Further details about best-practice for backscatter data acquisition can be found in Lamarche and Lurton (2017).

Acquisition and processing logs should be delivered alongside all raw data (including calibration test) and processed mosaics in accordance with Section 7.



    26. 
Total propagated uncertainties (TPU)
The total propagated uncertainty (TPU) for each sounding should be computed and included in the data submission (

<p id="gdcalert49" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: undefined internal link (link text: "Section 7"). Did you generate a TOC? </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert50">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

[Section 7](#heading=h.3x8tuzt)).

The TPU is the combination of the total horizontal uncertainties (THU) and the total vertical uncertainties (TVU) of that sounding ([Appendix E](#bookmark=id.odc9jc)). THU is a 2-dimensional quantity in the horizontal plane and is assessed only after the GNSS-Inertial system has been calibrated. TVU is a 1-dimensional quantity in the vertical dimension. TPU is not a linear addition of uncertainties in each system’s component. It is a propagated combination of uncertainties for the non-linear set of equations comprising the integrated swath acoustic-GNSS Inertial system. 

Uncertainty calculation is best addressed using most internationally accepted statistical models for determination of TPU, which are derived from Hare et al. (1995).  Current international best-practice statistical model for resolving the system of equations is the Combined Uncertainty Bathymetric Estimator (CUBE). The average horizontal and vertical TPU estimates determined by the software for a range of water depths is provided with respect to the IHO S-44 standard for position and depth accuracy in Table 6. 

_Table 9: Example Sounding Accuracy - TPU (calculated at 1σ, but most software computes at 2σ)_


<table>
  <tr>
   <td><strong>Depth band (m)</strong>
   </td>
   <td><strong>0-5</strong>
   </td>
   <td><strong>5-20</strong>
   </td>
   <td><strong>20-50</strong>
   </td>
   <td><strong>50-100</strong>
   </td>
   <td><strong>100-200</strong>
   </td>
  </tr>
  <tr>
   <td colspan="6" >Position Accuracy (m)
   </td>
  </tr>
  <tr>
   <td>IHO Standard
   </td>
   <td>5.25
   </td>
   <td>5.50
   </td>
   <td>6.00
   </td>
   <td>6.50
   </td>
   <td>7.25
   </td>
  </tr>
  <tr>
   <td>TPU Estimate
   </td>
   <td>0.27
   </td>
   <td>0.27
   </td>
   <td>0.30
   </td>
   <td>0.34
   </td>
   <td>0.42
   </td>
  </tr>
  <tr>
   <td colspan="6" >Depth Accuracy (m)
   </td>
  </tr>
  <tr>
   <td>IHO Standard
   </td>
   <td>0.38
   </td>
   <td>0.39
   </td>
   <td>0.44
   </td>
   <td>0.50
   </td>
   <td>0.63
   </td>
  </tr>
  <tr>
   <td>TPU Estimate
   </td>
   <td>0.27
   </td>
   <td>0.27
   </td>
   <td>0.28
   </td>
   <td>0.31
   </td>
   <td>0.35
   </td>
  </tr>
</table>