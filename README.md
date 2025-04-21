Acknowledgments
The data used for this competition was provided by the Healthy Brain Network, a landmark mental health study based in New York City that will help children around the world. In the Healthy Brain Network, families, community leaders, and supporters are partnering with the Child Mind Institute to unlock the secrets of the developing brain. In addition to the generous support provided by the Kaggle team, financial support has been provided by the California Department of Health Care Services (DHCS) as part of the Children and Youth Behavioral Health Initiative (CYBHI).

Health Care Services Logo

Sponsorship
Dell Technologies and NVIDIA are thrilled to partner with the Child Mind Institute, recognizing the profound impact this collaboration will have on advancing mental health support for children and adolescents. This partnership aligns perfectly with our commitment to leveraging technology for social good and fostering a healthier, more inclusive future.

Dell Technologies AI solutions from desktop to datacenter to cloud. NVIDIA pioneered accelerated computing to tackle challenges no one else can solve. Our work in AI and digital twins is transforming the world's largest industries and profoundly impacting society.

Dell Technologies NVIDIA
Evaluation
Submissions are scored based on the quadratic weighted kappa, which measures the agreement between two outcomes. This metric typically varies from 0 (random agreement) to 1 (complete agreement). In the event that there is less agreement than expected by chance, the metric may go below 0.

To compute the quadratic weighted kappa, we construct three matrices, O
, W
, and E
, with N
 the number of distinct labels.

The matrix O
 is an N×N
 histogram matrix such that Oi,j
 corresponds to the number of instances that have an actual value i
 and a predicted value j
.

The matrix W
 is an N×N
 matrix of weights, calculated based on the squared difference between actual and predicted values:

Wi,j=(i−j)2(N−1)2

The matrix E
 is an N×N
 histogram matrix of expected outcomes, calculated assuming that there is no correlation between values. This is calculated as the outer product between the actual histogram vector of outcomes and the predicted histogram vector, normalized such that E
 and O
 have the same sum.

From these three matrices, the quadratic weighted kappa is calculated as: 

κ=1−∑i,jWi,jOi,j∑i,jWi,jEi,j.
