# 🕹️ Advanced

![Advanced parameters tab](../.gitbook/assets/3.-advanced-1.png)







## Velocity depends on load and torque

**Mandrel velocity depends on load and torque \(on the main roll\)**  activation of this feature allows to control the mandrel motion due to load on mandrel and torque on the main roll.

![](../.gitbook/assets/3.-mandrel-velocity-depends.png)

**Axial roll velocity depends on load and torque** — activation of this feature allows to control the vertical motion of axial roll due to load and torque on the axial roll.

![](../.gitbook/assets/3.-axial-roll-velocity-depends.png)

![](../.gitbook/assets/3.-velocity-depends-on-load-and-torque.png)











## The relative speed difference

### Main roll and axial rolls

By default, the program calculates the rotational speed of axial rolls to exclude the slipping and pushing between axial rolls and ring, i.e. linear velocities on contact are equivalent and there is no deviation of the ring relative central rolling line. Linear \(tangential\) velocity of the ring rotation corresponds to the linear \(tangential\) velocity on the main roll rotation.

By using this option it is possible to control the relative speed difference between main roll and axial rolls in contact with ring.

To describe the relative speed difference between main roll and axial rolls is used right coordinate system \([right-hand rule](https://en.wikipedia.org/wiki/Right-hand_rule?oldformat=true)\). It means that to increase the relative speed of axial rolls it is necessary to set the value below zero. For instance, -10% \(top view on geometry\):

![Deviation of the ring by means of relative speed difference between main roll and axial rolls](../.gitbook/assets/3.-main-roll-and-axial-roll-difference.png)









### Upper and bottom axial rolls

It is possible to set the relative speed difference \(speed of rotation\) between upper and bottom axial rolls. To increase the relative speed of the upper axial roll it is necessary to set the value above zero.

For instance: value +10% means that rotational speed of upper axial roll will be on 10% greater than on the bottom axial roll \(cross cut of the ring in the axial gap\):

![Difference in the tangential velocity by means of relative speed difference between upper and bottom axial rolls](../.gitbook/assets/3.-upper-and-bottom-axial-roll-difference.png)















## Reducing/Axial gap

![](../.gitbook/assets/3.-reducing.-axial-gap.png)

To describe the last stage of the ring rolling it is possible to use _Reducing/Axial gap_ option. Axial roll will move up on the _Gap_ value until the some distance to the final position \(_Reducing_\) of the mandrel.

![](../.gitbook/assets/3.-reducing.-axial-gap-2.png)







## Rotation taking into account horizontal table

![](../.gitbook/assets/3.-rotation-with-deviation-from-horizontal-plane.png)

Activation of this option will add an invisible boundary condition on ring.

Also, you could use Table like a real object \(Plate in QForm interface\) for the more accurate calculation. The table should contain two halves with the web between them. Web should be in the bottom part of the table to exclude the intersection with ring. Intersection with bottom axial roll does not have an affect on simulation.

![Two parts of the table with web between them](../.gitbook/assets/3.-table-with-web.png)

