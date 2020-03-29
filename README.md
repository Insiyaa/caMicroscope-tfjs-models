This repository is further maintained under [camicroscope/tfjs-models](https://github.com/camicroscope/tfjs-models).

# caMicroscope-tfjs-models
Classification and segmentation sample models for caMicroscope.

## Common Issues:
- ***Provided weight data has no target variable***: This might be a common issue for the model to fail to load. To avoid this, make sure that the keras model is loaded exactly once. To make sure, reset the runtime and load the model before carrying to conversion. This case also goes when your converting using the bash command. The Keras model which you saved must be loaded just once. To make sure, save the model, reset the runtime, load the model and save it again. Multiple loads seem to mess up the layer names. You can track this issue further [here](https://github.com/tensorflow/tfjs/issues/755).
- Don't use Keras' Lambda in model definition. If want to use, save weights, remove Lambda calls, load weights again and then save the complete model as .hdf5

Feel free to contribute:).
