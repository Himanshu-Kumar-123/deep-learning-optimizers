## Optimizers

### Major problem of Gradient Descent approach - (can’t reach global minima):

#### Getting stuck in local minima -

![Optimizer Image 1](image1.png)

![Optimizer Image 2](image2.png)

#### Saddle points : Minima in one direction but maxima in another direction.

![Optimizer Image 3](image3.png)

---

Optimizers help to reach the global minima of loss curve with higher probability.

---

### Different variants of Optimizers :

---

#### 🔸 Momentum based Gradient Descent :

Gradient Descent uses only the current gradient (point gradient).

**Update Rule:**

![Optimizer Image 4](image4.png)

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

