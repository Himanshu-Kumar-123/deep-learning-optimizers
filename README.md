## 🔍 Optimizer Comparison Summary

This project compares the performance of several popular optimizers on a classification task. The training and validation metrics were observed over 20 epochs.

---

### 🧪 Optimizers Evaluated

#### 1. **SGD (No Momentum)**
- 🐌 Training loss decreases slowly and inconsistently.
- 📉 Validation loss improves slightly but remains high.
- ❌ **Conclusion:** Very slow convergence, prone to getting stuck. Least effective.

#### 2. **SGD + Momentum**
- 🚀 Faster and smoother training loss reduction.
- 📈 Validation accuracy improves steadily.
- ⚠️ Slight overfitting after peak performance.
- ✅ **Conclusion:** Best balance of stability and generalization.

#### 3. **Adagrad**
- ⚡ Quick performance gains in early epochs.
- 🔄 Validation loss plateaus early due to aggressive learning rate decay.
- ❌ **Conclusion:** Good starter, but underfits with time. Suitable for sparse data or early convergence.

#### 4. **RMSProp**
- 📉 Steady decrease in training loss.
- ⚠️ Validation loss fluctuates heavily.
- ❌ **Conclusion:** Sensitive to hyperparameters. Unstable generalization in this setup.

#### 5. **Adam**
- ⚡ Very fast training loss reduction.
- ⚠️ Validation loss highly erratic; overfitting observed.
- 🔄 Spikes in loss toward the end.
- ❌ **Conclusion:** Overfits quickly. Needs careful tuning or regularization.

---

### 📊 Summary Table

| Optimizer        | Training Convergence | Validation Stability | Generalization       |
|------------------|----------------------|-----------------------|------------------------|
| **SGD**              | ❌ Slow               | ⚠️ Flat                | ❌ Poor                |
| **SGD + Momentum**   | ✅ Stable             | ⚠️ Slight overfit      | ✅ Good                |
| **Adagrad**          | ✅ Fast (early)       | ⚠️ Plateaus early      | ❌ Underfits (later)   |
| **RMSProp**          | ✅ Good               | ❌ Highly unstable     | ❌ Inconsistent         |
| **Adam**             | ✅ Very fast          | ❌ Very unstable       | ❌ Overfits / erratic   |

---

### 🏁 Final Insight

- 🏆 **Best Overall**: **SGD + Momentum** — stable, generalizes well.
- 🛠️ **Use With Tuning**: **Adam**, **RMSProp** — strong learners but need regularization.
- ⚠️ **Avoid for long runs**: **Adagrad** — can underfit after early performance.
- 🐢 **Baseline Only**: **SGD** — too slow and inefficient without momentum.

---
