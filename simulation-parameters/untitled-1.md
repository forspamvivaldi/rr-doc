# 🔩 Workpiece mesh

![](../.gitbook/assets/simulation-paramaters-workpiece-mesh.png)

_Mesh adaptation in workpiece_ — control the adaptation of the computational mesh. The size of the elements of the computational mesh in the workpiece in the contact area with the tool corresponds to the dimension of the maximum element of the initial mesh that is divided by the specified value of the adaptation factor. By default, the optimal value of the maximum adaptation factor \(_Adaptation in the contact zone_\) is specified equal to 10.

Influence of different parameters on the **computational mesh** \(read further about dual mesh method and computational mesh\).

By default:

 ![](../.gitbook/assets/2.-computational-mesh-by-default.png) 

\_\_

_Adaptation factor_ — 2 \(size of the mesh in the whole volume of the ring are smaller in 2 times than with default parameters\):

 ![](../.gitbook/assets/2.-computational-mesh-adaptation-factor-2.png) 

\_\_

_Adaptation in the contact zone_ — 15 \(size of the mesh in the contact zones are smaller in 2 times than with default parameters\):

 ![](../.gitbook/assets/2.-computational-mesh-adaptation-in-contact-zone-15.png) 



Influence of different parameters on the **geometrical mesh** \(read further about dual mesh method and geometrical mesh\)

By default:

 ![](../.gitbook/assets/2.-geometrical-mesh-by-default.png) 

_Adaptation factor_ — 2_:_

![](../.gitbook/assets/2.-geometrical-mesh-adaptation-factor-2.png) 

_Minimum adaptation_ — 6_:_

![](../.gitbook/assets/2.-geometrical-mesh-minimum-adaptation-6.png) 

