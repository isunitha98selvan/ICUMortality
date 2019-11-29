### In-hospital mortality prediction

All the preprocessing scripts are present in preprocessing folder.

create_in_hospital_mortality.py creates the time series data.

For LSTM:
       
       python -um models.in_hospital_mortality.main --network models/keras_models/lstm.py --dim 16 --timestep 1.0 --depth 2 --dropout 0.3 --mode train --batch_size 8 --output_dir models/in_hospital_mortality

For logistic regression:
       
       python -um models.in_hospital_mortality.logistic.main --l2 --C 0.001 --output_dir models/in_hospital_mortality/logistic

For SVM classifier:
       python -um models.in_hospital_mortality.svm.main --l2 --C 0.001 --output_dir models/in_hospital_mortality/svm

For decision tree:
	python -um models.in_hospital_mortality.tree.main --l2 --C 0.001 --output_dir models/in_hospital_mortality/tree

For Random Forest:
	python -um models.in_hospital_mortality.forest.main --l2 --C 0.001 --output_dir models/in_hospital_mortality/forest

For KNN:
	python -um models.in_hospital_mortality.knn.main --l2 --C 0.001 --output_dir models/in_hospital_mortality/knn




