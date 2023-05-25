## This is a repository containing the work I made for my graduation project. 
# Be stars and its importance
Be stars, short for B-emission stars, are a class of rapidly rotating, hot, and luminous stars. They belong to the spectral class B, which is characterized by their blue color and high surface temperatures.

What sets Be stars apart is the presence of emission lines in their spectra, indicating the presence of a circumstellar disk of gas and dust surrounding the star. These disks are formed due to the rapid rotation of the star, which causes the material at the equator to be thrown outward, creating a flattened disk-like structure.

The exact mechanisms responsible for the formation and maintenance of the circumstellar disks in Be stars are still not fully understood. However, it is believed that the disks may be formed from material ejected from the star's atmosphere or from the interaction between the star and a companion in a binary system.

Be stars are known for their variability in brightness and the presence of spectral line variations. The emission lines in their spectra can change in strength and shape over time, indicating ongoing processes within the circumstellar disk.

These fascinating stars have been the subject of extensive observational and theoretical studies, as they provide valuable insights into stellar evolution, mass loss mechanisms, and the physics of circumstellar disks. They are commonly found in regions of star formation and young stellar clusters.

Overall, Be stars stand out for their distinctive spectral features and the intriguing circumstellar disks that surround them, making them an intriguing area of research in astrophysics.
# Photometry
In astrophysics, photometry is a technique used to measure and study the properties of celestial objects based on their observed light. It involves measuring the intensity or brightness of light emitted or reflected by stars, galaxies, or other astronomical sources.

Photometry typically involves the use of specialized instruments called photometers, which are sensitive detectors capable of measuring the amount of light received from an astronomical object. These measurements are usually obtained through specific filters that allow only certain wavelengths of light to pass through, enabling astronomers to study specific regions of the electromagnetic spectrum.

By analyzing the brightness of an object at different wavelengths or over time, astronomers can gain valuable information about various astrophysical properties. Photometry can be used to determine the temperature, size, composition, distance, and variability of celestial objects.

One fundamental concept in photometry is the magnitude system, which quantifies the apparent brightness of an object. The magnitude scale is logarithmic, with brighter objects having lower (negative) magnitudes. The difference in magnitude between two objects corresponds to a specific ratio of brightness.

Photometry plays a crucial role in various areas of astrophysics, including stellar astronomy, extragalactic astronomy, and the study of transient phenomena. It is widely used to characterize stars, measure their properties, detect exoplanets through the transit method, study the variability of variable stars, determine the luminosity and distances of galaxies, and much more.

Overall, photometry provides a quantitative approach to studying the light emitted by celestial objects, allowing astronomers to unravel the mysteries of the universe and gain insights into the physical processes occurring in the cosmos.
# Methodology and Objectives
This work aims to utilize techniques like AI and machine learning to classify Be stars. With help from numeric simulations, we can generate large clusters of stars synthetically and use that data to train machine learning algorithms to classify stars about wether they are Be or not. 
I tested different methods and used the data to analyze which ones are better fit for the task at hand with the goal to start a walk towards a good algorithm that will be able to rapidly and accurately classify stars en masse.
# Downsampling
Our classes are not balanced, given that Be stars are much less common on the universe than stars that aren't Be. To avoid giving biases to the algorithm, I performed downsampling of the training database. I also tested without downsampling.
# Metrics
Since classes aren't balanced, I had to choose metric that are better suited for this problem. 
# Testing on data from the NGC330 cluster
When I am predicting data from a real cluster, not all Be stars are already found. So the positives the algorithm gives are potential candidates for a Be star. I had to bear that in mind to choose adequate metrics to evaluate the models.
# Calibration
The best suited model for this analysis was the SVM model. I had to use a calibration technique to get the chance a star was a Be in the real cluster, so that I could choose a cut off value and better limit potential candidates. 
# Permutation Feature Importance
Using PFI I was able to evaluate which photometric filters are contributing more to the predictive power of the machine learning algorithm