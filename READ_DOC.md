# RECAP

This document contains (1) the full Science article **“A Neural Substrate of Prediction and Reward”** by Schultz, Dayan, and Montague, and (2) the beginning of **“Language Acquisition and Use: Learning and Applying Probabilistic Constraints”** by Seidenberg.

---

## Part A — A Neural Substrate of Prediction and Reward  
**W. Schultz, P. Dayan, P. R. Montague**

---

## 1. Importance of prediction

Adaptive organisms must predict future events such as food, danger, or mates.  
Prediction allows preparation of behavior and better decision-making because different actions lead to different outcomes.

Animals can predict many properties of stimuli, but a particularly important form of prediction concerns the **time and magnitude of future rewards**.

---

## 2. Definition of reward

Reward is defined operationally as the positive value assigned to an object, action, or internal state.

- Rewards induce approach behavior.
- Rewards act as positive reinforcers during learning.
- Reward value is not fixed; it depends on internal state and experience.

---

## 3. Conditioning and learning from prediction

In conditioning:
- A neutral stimulus becomes a **conditioned stimulus (CS)** if it reliably precedes a reward (unconditioned stimulus, US).
- After learning, the CS predicts the **time and magnitude** of the reward.

Learning theories suggest that learning depends on **unpredictability** of reward.  
When a reward is fully predicted, no new learning occurs.

This explains **blocking**: if one cue already predicts the reward, adding a new cue provides no new predictive information, so no learning occurs for the new cue.

---

## 4. Dopamine neurons and reward processing

Dopamine neurons in the ventral tegmental area (VTA) and substantia nigra project to brain areas involved in motivation and goal-directed behavior.

Evidence linking dopamine to reward learning includes:
- Addictive drugs prolong dopamine effects.
- Dopamine pathways support electrical self-stimulation.
- Dopamine antagonists impair reward learning.

---

## 5. Dopamine neuron responses in monkeys

Single-neuron recordings show that dopamine neurons:
- Produce short phasic activations to appetitive stimuli.
- Respond similarly across different rewarding stimuli.

After learning:
- The phasic response **shifts from reward delivery to the onset of the predictive cue**.
- The predicted reward itself no longer elicits a response.

If the reward is omitted:
- Dopamine activity drops **below baseline at the exact expected time of reward delivery**.

This shows dopamine neurons encode **both reward prediction and reward timing**.

---

## 6. Dopamine as a prediction error signal

The article interprets dopamine activity as encoding the deviation between actual and predicted reward:

- Better than predicted → positive signal  
- As predicted → no signal  
- Worse than predicted → negative signal  

Thus dopamine neurons report a **reward prediction error**.

---

## 7. Temporal Difference (TD) learning framework

### Value function

The computational goal is to predict the discounted sum of future rewards:

$$
V(t) = \mathbb{E}\left[\sum_{k=0}^{\infty} \gamma^k r(t+k)\right]
$$

where $r(t)$ is the reward at time $t$ and $\gamma$ is a discount factor.

---

### Consistency condition

The value function satisfies:

$$
V(t) = \mathbb{E}[r(t) + \gamma V(t+1)]
$$

---

### TD error

A temporally local prediction error is defined as:

$$
\delta(t) = r(t) + \gamma \hat V(t+1) - \hat V(t)
$$

This error signal is immediately available and drives learning.

---

## 8. Temporal representation of stimuli

A single weight per cue cannot explain learning of reward timing.  
Therefore, each cue is represented as a **vector across time delays**:

- $x(t) = \{x_1(t), x_2(t), \ldots\}$
- $x_i(t) = 1$ exactly $i$ time steps after cue onset, and $0$ otherwise

Each component has its own weight $w_i$.

The predicted value is:

$$
\hat V(t) = \sum_i w_i x_i(t)
$$

---

## 9. Learning rule

Weights are updated according to the correlation between stimulus representation and prediction error:

$$
\Delta w_i = \alpha_x \sum_t x_i(t)\,\delta(t)
$$

Under suitable conditions, this rule converges to the true value function.

---

## 10. Neural interpretation of the model

The model assumes the dopamine system has access to:
1. Reward information $r(t)$,
2. A signal related to changes in predicted value,
3. A site to combine these signals,
4. Projections that broadcast the error signal to learning structures.

The model reproduces:
- the shift of dopamine responses from reward to cue,
- blocking,
- secondary conditioning,
- and timing-dependent effects.

---

## 11. Testable predictions stated in the paper

- With multiple predictive cues, dopamine responses should transfer to the **earliest reliable cue**.
- After learning a sequence (cue1 → cue2 → reward), omission of cue2 should produce a **dopamine decrease at the expected time of cue2**.

---

## 12. Action selection and dynamic programming

The TD value function can guide action choice by solving the **temporal credit assignment problem**.

When average prediction error is near zero:
- $\delta(t) > 0$ indicates outcomes better than expected,
- $\delta(t) < 0$ indicates outcomes worse than expected.

The paper describes simple strategies that exploit this signal to bias behavior toward reward-maximizing actions.

---

## 13. Open questions identified by the authors

The paper highlights unresolved issues:
- how stimuli are represented through time,
- how aversive events are encoded,
- limits of scalar (dopamine) signals versus richer vector representations,
- the role of attention,
- and how dopamine influences plasticity in striatum and cortex.

---

## Part B — Language Acquisition and Use (beginning only)

The document also includes the opening of Seidenberg’s article, which introduces:
- the standard linguistic view that language knowledge equals grammar,
- the competence–performance distinction,
- and the exclusion of probabilistic/statistical information from core grammar in traditional theories.

Only the introductory section is present in the provided document.
