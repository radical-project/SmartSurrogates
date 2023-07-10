**Working
Document for SI at Brookhaven 2023**

The overall goal
is to build a prototype of ROSE. This can be divided into various steps and
milestones that can help in achieving the desired outcome. For the summer internship
program, it can be laid out as follows: -

1^st^ step  meet with multiple
stakeholders and figure out the surrogate models that are currently in use. For
example, meeting with Univ of Virginia and Rochester Univ. This will help me
understand the models and the underlying methodology towards building one.

a.
The next step is to figure out how to improve
the model. The improvement largely is motivated by the uncertainty
quantification. There are multiple types of uncertainties in a surrogate
modelling process. For example, aleatoric, epistemic, input related, model
approximation, extrapolation etc. Depending on the specific case selected, the uncertainties
in the model will need be identified. The metrics for improvement of the model can
be accuracy, efficiency, resource utilization.

2^nd^ step  To build an improved version
of the model. The model provided by the stakeholders will be used as the baseline
model and new model that supersedes the baseline model. The threshold can
depend on the metric used for assessment. The new model will incorporate the
active learning approach. The goal here is that the model should improve by selectively
choosing the informative data points, hence reducing the amount of data to
train an accurate surrogate model. In this process, following are the likely
steps involved: -

a.
Define the type of surrogate model to be used. As
from 1a above, a baseline model will be available from other stakeholders.

b.
Choosing the dataset that represents the original
labelled dataset.

c.
Train a surrogate model. Until here the steps
are linked with univ of Virginia and Rochester.

d.
Here onwards, we want to decide what type of
active learning (AL) methodology will be used. For example, whether it is uncertainty
sampling, density based etc.

e.
The selected AL method will be used for uncertainty
measurement, estimating the diversity of data and calculating the confidence
levels of prediction tasks.

f.
The data points are then selected for labelling.
The data could be from real time experiments or simulations.

g.
The surrogate model is then updated. This should
be validated with a test set that has been held out for performance checks.

h.
The process continues to iterate, and the surrogate
model is improved for performance. A workflow diagram is also placed in the GitHub
repo for this.

Next logical steps  following the aforesaid work
in 1^st^ and 2^nd^ steps, the next goal is to build an infrastructure
that can support the exploration of optimal surrogate models, hence the ROSE. ROSE
can be visualized as a layer on top of RCT infrastructure. The RCT framework
comprises of RADICAL-Pilot, RADICAL – SAGA, RADICAL EnTK and analytics. These
components facilitate features like – task scheduling, workflow management,
resource management and data management. The focus is towards scientific applications
and provides scalability and flexibility. Hence enabling scientific computing
on HPC resources in an optimized distributive manner.

Presently, the comparables to ROSE like deephyper,
have a static approach. i.e., the parameter or a NN search is based on a static
dataset. The idea is to provide a dynamic structure to ROSE wherein the active
learning methods continue to update the labelled database and the model improves
based on the set of metrics.

Mounting ROSE on RCT is likely to involve understanding/
execution of the following steps: -

a.
Surrogate modelling requirements/ dependencies

b.
Data management with RCT

c.
Task execution with RCT

d.
Workflow management for SM by using RCT

e.
Performance analysis + optimization

f.
Development and version control

g.
Integration of SM infrastructure (ROSE) with RCT

h.
Evaluation

Following is a
pseudocode for building the infrastructure (based on the above steps).

understand_requirements
--> integrate_components

integrate_components
--> data_management

integrate_components
--> task_execution

data_management
--> task_execution

task_execution
--> workflow_management

task_execution
--> performance_analysis

workflow_management
--> iterative_development

performance_analysis
--> iterative_development

iterative_development
--> integration_surrogate_models

integration_surrogate_models
--> evaluate_validate

evaluate_validate
--> end

A sample code
template to start the infrastructure building process is placed in the GitHub
repo. The idea is after the 1^st^ and 2^nd^ steps a new repo
for SWE and version control will be created to translate the infrastructure
into a protype software. This will be updated as the dev phase moves along.
