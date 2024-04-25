Multiple parallel pipelines are present on git and are used for automation of this pipeline:

2. Data collect(DB, Iot devices(sensors), transactions)-> Apache Kafka(tool if data is from different sources and we want to transform it in single form.) or Apache flink(another tool for transformation for data coming from subscribers)
3. Validate -> verofy quality+ relevance of data domain with goal
4. Curate -> clean +format(remove missing values and outliers) +ensure quality of data
5. Analyse -> find features and patterns, collect insights, + visualizations, correlation, data ready to be given to the model
6. Train -> data should be divided into train 80% and test(validation) 20% data
7. Evaluate -> based on different scores accuracy, f1-scores etc
8. Deploy model-> on production where model predicts on run time

Divide code in modules-> modularization:
  divide code into stages and modules, so that the code can be reusable and we get a proper workflow with proper structure
  1. code is divided into modules(folders and subfolders with py files with relevant code with classes or functions)
     eg model folder with
     like configurations folder (settings/ variables that can be used in different modules+like global variables)
       pre processing folder
       training folder etc
     then we create a pipeline and we tell what module should be running at what part of the pipeline
2. tracing all experiments
3. validate and approve pipelines

Deployment:
(the dockerized model is deployed)
   integration with app
   front end
   containeraization with app
Model Monitoring:
  resource monitoring/trends changing
  Alerts
  
