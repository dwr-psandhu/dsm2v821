# Input Gate

## Overview:

Gate inputs are time series assignments to gate structure physical and
operational parameters.

## Tables:

-   [INPUT_GATE](http://msb-confluence/display/DSM2/Input+Gate#InputGate-input_gate)

### INPUT_GATE

A gate input assigns time varying properties to
to [gate](file:///U:/dsm2/doc/html/reference/gate.html) parameters, The
table assigns a time series data source.

#### Field Descriptions

##### GATE_NAME

This must be the same as the name of the gate.

##### DEVICE

This must be the same as the name of the gate device. Generally all the
variables except "install" are device specific. If the variable is
"install" set the device to "none".

##### VARIABLE

The variable that is set by this assignment.

##### FILLIN

Method for filling in data if the time step of the assigned series is
coarser than the time step of the model. See fillin types

##### FILE

DSS or text file in which data are stored. Use consistent case when
referring to the same file. You may also enter the word constant if you
would like to assign a constant value to the input (the value will be
entered in the next column).

##### PATH

The path within the text or DSS file of the time series data. If you
used the constant keyword in the Input File column, enter the value
(e.g. 4.22) here.

#### Table Info

##### Identifier:

NAME

##### Include Block:

HYDRO_TIME_SERIES
