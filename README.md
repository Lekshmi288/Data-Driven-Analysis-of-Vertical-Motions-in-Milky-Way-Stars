# Data-Driven-Analysis-of-Vertical-Motions-in-Milky-Way-Stars

Overview
--------
This project (*Thulasidharan et al. 2022*) applies statistical analysis and data-driven modeling to study the vertical motions of young stars in the Milky Way. The goal is to investigate whether the Radcliffe Wave (RW)—a recently discovered large-scale gas structure—also has a corresponding kinematic signature in stellar motions. By analyzing stellar position and velocity data from large-scale sky surveys, we explore whether external perturbations, such as satellite galaxy interactions, could have influenced these vertical oscillations. 

Key Questions:

  (1) Is the Radcliffe Wave a kinematically coherent structure?
             Can we detect vertical oscillations in the motion of young stars that align with the RW?
             
  (2) What caused these vertical motions?
             Could they be triggered by external forces, such as the impact of a satellite galaxy?

The peer-reviewed publication is available at : https://www.aanda.org/articles/aa/full_html/2022/04/aa42899-21/aa42899-21.html

Skills & Techniques Used
------------------------

✅ Large-Scale Data Analysis:

  ◆ Analyzed stellar motion data from Gaia and other astronomical surveys (3,650,719 stars).
       
✅ Statistical Modeling:

  ◆ Applied velocity transformations, kinematic approximations, and data-driven modeling to infer vertical motions. 
       
  ◆ Performed Pearson correlation tests to assess the relationship between the signatures of stellar vertical motions across various catalogues and to determine their statistical significance.

  ◆ Performed bootstrapping to estimate uncertainties in the median vertical velocities and assess the robustness of our results. This method provided statistical confidence in detecting vertical oscillations and ensured that our findings are statistically significant.
       
✅ Data Cleaning & Preprocessing:

   ◆ Filtered and selected high-quality star samples by applying quality cuts. 
       
   ◆ Performed crossmatching between various stellar catalogues to remove the duplicates if any.
       
   ◆ Converted sky coordinates to 3D Galactic Cartesian coordinates using the Astropy package for accurate positional representation and for the ease of understanding.
       
   ◆ For young stars without line-of-sight velocities, derived vertical velocities using just their proper motions, accounting for Galactic rotation and solar motion using Drimmel et al. (2000) approximations.
   
   ◆ Applied Gaussian smoothing to better visualize trends and reduce noise in kinematic data, helping to highlight the underlying patterns in vertical motions which aided in the discovery of a new kinematic wave in the Milky Way.
       
✅ Comparative Analysis:

   ◆ Used older stars as a control sample to account for the effects of dynamical heating.
       
✅ N-body Simulations:

   ◆ Modeled the effect of a Sagittarius-like satellite impact on galactic disk kinematics.
   
✅ Python Packages Used:

  ◆ Pandas: Utilized for data manipulation and preprocessing large-scale datasets.
  
  ◆ NumPy: Applied for numerical operations and handling large arrays of data.
  
  ◆ SciPy: Used for statistical analysis such as computing bidimensional binned statistic which in this case is Median vertical velocity of stars.
  
  ◆ Matplotlib and Seaborn: Employed for data visualization and creating plots to analyze kinematic signatures.
  
  ◆ Astropy: Used for transforming sky coordinates and distances into 3D Galactic Cartesian coordinates.

Data Sources
-----------
🔹 Young Stellar Samples: Open clusters (Cantat-Gaudin et al. 2020), OB stars (González et al. 2021), Upper Main Sequence stars (Poggio et al. 2021).

🔹 Control Sample: Giant stars (Poggio et al. 2018) to compare with dynamically heated older stars.

🔹 Observational Surveys: Gaia DR2/DR3 for stellar positions and motions.

Choosing the right dataset is critical to ensuring a meaningful analysis. Since we aimed to detect kinematic oscillations, we needed:

🔹 Young stars close to their parent molecular clouds (tracing recent motions).

🔹 A control sample of older stars to separate organized motion from random dispersion (accounting for dynamical heating).

🔹 Large-scale datasets with proper motion measurements but missing radial velocities, requiring mathematical approximations to estimate vertical motion.

Challenges & Solutions
----------------------
🔹 Missing Radial Velocities for Young Stars → Used an approximation from Drimmel et al. (2000) for vertical velocity estimation.

🔹 Separating Ordered Motion from Random Motion → Compared young star kinematics with an older control population to isolate coherent trends.


Key Findings
------------
📌 Discovered a distinct kinematic wave in the Milky Way in the young stars, separate from the known Galactic warp.

📌 The kinematic wave exhibits an oscillation amplitude and extent that vary with the age of the stellar population, with younger stars showing the largest perturbations. This suggests that the vertical motions are likely the result of a recent perturbation in the Milky Way's disk. 

📌 Simulations suggest a satellite galaxy impact (like Sagittarius) could be linked to this wave, but open questions remain.

Relevance to Data Science
-------------------------
This project showcases advanced data analysis, statistical modeling, and large-scale dataset handling—skills that are directly applicable to data science. By leveraging observational datasets, transforming noisy data, and performing statistical analysis, we extract meaningful insights from complex real-world data.

References:

[1] Alves, J., Zucker, C., Goodman, A.A. et al. A Galactic-scale gas wave in the solar neighbourhood. Nature 578, 237–239 (2020). https://doi.org/10.1038/s41586-019-1874-z
