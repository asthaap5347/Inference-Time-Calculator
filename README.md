# Inference Time Calculator

A simple, interactive calculator exploring probability and AI inference.

This project was inspired by the probability concepts explored in **Stanford Code in Place**. It demonstrates how probability can help estimate the number of independent attempts needed to achieve a desired chance of success.

## 💡 About the Project

Imagine running multiple independent copies of an AI model, where each copy has a probability \(p\) of fixing a bug.

Even if one copy has a relatively low chance of success, running multiple copies increases the probability that at least one will succeed.

This calculator helps answer the question:

**How many copies do we need to run to achieve a target probability that at least one fixes the bug?**

## 🧮 The Mathematics

Let:
- \(p\) = probability that one copy fixes the bug
- \(n\) = number of independent copies
- \(P(E)\) = probability that at least one copy fixes the bug

The probability that one copy fails is:

\[
1-p
\]

Assuming the copies act independently, the probability that all \(n\) copies fail is:

\[
(1-p)^n
\]

Using the complement rule, the probability that at least one copy succeeds is:

\[
P(E) = 1-(1-p)^n
\]

To achieve a target probability \(t\), we require:

\[
1-(1-p)^n \geq t
\]

Solving for the smallest integer \(n\):

\[
n = \left\lceil \frac{\ln(1-t)}{\ln(1-p)} \right\rceil
\]

The calculator uses this formula to determine the minimum number of copies required to meet the target probability.

## 🚀 How to Use

1. Enter the probability that one copy fixes the bug.
2. Enter your target probability that at least one copy succeeds.
3. Click **Solve**.
4. View the minimum number of copies required and the resulting probability of success.

### Example

Suppose:
- Probability of success per copy: 0.159 (15.9%)
- Target probability of success: 0.99 (99%)

The calculator estimates how many independent copies are needed to achieve at least a 99% chance that one or more copies succeed.

## 🛠️ Built With

- HTML
- CSS
- JavaScript
- Probability and logarithms

The calculator runs directly in a web browser without requiring additional software.

## 🎯 Learning Objectives

- Understand the complement rule in probability.
- Explore independent trials and repeated attempts.
- Apply logarithms to solve probability inequalities.
- Connect probability concepts to AI inference and problem-solving.

## 📚 Inspiration

Inspired by probability concepts explored through **Stanford Code in Place**, using a practical AI-related scenario to make the mathematics interactive.

This is an independent learning project, not an official Stanford University project or an official Stanford Code in Place tool.

## 📄 License

This project is available for learning and educational purposes. No license has been specified yet.
