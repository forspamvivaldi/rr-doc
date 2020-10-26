# Basic

![Basic parameters tab](../.gitbook/assets/basic%20%284%29.png)

## Ring rolling mill

![Ring rolling mill data base](../.gitbook/assets/1.-rr-mill-db.png)

{% hint style="info" %}
To take into account the power parameters of the ring rolling mill it is necessary to activate corresponding [options](https://danila-master.gitbook.io/documentation-ring-rolling/process-parameters/advanced#velocity-depends-on-load-and-torque).
{% endhint %}

### **Mandrel**

_Nominal mandrel load \[MN\]_ — maximum mandrel velocity starts to decrease when this value is reached.

_Maximum mandrel load \[MN\]_ — load on mandrel can't be greater than this value.

_Maximum mandrel velocity at nominal load \[mm/s\]_ — mandrel velocity can't be greater than this value.

_Mandrel idle velocity \[mm/s\]_ — the velocity of the mandrel before the contact with a ring.

_Mandrel velocity to lamination curve \[mm/s\]_ — the velocity of mandrel motion \(in contact with ring\) before the reaching of the initial point on ring rolling curve.

### **Main roll**

_Nominal main roll torque \[kN/m\]_ — maximum mandrel velocity starts to decrease when this value is reached.

_Maximum main roll torque \[kN/m\]_ — torque on the main roll can't be greater than this value.

_Maximum rotational velocity of main roll at nominal torque \[rpm\]_ — rotational velocity of the main roll can't be greater than this value.

### **Guide roll**

_Maximum guide rolls velocity \[mm/s\]_ — guide rolls velocity can't be greater than this value.

_Maximum summary load of guide rolls \[MN\]_ — load on both guide rolls can't be greater than this value.

### **Axial roll**

_Nominal load of axial roll \[MN\]_ — maximum velocity of motion of axial rolls start to decrease when this value is reached.

_Maximum load of axial roll \[MN\]_ — load on axial roll can't be greater than this value.

_Maximum axial roll velocity at nominal load \[mm/s\]_ — axial roll velocity of motion can't be greater than this value.

_Axial roll idle velocity \[mm/s\]_ — the velocity of the axial roll before the contact with a ring.

_Axial roll velocity to lamination curve \[mm/s\]_ — the velocity of axial roll motion \(in contact with ring\) before the reaching of the initial point on the ring rolling curve.

_Nominal axial roll torque \[kN\m\]_ — maximum velocity of motion of axial rolls start to decrease when this value is reached.

_Maximum axial roll torque \[kN\m\]_ — torque on axial roll can't be greater than this value.

## Rotation speed of main roll

![](../.gitbook/assets/1.-rotation-speed-of-main-roll.png)

It is necessary to choose one of the variants of setting the rotational speed of the main roll: angular velocity or linear velocity.

For both variants possible to set constant value or table function depends on the outer diameter of the ring.

## Guide rolls

![](../.gitbook/assets/1.-load-on-guide-rolls%20%281%29.png)

### Load on guide rolls

Load on guide rolls is specified in percent from _Maximum summary load of guide rolls_ \(Ring rolling mill database\). Load on guide rolls may be set constant or table function \(dependent on the current ring diameter\).

> Guide rolls have a great influence on the stability of the process and on the results of the simulation. So, if in a real process you have guide rolls use them in a simulation too.

### Deviation of guide rolls axis

To describe the deviation of the guide rolls from the central rolling line is used the right coordinate system \([right-hand rule](https://en.wikipedia.org/wiki/Right-hand_rule?oldformat=true)\).

![](../.gitbook/assets/1.-right-coordinate-system.png)

![Guide rolls deviation ](../.gitbook/assets/1.-guide-rolls-deviation.png)

In practice, this feature is used together with [relative speed difference between main roll and axial rolls](advanced.md#main-roll-and-axial-rolls).

## Displacement of axial rolls

### Horizontal

There are a few variants of Horizontal motion settings:

* _Automatically_ \(by default\). The horizontal velocity of axial rolls is equal half of the ring grow speed.
* _Table_. The horizontal velocity of axial rolls is dependent on the current ring diameter.
* _Starting from specified diameter_. Axial rolls start to move when specified ring diameter is reached.  The velocity of axial rolls is equal to the ring grow speed.

### Vertical

* _Movement only upper roll_. Shifting only the upper axial roll.
* _Upper/Lower symmetrical_. Upper and lower rolls move towards each other or in opposite directions with the same velocity. 
* _Upper/Lower in ratio_. Upper and lower rolls are moved toward each other or opposite sides with the specified velocity ratio. 



## The motion of the mandrel and both cones

There are a few variants of setting the motion of the mandrel and axial rolls:

* Ring rolling curve / Ring grow speed
* Velocity
* Mandrel velocity / Ring height
* Mandrel circular motion

Select one of these variants depending on what type of ring rolling machine you have:

![](../.gitbook/assets/1.-the-position-of-mandrel-and-both-cones.png)

### 

### Ring grow speed / Ring rolling curve

![Ring rolling curves](../.gitbook/assets/1.-rrc.png)

By default in the calculation is used adaptive algorithm: calculation of the velocity of the mandrel and axial roll are based on a current outer diameter of the ring.

It is necessary to specify two tables:

**Ring rolling curve** — the height of the ring depends on the thickness of the ring.

![](../.gitbook/assets/1.-rrc-table.png)

**Ring grow speed** — ring grow speed depends on the outer diameter of the ring.

![RGS table](../.gitbook/assets/1.-rgs-table.png)

It is necessary to know the current thickness, height, and the outer diameter of the ring to find the current velocity of tools according to these graphs:

* thickness calculation depends on the distance between the main roll and mandrel axis \(_X_\), the radius of the main roll, and the radius of mandrel

$$
\text {Thickness }=X-R_{\text {main roll}} -R_{\text {mandrel}}
$$

* height is calculated automatically according to the axial rolls geometry
* the outer diameter can be calculated as maximum outer diameter or diameter on some Z level; depends on what is specified in _Stop conditions tab_:  _maximum diameter_ or _diameter at Z level_.

#### **The stage before the RRC**

Velocities of the mandrel and axial roll before the reaching of the first point in RRC are determined according to the parameters from the ring rolling mill database:

* _Mandrel idle velocity_
* _Mandrel velocity to lamination curve_
* _Axial roll idle velocity \[mm/s\]_
* _Axial roll velocity to lamination curve \[mm/s\]_

![](../.gitbook/assets/1.-stage-before-rrc.png)

### 

### Velocity

**Radial velocity** table — velocity of mandrel motion toward the main roll.

![](../.gitbook/assets/1.-radial-velocity.png)

**Axial velocity** — velocity of reducing the axial gap \(the gap between axial rolls\).

![](../.gitbook/assets/1.-axial-velocity.png)

### 

### Mandrel velocity/ring height

It is necessary to specify two tables:

**Radial velocity** — velocity of the mandrel depends on the outer diameter of the ring.

![](../.gitbook/assets/1.-radial-velocity-vs-diameter.png)

**Ring height** — the height of the ring depends on the outer diameter of the ring.

![](../.gitbook/assets/1.-ring-height-vs-diameter.png)

### Mandrel circular motion

You could see the explanation for this type of tools motion on the figure below.

Source: ASM Handbook Vol. 14 - Forming and Forging

![](../.gitbook/assets/1.-mandrel-circular-motion.png)

Schematic showing principle of operation of a four-station mechanical \(radial\) ring rolling mill. The ring blank is loaded at position 1. Rolling begins at position 2 and is completed at position 3. The finished ring is unloaded at position 4. A, driven roll; B, mandrels; C, guide rolls.

It is necessary to specify an additional \(second\) axis for mandrel for this type of technology. The red dot on the picture above shows the position of the second mandrel axis.

It is necessary to specify one parameter for this type of tools motion:

**Rotation velocity about Axis 2 \[rpm\]** — The rotational speed of the mandrel around the second axis.



## Diameter of the main roll

It is necessary to specify the diameter of the main roll.

The diameter of the main roll is used:

* to find the rotational speed of the main roll by using _Linear velocity_
* to find the current thickness of the ring

> current thickness of ring is used to determine the velocity of the mandrel and axial roll \(if RRC and RGS are used\)



## Diameter of the mandrel

It is necessary to specify the diameter of the main roll.

The diameter of the main roll is used to find the current thickness of the ring.

