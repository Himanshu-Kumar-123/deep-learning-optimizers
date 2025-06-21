## Optimizers

### 🔸 Gradient Descent

Also known as **Batch Gradient Descent**.

- Gradient Descent uses only the current gradient (point gradient).

**Update Rule:**

$$
w_{t+1} = w_t - \alpha \cdot \frac{dL}{dw_t}
$$

Where:  

$w_t$ → weight at time step $t$  
$\alpha$ → learning rate  
$\frac{dL}{dw_t}$ → gradient of the loss function w.r.t. $w_t$  
$w_{t+1}$ → updated weight for the next iteration

#### Major problem of Gradient Descent approach - 
Can’t reach global minima

- Getting stuck in local minima -

![Optimizer Image 1](images/minima.jpg)

![Optimizer Image 2](images/minima2.jpg)

- Saddle points : Minima in one direction but maxima in another direction.

![Optimizer Image 3](images/saddle.jpg)

---

Different **Optimizers** help to reach the global minima of loss curve with higher probability.

---

### Different variants of Optimizers :

---

#### 🔸 Momentum based Gradient Descent :

Gradient Descent uses only the current gradient (point gradient).

**Update Rule:**

$$
w_{t+1} = w_t - \alpha \cdot \frac{dL}{dw_t}
$$

Where:  
$w_t$ → weight at time step $t$  
$\alpha$ → learning rate  
$\frac{dL}{dw_t}$ → gradient of the loss function w.r.t. $w_t$  
$w_{t+1}$ → updated weight for the next iteration


Momentum based Gradient Descent uses both historical and current gradient info.

**Update Rule:**

![Optimizer Image 5](image5.png)

![Optimizer Image 6](image6.png)

Gamma here is a hyperparameter.

`momentum_t` is an accumulator variable.

![Optimizer Image 7](image7.png)

Orange ball → Momentum based GD  
Blue ball → Vanilla GD

Note that momentum based GD takes more time or more oscillations to settle down than vanilla GD because of the “history” it carries.

