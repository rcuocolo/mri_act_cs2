# Atypical cartilaginous tumor and G2 chondrosarcoma classification project data

Model data developed with scikit-learn for the classification of cartilaginous tumors using radiomics data from T1-weighted MRI images.
The "Files" folder contains the trained model (as a pickled Python object, "ET.pkl") that can be employed on new data prepared following the study processing pipeline.

# Preparing the data

The model was trained on radiomic data extracted using [PyRadiomics](https://pyradiomics.readthedocs.io/en/latest/). Using bidimensional masks and the settings file ("params.yaml") included in the repository, an appropriate test set can be obtained from any cartilaginous tumor MRI exam including non-contrast T1-weighted images.
The extracted data should then be scaled by using the pickled Python objects also included in the repository. The pickled feature list ("features_scaler.pkl") contains the feature set on which to apply the scaler, while the scaler object ("scaler.pkl") contains the scikit-learn MinMaxScaler that can be loaded and fitted to the new data.
Finally, from the resulting, scaled dataset the features actually employed to train the model should be selected (included in the "features_model.pkl" file). The resulting data can now be used by the included trained model to obtain new predictions.

## Citation

- Gitto S, Cuocolo R, van Langevelde K, et al (2022) MRI radiomics-based machine learning classification of atypical cartilaginous tumour and grade II chondrosarcoma of long bones. EBioMedicine 75:103757. [https://doi.org/10.1016/j.ebiom.2021.103757](https://doi.org/10.1016/j.ebiom.2021.103757)

## License

Creative Commons Attribution 4.0 International (CC-BY-4.0). See "LICENSE" file for full details.
