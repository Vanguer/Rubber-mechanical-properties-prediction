# DNN model for predicting mechanical properties of carbon black filled rubber composites
Here, we present the deep neural network (DNN) model and the calculated Pareto front in the paper, hoping to provide inspiration for the process design of carbon black-filled rubber composites(CRC).

## File description

- strength.h5:

  DNN model for predicting CRC yield strength

- elongation.h5:

  DNN model for predicting CRC elongation at break

- log-fatigue.h5：

  DNN model for predicting CRC tensile fatigue life

- pareto points.xlsx：
  
  The Pareto front point calculated based on the prediction results of the DNN model

## Dependencies

1. Install Anaconda <https://www.anaconda.com>
2. Create a virtual environment
3. Activate this virtual environment
4. Install [Tensorflow](https://www.tensorflow.org/get_started/os_setup), [Pandas](https://pandas.pydata.org/getting_started.html), [Numpy](https://numpy.org/install)

## Using
  An example:
  
 ```shell
  data = pd.read_csv('data.csv')
  model = tf.keras.models.load_model('strength.h5')
  predict_results = model.predict(data)
  ```
  Notice:
In actual use, the predicted values ​​of the DNN model need to be multiplied by 40(strength), 7(log-fatigue), 700(elongation) respectively.

## Cite
 If you use any of our data or code, partly or as it is, please cite our paper.
