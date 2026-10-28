# SIP Dropout Prediction

An applied machine-learning project exploring how to identify Systematic
Investment Plans (SIPs) that may be discontinued, understand possible
reasons, and support appropriate investor-retention actions.

> **Project status:** Early research and data discovery stage. No
> SIP-specific prediction model has been trained yet.

## Problem

A SIP is a recurring investment into a mutual fund. When a SIP is
discontinued, the reason matters:

-   **Financial hardship:** offer flexibility, such as reducing the
    contribution or pausing where supported.
-   **Market panic:** provide balanced, educational information rather
    than pressure.
-   **Switching:** understand whether the investor is moving to another
    fund or provider.
-   **Goal completion:** help the investor plan a new financial goal
    instead of treating every discontinuation as a failure.

The long-term goal is to explore a workflow that can estimate the risk
of a SIP lapsing over a defined future window and, where reliable labels
exist, identify a likely reason to guide a suitable response.

## Current stage

The first notebook is a **data-inspection exercise** using the IBM Telco
Customer Churn sample dataset. It practises loading a public CSV,
inspecting columns and data types, checking missing values and
duplicates, and visualising a churn label.

**Important limitation:** telecom churn is not SIP discontinuation. This
dataset does not provide mutual-fund SIP instalment histories, SIP
mandate bounces, fund-level market context, or SIP-specific
discontinuation reasons. It is only a workflow-learning proxy and must
not be presented as evidence of SIP investor behaviour.

The next research task is to investigate public SIP statistics and
determine whether suitable individual-level, longitudinal SIP data is
available. Aggregate industry statistics can support trend analysis, but
cannot by themselves identify which individual SIP will lapse.

## Repository contents

``` text
sip-dropout-prediction/
├── README.md
└── SIP_Dropout_Milestone_1_Dataset_Discovery.ipynb
```

As the project grows, notebooks, documentation, and source code can be
organised into separate folders. Do not commit private investor
information, credentials, API keys, or other sensitive data.

## Getting started

### Option A: Run in Google Colab

1.  Open [Google Colab](https://colab.research.google.com/).
2.  Choose **File → Upload notebook**.
3.  Upload `SIP_Dropout_Milestone_1_Dataset_Discovery.ipynb`.
4.  Run the cells from top to bottom.
5.  The notebook loads the public CSV from the internet, so an internet
    connection is required.

### Option B: Run locally in Jupyter

You need Python and Jupyter installed. In a terminal, install the
required packages:

``` bash
python -m pip install jupyter pandas matplotlib
```

Start Jupyter:

``` bash
jupyter notebook
```

Open the notebook and run cells from top to bottom. If you use
JupyterLab instead, you can start it with `jupyter lab`.

## Data sources

-   **IBM Telco Customer Churn sample CSV:**\
    https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
-   **IBM sample documentation:**\
    https://www.ibm.com/docs/en/cognos-analytics/12.0.x?topic=samples-telco-customer-churn
-   **AMFI mutual-fund information:**\
    https://www.amfiindia.com/mutual-fund
-   **AMFI-related public monthly SIP statistics listing:**\
    https://dataful.in/datasets/20840/

Check the original source for current availability, licensing,
definitions, and coverage before reusing data. Record dataset provenance
and limitations in future notebooks.

## Planned roadmap

1.  **Data discovery:** validate public datasets and document their
    limitations.
2.  **Project setup:** organise notebooks, documentation, and version
    history with Git.
3.  **Data understanding:** inspect distributions, missingness, and
    potential leakage.
4.  **Baseline modelling:** only after a defensible target and suitable
    data are identified.
5.  **Evaluation:** choose metrics appropriate for rare dropout events
    and validate on data that respects time.
6.  **Reason analysis:** explore reason classification only if
    trustworthy reason labels are available.
7.  **Retention workflow:** map validated predictions to appropriate,
    non-coercive interventions.
8.  **Presentation:** document findings, limitations, and a reproducible
    workflow.

## Responsible-use principles

-   Do not describe proxy or simulated data as real SIP data.
-   Do not claim that a model predicts future SIP lapses unless its
    target, data, and evaluation support that claim.
-   Avoid treating goal completion as a negative outcome by default.
-   Protect investor privacy and use only data with appropriate
    permission.
-   Document uncertainty, limitations, and potential harms before
    proposing real-world interventions.

## Learning approach

This is a hands-on project. Core ML theory is being studied separately
through Andrew Ng's Machine Learning course. This repository focuses on
applying concepts to the project and learning practical tools such as
Jupyter, pandas, Git, and GitHub as they become necessary.

## License

No project license has been selected yet. Until a license is added, do
not assume that others have permission to reuse this repository's
original content. Dataset terms are governed by their respective
sources.
