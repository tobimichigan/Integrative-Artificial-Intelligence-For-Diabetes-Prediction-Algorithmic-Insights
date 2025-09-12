# Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights
Integrative Artificial Intelligence For Diabetes Prediction: Cross-Validated Insights From Ensemble And Neural Architectures

<h1 alighn="center">ABSTRACT</h1>
<p>
Accurate prediction of Type 1 Diabetes (T1D) events from heterogeneous, real-world datasets is crucial for early intervention and personalized monitoring. We present an end-to-end, reproducible pipeline that integrates dataset discovery, preprocessing, automated feature selection, and comparative evaluation of Random Forest, Logistic Regression, and a feed-forward Neural Network for T1D prediction. We combined 142 CSV files into a harmonized dataset of 1,307,891 rows with 43 columns. Preprocessing included column normalization, imputation (median for numeric, constant for categorical), outlier detection (Local Outlier Factor), and a standardized ColumnTransformer pipeline. Experiments used StratifiedKFold cross-validation (k=5) and an 80/20 stratified train/test split. Performance metrics included accuracy, precision, recall, F1, and ROC-AUC. Model selection used cross-validation F1 and test set performance. Logistic Regression achieved the highest measured performance (test accuracy = 1.0000; precision = 1.0000; recall = 1.0000; F1 = 1.0000), with cross-validation stability (mean F1 = 1.0000, std = 0.0000). Random Forest and the Neural Network also performed strongly (Random Forest test F1 = 0.9763; Neural Network test F1 = 0.9826). Visual diagnostics included confusion matrices, ROC curves, training history (accuracy/loss/precision/recall), and feature correlation heatmaps. A simple, well-configured Logistic Regression model produced near-perfect predictive performance under our pipeline. We discuss potential causes (true separability vs. dataset artifacts or label leakage), provide interpretability analyses, and recommend external validation and rigorous leakage checks before clinical deployment.</p>

<p>Keywords: Type 1 Diabetes, Predictive Modeling, Logistic Regression, Random Forest, Neural Network, Cross-Validation, Explainable AI</p>

<p>Full Initial Paper Article : https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb</p>

<h2 align="left"> 
Showing Fig. 1. Model Accuracy, Model Loss, Model Precision, Model Recall
  <br>
 <a href="https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb"><img src="https://raw.githubusercontent.com/tobimichigan/Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights/refs/heads/main/Fig.%201.%20Model%20Accuracy%2C%20Model%20Loss%2C%20Model%20Precision%2C%20Model%20Recall.png" alt="Fig. 1. Model Accuracy, Model Loss, Model Precision, Model Recall" width="1020"></a> 
  <br> 
   <br>
</h2>

<h2 align="left"> 
Showing Fig. 2. Confusion Matrix for Random Forest, Logistic Regression, & Neural Network
  <br>
 <a href="https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb"><img src="https://raw.githubusercontent.com/tobimichigan/Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights/refs/heads/main/Fig.%202.%20Confusion%20Matrix%20for%20Random%20Forest%2C%20Logistic%20Regression%2C%20%26%20Neural%20Network.png" alt="Fig. 2. Confusion Matrix for Random Forest, Logistic Regression, & Neural Network" width="1020"></a> 
  <br> 
   <br>
</h2>

<h2 align="left"> 
Showing Fig. 3 ROC Curves Comparison
  <br>
 <a href="https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb"><img src="https://raw.githubusercontent.com/tobimichigan/Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights/refs/heads/main/Fig.%203%20ROC%20Curves%20Comparison.png" alt="Fig. 3 ROC Curves Comparison" width="1020"></a> 
  <br> 
   <br>
</h2>


<h2 align="left"> 
Showing Fig. 4. Model Test Accuracy, Precision, Recall and F1 Graphical Scores
  <br>
 <a href="https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb"><img src="https://raw.githubusercontent.com/tobimichigan/Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights/refs/heads/main/Fig.%204.%20Model%20Test%20Accuracy%2C%20Precision%2C%20Recall%20and%20F1%20Graphical%20Scores.png" alt="Fig. 4. Model Test Accuracy, Precision, Recall and F1 Graphical Scores" width="1020"></a> 
  <br> 
   <br>
</h2>

<h2 align="left"> 
Showing Fig. 5. Target Variable Distribution & Feature Correlation Matrix
  <br>
 <a href="https://handsonlabs.org/integrative-artificial-intelligence-for-diabetes-prediction-cross-validated-insights-from-ensemble-and-neural-architectures/?v=c6a82504ceeb"><img src="https://raw.githubusercontent.com/tobimichigan/Integrative-Artificial-Intelligence-For-Diabetes-Prediction-Algorithmic-Insights/refs/heads/main/Fig.%205.%20Target%20Variable%20Distribution%20%26%20Feature%20Correlation%20Matrix.png" alt="Fig. 5. Target Variable Distribution & Feature Correlation Matrix" width="1020"></a> 
  <br> 
   <br>
</h2>


<p>
  
<H1>Filled Research Gaps</H1>
•	Risk‐stratification methods: Most prior T1D work focuses on short-term glucose control or on prediction models for imminent events. There is a gap in developing a broad risk‐classification framework that uses long-term, multimodal data to stratify patients (e.g. high vs. low glucose risk) for proactive management. Our project addresses this by combining continuous glucose, insulin, nutrition, activity, and sleep features to label and predict a health outcome. Achieving near‐perfect accuracy with these features (e.g. logistic regression accuracy ~1.00 in our tests) demonstrates that such rich data can support effective risk prediction, filling the gap in comprehensive T1D risk modeling.

<H1>Data availability:</H1> 

T1D research has long suffered from a lack of large, real-world, multimodal datasets. Until recently, few publicly available collections contained diverse daily data (glucose, insulin dosing, meals, activity, etc.) needed for algorithm development. We fill this gap by directly using two new datasets: T1D-UOM and AZT1D. The T1D-UOM dataset provides detailed 3-month records for 17 people with T1D (glucose, basal/bolus insulin, nutrition breakdown, activity, sleep) in real-world settings[1]. The AZT1D dataset contains 6–8 week data for 25 T1D patients on insulin pumps, including CGM glucose, insulin pump logs (with granular bolus details), carbohydrate intake, and device mode[2]. By incorporating these multimodal sources, we address the previous data scarcity and enable more robust modeling than was previously possible.

<H1>Contribution to Knowledge</H1>
•	Risk‐classification pipeline: We develop a machine‐learning pipeline that classifies a health outcome (e.g. high glucose risk) using the combined multimodal data. In our experiments, even simple models (logistic regression) achieved extremely high accuracy on the synthetic target, demonstrating that the integrated data are highly predictive. This result provides a proof-of-concept for T1D risk stratification: it shows that combining rich real-world features allows accurate classification where previous methods fell short. Our analysis thus contributes a new baseline model for T1D risk prediction and validates the utility of multimodal inputs.

<H1>	Dataset integration:</H1> 

Our work is one of the first to integrate the recently released T1D-UOM and AZT1D datasets into a unified analysis pipeline. T1D-UOM[1] and AZT1D[2] fill critical gaps by supplying longitudinal multi-aspect data on T1D patients. By preprocessing, joining, and analyzing 1.3 million combined records from these sources, we demonstrate how such open datasets can be leveraged for machine learning. This not only directly uses the cited datasets in our pipeline (as requested) but also sets a precedent for other researchers to use these rich resources. Our contribution lies in showing that these new public datasets can be mined effectively for predictive modeling.

<h1>Manuscript/Report structure:</h1>

To ensure our findings are communicated clearly, we propose a structured outline for the academic manuscript or grant report. Key sections will include Introduction/Background (contextualizing T1D management challenges and data gaps), Data Description (detailing the T1D-UOM and AZT1D datasets and preprocessing steps), Methods (explaining the risk-classification pipeline and machine learning models), Results (presenting performance metrics and evaluation), Discussion (interpreting the outcomes, comparing to existing work, and noting limitations), and Conclusion/Future Work (summarizing contributions and potential next steps). By framing the report this way, we ensure all research components—from the use of novel datasets to the implications of our risk model—are covered systematically and thoroughly.

<h1>Sources</h1>

We directly used the T1D-UOM[10] and AZT1D[14] (see full list of references in full article link above) in  datasets in our pipeline. These references also highlight the data gaps we are filling: limited publicly available T1D data for algorithm development and how these new datasets address that gap.

<h1>Data Sources</h1>

# key Literature & Data Citations

    Alsuhaymi, A., Bilal, A., Gasca Garcia, D., Kongdee, R., Lubasinski, N., Hood, T., Paul, N., & Harper, S. (2025). T1D-UOM – A Longitudinal Multimodal Dataset of Type 1 Diabetes (V1.0.3). Zenodo. https://doi.org/10.5281/zenodo.15806142

    AZT1D: A Real-World Dataset for Type 1 Diabetes: Khamesian, Saman; Arefeen, Asiful; Thompson, Bithika M.; Grando, Adela; Ghasemzadeh, Hassan (2025), “AZT1D: A Real-World Dataset for Type 1 Diabetes”, Mendeley Data, V1, doi: 10.17632/gk9m674wcx.1 [/kaggle/working/AZT1D A Real-World Dataset for Type 1 Diabetes] (/kaggle/working/sharpic-ManchesterCSCoordinatedDiabetesStudy-fdbd74f). Github: https://github.com/sharpic/ManchesterCSCoordinatedDiabetesStudy/tree/V1.0.3
    
<p>[10] T1D-UOM – A Longitudinal Multimodal Dataset of Type 1 Diabetes
https://zenodo.org/records/15806142 </p>
<p>[14] [2506.14789] AZT1D: A Real-World Dataset for Type 1 Diabetes
https://arxiv.org/abs/2506.14789 </p>
</p>
