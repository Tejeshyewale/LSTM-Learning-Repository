# 🧠 LSTM (Long Short-Term Memory) Notes

## 📌 1. Introduction

LSTM (Long Short-Term Memory) is a type of **Recurrent Neural Network (RNN)** designed to handle **sequential data**.

Examples of sequential data:

* Time series (stock prices)
* Text (sentences)
* Speech signals

---

## ❗ 2. Problem with RNN

Traditional RNN suffers from:

* Vanishing Gradient Problem
* Cannot remember long-term dependencies

Example:
In a long sentence, RNN forgets earlier words.

---

## 🚀 3. Why LSTM?

LSTM solves this problem by introducing:

* Memory cell
* Gates to control information flow

---

## 🧩 4. LSTM Architecture

LSTM consists of:

* Cell State (Cₜ)
* Hidden State (hₜ)
* Gates:

  * Forget Gate
  * Input Gate
  * Output Gate

---

## 🔑 5. Gates in LSTM

### 1. Forget Gate

* Decides what information to remove
* Uses sigmoid function (0 to 1)

If value ≈ 0 → forget
If value ≈ 1 → keep

### 2. Input Gate

* Decides what new information to add
* Updates cell state

### 3. Output Gate

* Decides what to output
* Produces hidden state

---

## 🧮 6. LSTM Working (Step-by-Step)

1. Forget old information
2. Add new information
3. Update cell state
4. Generate output

---

## 📐 7. Important Equations

Forget Gate:
fₜ = σ(Wf · [hₜ₋₁, xₜ] + bf)

Input Gate:
iₜ = σ(Wi · [hₜ₋₁, xₜ] + bi)

Candidate Memory:
C̃ₜ = tanh(Wc · [hₜ₋₁, xₜ] + bc)

Cell State:
Cₜ = fₜ * Cₜ₋₁ + iₜ * C̃ₜ

Output Gate:
oₜ = σ(Wo · [hₜ₋₁, xₜ] + bo)

Hidden State:
hₜ = oₜ * tanh(Cₜ)

---

## 📊 8. Advantages

* Captures long-term dependencies
* Solves vanishing gradient problem
* Works well for sequence data

---

## ⚠️ 9. Limitations

* Complex architecture
* High computation cost
* Requires more data

---

## 🧠 10. Applications

* Stock price prediction
* Sentiment analysis
* Speech recognition
* Language translation

---

## 🔄 11. LSTM vs RNN vs GRU

| Feature     | RNN   | LSTM | GRU    |
| ----------- | ----- | ---- | ------ |
| Memory      | Short | Long | Medium |
| Complexity  | Low   | High | Medium |
| Gates       | No    | 3    | 2      |
| Performance | Low   | High | High   |

---

## 💡 12. Key Points to Remember

* LSTM = RNN + Memory + Gates
* Works best for sequential/time-based data
* Uses sigmoid & tanh activation functions
* Maintains long-term dependencies

---

## 📚 13. Conclusion

LSTM is a powerful deep learning model for handling sequence data, widely used in NLP and forecasting.
