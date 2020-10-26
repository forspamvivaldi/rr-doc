# Chain of the ring rolling operation

Some technology contains a few ring rolling operations with intermediate heating. Such sort of technologies could be used for the deformation of high-strength materials: titanium alloys, nickel alloys, superalloys and etc.

Our recommendations for creating the next ring rolling operation \(2nd, 3rd, etc\):

* to create a new operation use _Copy data from previous operation_ with active option _Inherit data from previous operation_
* in _Workpiece parameters_ tab select the option for the Temperature - _Defined for current operation_ \(to imitate the heating operation\)
* then, set the initial temperature of ring for this operation
* the same think better to do with _Accumulated effective strain_ - select _Defined for current operation_
* then, set the value of _Accumulated effective strain_ equal 0 \(to imitate zeroing of the plastic strain after heating operation\)

![Zeroing of the plastic strain after heating operation](.gitbook/assets/chain-of-operations.png)

* all other parameters it is necessary to set according to the technology

