# MLops-Specialization

## Machine Learning Modelling Pipelines in Production

### Week 5: 

#### Explainable AI

- Responsible AI
    - Faireness
    - Explainablity
    - Privacy
    - Secrurity

- Explainable Aritificial Intelligence (XAI)
    - Importance of explanations:
        - To ensure algorithmic faireness
        - Identify potential bias and problems in the training data
        - To ensure algorihms/models works as expected.

    - Need for Exaplainability in AI
        - Deep Neural Networks (DNNs) can be fooled into misclassifying inputs with no resemblance to the true category.

Reference
1. For more information see [DARPA's Explainable Aritification Intelligence Program](./MLops-Specialization/Week-5/2850-Article Text-6600-1-10-20190624.pdf)

#### Interpretability

What is intergretability:
    
    (Models) are interrepatable if their operations can be understood by a human, either through introspection or through a produced explanation.

Categorizing Model Interpretation Methods:

- Intrinsic or Post-Hoc

- Model Specific or Model Agnostic

- Local or Global

Intrinsically Interoretable Models
- Learn model are easy to understand the relationship
- Feature importance:
    Linear regression model, t-statistic

 TesorFlow Lattice:


Good Reference on '**Interpretable Machine Learning**'   
https://christophm.github.io/interpretable-ml-book/

**Model Agnostic Methods**

This methods separate explanation from the machine learning model

    Desised Characteristics:
        - Model Flexibility
        - Explanation Flexibility
        - Representation Flexibility

**Partial Dependence Plots**
    
**Permutation Feature Importance**


**Shapley Value**
It is a method for assigning payouts to players depending on their contribution to the total
Advantages of the Shapley Values
  
    - Based on Solid theoritical foundation. Satisfies Effieciency, Symmertry, Dummy, and Addtivitiy properties

Disadvantages:

    - Conputationally expensive
    - Easily misintergreted
    - Alwasys uses all the features, so not good for explanation of only a few features
    - No prediction model.
    - Does not work well when features are not correlated    

Tool: Open source tool named SHapley Addtive exPlanation(SHAP). 
Github: https://github.com/slundberg/shap

It includes extensions for:
 
 1. TreeExplainer: High-speed exact algorithm for tree ensembles
 2. DeepExplainer: High-speed approximation algorithm for SHAP values in deep learning models
 3. GradientExplaniner: Combines ideas from Interatred Gradients, SHAP abd SmoothGrad into a single expected value equation.
 4. KernelExplainer: uses a specially-weighted local linear regression to estimate SHAP values for any model

 Shap values can be visualised as forces in forceplot



