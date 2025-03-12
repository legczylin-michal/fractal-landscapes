# Surface fractal interpolation

A jupyter notebook with implemnatation of fractal surface interpolation and brownian mothions in 3d.

## Interpolation
Based on initial points in 3d space creates continuous (as number of generated points tends to infinity) surface that interpolates the unknown one to which initial points belong.
Fractal interpolation is used which means that group of initial points is affinely transformed into many new groups each covering a part of original 2d domain but together covering the whole 2d domain of original initial points.

## Brownian motions
Brownian motion or Wiener's process is a stochastic process which satisfies 4 conditions:
1. $W_0=0$,
2. $\forall_{0 \leq t < s}\hspace{0.25cm}W_s - W_t \sim \mathbb{N} (0, s - t)$,
3. $\forall_{n \in \mathbb{N}}\hspace{0.25cm}\forall_{0 \leq t_1 < t_2 < t_3 < ... < t_{n-1} < t_n}\hspace{0.25cm}(W_{t_2} - W_{t_1}) {\perp\perp} (W_{t_3} - W_{t_2}) {\perp\perp} ... {\perp\perp} (W_{t_n} - W_{t_{n-1}})$,
4. $\forall_{\omega \in \Omega}\hspace{0.25cm}X_{\bullet}(\omega): T \to R$ is a continuous function.
In our project modified version, named fractional Brownian motion, is used to randomly generate surface in 3d.

## Usage
What are they for? Fractal interpolation, well like with regular ones, can be used to either recreate desired surface based on passes points (data recovery after compression) or to approximate the surface we are looking for.
While Brownian motion finds its uses in games for generating landscapes etc.

## Examples
|![Initial points forming pyramid — one at the center at height 1 and four around it at height 0](img/pyramid_data.png "Initial points")|
|:--:| 
| *Initial points* |

|![Interpolated surface forming hill-like shape](img/pyramid_pred.png "Interpolated surface")|
|:--:| 
| *Interpolated surface* |

|![Initial points normally distributed on uniform cube](img/random_normal_data.png "Initial points")|
|:--:| 
| *Initial points* |

|![Interpolated surface rather looking noncontinuous due to finite number of points](img/random_normal_pred.png "Interpolated surface")|
|:--:| 
| *Interpolated surface* |

|![Dense grid of uniformly selected initial points on uniform square as arguments for sin(x^2 + y^2) function](img/sin_of_sum_of_x_sq_and_y_sq_true.png "Initial points")|
|:--:| 
| *Initial points* |

|![Interpolated surface strongly resembling original function, though seems to be thicker due to fractality](img/sin_of_sum_of_x_sq_and_y_sq_pred.png "Interpolated surface")|
|:--:| 
| *Interpolated surface* |

### Credits
Developed by Piotr Kosakowski and Michał Legczylin.
