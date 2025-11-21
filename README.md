# Average-Fork-Length-in-Campbell-Creek
Morgan Lemmings-https://github.com/morganlemmings
Melissa Tran-https://github.com/melissatran0
Mahathi Bodhanapalli-https://github.com/mrb74060
Jason Goldblatt-https://github.com/jasongold3
Clark Farrell-https://github.com/clarkfarrell2



The dataset contains 402 rows and 5 columns of juvenile salmon measurements from Campbell Creek in Alaska. It includes reach ID, fork location, fork length from snout to tail split, species, and dates. Fork length is numeric while the other fields are categorical or date type.







Question 1: What is the average fork length of Chinook vs. Coho salmon across all reaches, and how does it vary by fork (Main Stem, North Fork, South Fork)?

Importance: The average fork length is a strong indicator of fish health, growth rate, and habitat quality. By comparing these two species of salmon, we can identify species-specific habitat use within each fork of Campbell Creek. The different sizes across the Main Stem, North Forth, and South Fork can reveal which areas support growth faster and which areas may be less productive. Differences by location help agencies understand localized habitat conditions, such as food availability, water temperature, or flow differences. Understanding which forks produce larger salmon can guide management strategies that support long-term fishery sustainability. By using this data, we can sustain healthy salmon populations that ensure the continuation of traditional fishing practices and cultural heritage since salmon have a deep cultural significance for Indigenous communities residing in Alaska. 

Question 2: Can we predict the fork length of a salmonid based on the sampling reach and date of capture during the 2021 Campbell Creek study?

Importance: As stated above, fork length is a key indicator for understanding fish health, growth rate, and the quality of the habitat. Being able to predict fork length can reveal spatial and seasonal growth patterns. Predictive models will help identify habitats that produce faster-growing fish. Predictive models also help biologists anticipate when and where salmon will reach key size thresholds. Modeling growth over time will also aid in detecting shifts in timing, such as early or delayed seasonable development due to climate or flow changes. The data for fork length, species, date of capture, and sampling reach are once again the needed variables to answer the predictive analysis question. Reach represents spatial variation, while the date represents temporal variation, making them ideal predictors of growth.

Manipulations applied to the data set of analysis: 

To prepare the data for analysis, we first deleted any rows with missing fork length values in Excel so that only valid measurements were used in Tableau.

Question 1: —Removing the null values from the fork length column improves the quality and reliability of the analysis because it ensures that only real measured lengths are used when Tableau calculates the averages. If null values had been left in the data they would not contribute any information but they could still affect how Tableau groups or counts the records. By taking them out you prevent the averages from being influenced by missing entries and you avoid situations where certain species or forks appear to have fewer or oddly skewed values simply because some observations had no recorded length. This makes the final chart more accurate since every bar represents only actual measured fork lengths and every comparison between species months and fork locations is based on complete usable data rather than a mixture of real numbers and missing measurements.



Question 2: The date field was set to a continuous format, which allowed us to create line charts and look at changes over time. Fork length values were averaged to reduce the impact of outliers and make comparisons clearer across different reaches and species. We grouped the data by both reach and species so that patterns could be visualized more easily. Trend lines were added to the line charts to show how fork length changed with date, and Tableau displayed the equations and R² values to measure how strong those relationships were. Finally, we used Tableau’s forecasting tool to project fork lengths beyond the study period, adjusting the forecast length and confidence intervals to fit the dataset.

Results Summary:
Question 1: 
Explanation: This chart shows how average fork length of salmon changes by month, species, and river fork location. The two species shown are chinook on the left and coho on the right. Each species has three locations which are Main Stem, North Fork, and South Fork. Within each location the bars show the average fork length for June, July, August, and in some cases September.
Key points for chinook: In the Main Stem chinook are longest in June at about 80 cm then decrease through July and August.
 In the North Fork chinook show a similar pattern since June and July hold the smaller values with a small rebound in September.
 In the South Fork the smallest values occur in August while the largest values appear in September. Chinook in the South Fork also tend to be slightly longer in general than those in the North Fork.
Key points for coho: In the Main Stem coho are longest in June and decline each month through August.
 In the North Fork coho again start highest in June and steadily decrease into August and September.
 In the South Fork coho show a similar trend dropping from June to August then slightly rising in September.
Overall observations: Fish are generally longest in June across almost every species and fork.
 Lengths usually decline as the summer progresses likely due to sampling of younger fish later in the season.
 Chinook have higher fork lengths in general than coho.
 The South Fork tends to show the smallest August values while September rebounds slightly.

Question 2:
Analysis of the trend lines revealed several important growth patterns across reaches and species. Main Stem Coho and South Fork salmon (both Coho and Chinook) showed clear positive growth over time, while North Fork salmon exhibited little to no growth, with Coho remaining flat and Chinook declining. Main Stem Chinook also declined slightly, indicating mixed results within that reach. Overall, the South Fork emerged as the most consistent location for growth across both species, whereas the North Fork proved to be the weakest predictor, with flat or negative slopes. Species differences were also evident: Coho generally displayed stronger positive growth slopes than Chinook, whose growth was highly location-dependent, positive in the South Fork but negative in the Main Stem and North Fork. These regression equations can be used to predict fork length for any given day and reach. For example, on Day 20 in the South Fork, the predicted Coho fork length is approximately 58.1 mm, calculated as 0.44217×20+49.25
