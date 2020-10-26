# 🪐 Axis setting

## Evolution of the axis setting in QForm

![](../.gitbook/assets/evolution-of-axis-setting.png)













## Automatically

1. load the 3D geometry from step-format directly in QForm.
2. Go to the _Axes_ tab.
3. Select all objects \(by using _Shift_ button\) and press the button **Compute all axes.**

![](../.gitbook/assets/axis%20%282%29.gif)











## Semi-automatically

It is possible to set axes automatically in QShape. The geometry file should contain all objects for simulation. Use [STEP](https://en.wikipedia.org/wiki/ISO_10303-21?oldformat=true) format to load geometry in QShape.

1. Select a _Shell_ in _Model_ window
2. Press the button _Mesh generation_ in _Operations_ window
3. Select the cylindrical or conical surface on created _Solid_ object \(or on another more difficult surface of rotation\) and press the button _Use face axis as Axis 1_
4. Convert _Solid_ object into the tool from _Ring rolling object_ list

![Setting of the axis in QShape](../.gitbook/assets/4.-automatic-axis.gif)





## Manually

It is necessary to use mannual approach to set two [second axes](https://danila-master.gitbook.io/documentation-ring-rolling/v/v-9.1/geometry-preparation/geometry-requirements) for guide rolls. Coordinates of these axis depends on the concret ring rolling mill. To set axis manually:

1. Go to the **axes** tab
2. Select one of the guide rolls
3. Activate the _Axis 2_ option \(put a tick opposite _Axis 2_\)
4. Specify coordinate of the Start point \(it should be the coordinate of the any point on the axis\)
5. Select the radio button Direction and specify the Z-axis direction and length of the axis \(it could be any number, for example 600 or 1000\)

![](../.gitbook/assets/axes-manually.gif)

