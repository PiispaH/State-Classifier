# State-Classifier

A quantum machine learning model for detecting if a diagonal bell state is separable or not.

## Data generation
Diagonal Bell states are created with randomised probability coefficients. The separability
of the states are checked and saved as a labels for the data points. The features for the ML
model are made by taking XX, YY and ZZ Pauli measurements of the states. The features are scaled to
the interval [0, 2*Pi].

## QML model
The classical features are encoded to the quantum circuit with phase gates and entangling gates.
The rest of the quantum circuit acts as a neural network, where weights are updated by a classical
optimiser to minimize the loss function. The Pauli Z observable measurements made at the end of the
circuit act as the output of the QNN.

## To run:
1. Clone the repository.
2. Create and activate a virtual environment.
3. In project root run
    ```
    pip install .
    ```
    to install all the dependencies.
4. Run the `model.ipynb` file.
