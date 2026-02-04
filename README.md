Title: Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model
1. Methodology
   
   <img src="screenshots/Screenshot%202026-02-04%20212710.png" width="700">
3. Description
  a.  Data Collection:
   The air quality dataset containing NO₂ concentration values was collected from Kaggle.
  b. Data Pre-Processing:
     The dataset was cleaned by removing missing and corrupted entries. The NO₂ feature was transformed using a roll-number-based non-linear transformation.
  c. PDF Parameter Estimation:
    A Gaussian-shaped probability density function was assumed for the transformed data. The parameters μ, λ, and c were estimated using Maximum Likelihood Estimation.
  d. Density Evaluation:
     The learned probability density function was evaluated for the transformed data points to model their distribution.
  e. Result Interpretation:
    The estimated parameters were analyzed, and the learned probability density function was visualized to validate the model.
4. Input/Output
   Input NO₂ Concentration Values from Dataset (x)
   -> Input University Roll no.
   -> Compute Transformation Parameters aᵣ = 0.05 × (r mod 7); bᵣ = 0.3 × (r mod 5 + 1)
   -> Apply Non-Linear Transformation z = x + aᵣ sin(bᵣ x)
   -> Input Transformed Values (z) to PDF Model
   -> Learn PDF Parameters(λ, μ, c) using Estimation Method
   -> Compute Predicted Probability Density p̂(z)
   -> Output Results • λ, μ, c • p̂(z) values
5. Live Link
   https://colab.research.google.com/drive/1gS7AKBCZ3bCScFQ4v2JwD19hiChSpsTL#scrollTo=XpY3L_qoOqAO
6. Screenshot
   
   <img src="screenshots/Screenshot%202026-02-04%20212710.png" width="500">

