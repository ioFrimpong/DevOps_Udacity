Deploy a Highly Available Web App using CloudFormation

In this CloudFormation based project, I deployed four Apache Servers in Private Subnets across two Availability Zones using an AutoScaling Group. A Launch Configuration was used for this AutoScaling Group.
A Load Balancer was used to serve the content of the Servers to the Internet.

Two stacks were created: one stack was for the network configuration, which included a VPC in the US-East-1 region with Public and Private Subnets in two Availability Zones. Two NAT Gateways were deployed in the Public Subnets to enable the Private Instances to reach the internet. The template also included an Internet Gateway and Route Configurations.

The second stack deployed the Servers using a Launch Configuration and an AutoScaling Group. It also deployed a Load Balancer, Listener and a Target Group for the Listener and AutoScaling Group.


URL of LoadBalancer: http://udapr-webap-1qh9tsp55wouc-1868388898.us-east-1.elb.amazonaws.com/
