# RF-MPC

Representation-Free Model Predictive Control (RF-MPC) is a MATLAB simulation framework for dynamic legged robots. RF-MPC represents the orientation using the rotation matrix and thus does not have the singularity issue associated with the Euler angles. The linear dynamics on the rotation matrix is derived using variation-based linearization (VBL).

![](https://i.imgur.com/mvZZUCj.gif)

video available at: [YouTube Video](https://www.youtube.com/watch?v=iMacEwQisoQ&t=101s)


## Requirement
Basic: MATLAB and MATLAB optimization toolbox

Optional: qpSWIFT (an efficient QP solver to MPC problems)

## Installation
There is no need to install external packages.

## Usage
navigate to the root directory and run the MAIN.m function

``` MATLAB
MAIN
```
### The Plant
The robot is modeled as a single rigid body (SRB). The SRB dynamics is defined in
``` MATLAB
...\fcns\dynamics_SRB.m
```

### VBL and vectorization
The code for variation-based linearization and vectorization steps is in
``` MATLAB
...\fcns_MPC\fcn_get_ABD_eta.m
```

### Quadratic Program (QP)
The code for QP formulation is in
``` MATLAB
...\fcns_MPC\fcn_get_QP_form_eta.m
```
The QP could be solved by either the MATLAB QP solver *quadprog* or a efficient QP solver qpSWIFT (coming soon!)



## References
This code is based on the following publications:
* Yanran Ding, Abhishek Pandala, and Hae-Won Park. "Real-time model predictive control for versatile dynamic motions in quadrupedal robots". In IEEE 2019 International Conference on Robotics and Automation (ICRA). [PDF](https://ieeexplore.ieee.org/abstract/document/8793669)
* Yanran Ding, Abhishek Pandala, Chuanzheng Li, Young-Ha Shin, Hae-Won Park "Representation-Free Model Predictive Control for Dynamic Motions in Quadrupeds". In IEEE Transactions on Robotics. [PDF](https://arxiv.org/abs/2012.10002)

## Authors
[Yanran Ding](https://sites.google.com/view/yanranding/home) - Initial Work/Maintainer

## Contributing
For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgments
* Thanks to co-authors and mentors
