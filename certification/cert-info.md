**Certifying a RedHat Openshift Operators**

- [Why certify operators](#Why-certify-operators)
- [Configuring Account](#Configuring-Account)
- [Creating Project](#Creating-Porject)
- [Certified Operators](#Certified-Operators)
- [Choosing Operator Image](#Choosing-Operator-Image)
- [Installing Dependencies](#Installing-Dependencies)
- [Running as non-root](#Running-as-non-root)
- [Pushing Operator image to project](#Pushing-image-to-project)

 At a high level the Operator certification steps include:
 1. Confirming that the application’s container images and Operator image is Red Hat certified. Certified images must be:
    1. Built using Red Hat Enterprise Linux or Red Hat Universal Base Image as the base layer.
    2. Comply with Red Hat Container Certification requirements.
    3. Submit to Red Hat to verify and publish.
    4. Provide product information for publishing in the Red Hat Container Catalog.
2. Then the Operator and Application container images are packaged and submitted through the Red Hat Partner Connect website along with additional metadata. The Operator metadata allow it to be deployed using the Operator Lifecycle Manager and to render the Operator’s detail page in OperatorHub.
3. The Operator and Application images then undergo a security health check.
4. Once they complete the health checks the RH team will post the Operator in the embedded OperatorHub.

## Configuring Account

In order to certify an image you first need to create and configure a Red Hat Technology Partner account, to login here at [Certified Technology portal](https://connect.redhat.com/login)

After the account is created you much accept the licenses.  The first three licenses are prompted during account setup, the fourth you will need to find by going to "my Compnay"->"view user agreements" then "view and accept" the container program appendix.  For further instuctions refer to the Red Hat documentation.

To submit your image you will need to create a project.  The first time you do this you will need to go to "Zones & Resources"->"Red Hat OpenShift & containers", next select to "join" the zone.  From here you can either click "certify" or go to "Product & Certification"->"Manage Projects".

### Creating Project

[Creating Operator Project](https://redhat-connect.gitbook.io/partner-guide-for-red-hat-openshift-and-container/certify-your-operator/certify-your-operator-bundle-image/creating-operator-bundle-image-project)

At this point you can create a project and push your image to the project.  For container certification you will choose "operator image".  From here you will choose your project name, publishing registry, and base operating system. 

There are two methods avaialble to pushing images, you can do it manually or configure a build service that will automatically search a url and apply the dockerfile.  In either case after pushing the image Red Hat will automatically begin to scan the image for certification. Below is more information on the requirments to certify containers and operators.

### Certified Operators
Check out the detailed guide to OpenShift Operator Certification
- [Partner Guide for OpenShift Operator and Container Certification](https://redhat-connect.gitbook.io/partner-guide-for-red-hat-openshift-and-container/)

In general, to have a Certified Operator, you must first complete the Container Application Certification for all the applications you will be deploying with your operator.

![Certification workflow](https://github.ibm.com/TT-ISV-org/operator/blob/operator-certification/images/Certification-workflow.png)

The certification of an operator as shown in the above image is done 2 stages as follows:

1. Operator image certification process:

    . Create a Container Image project in https://connect.redhat.com/projects
    . Update operator files for certification.
    . Build and test the operator image.
    . Upload the operator image to scan.connect.redhat.com

2. Operator bundle image certification process:

    . Create an Operator Bundle Image project in https://connect.redhat.com/projects
    . Bundle the operator
    . Update operator bundle files for certification
    . Build and test the bundle image
    . Upload the operator bundle image to scan.connect.redhat.com

How to create the Operator images:
There are 3 kind of Operators available according to the Operator maturity model as follows:

1. Building a Helm Operator: 
https://redhat-connect.gitbook.io/certified-operator-guide/helm-operators/building-a-helm-operator

2. Building an Ansible Operator: 
https://redhat-connect.gitbook.io/certified-operator-guide/ansible-operators/building-an-ansible-operator

3. Building a Golang Operator:
https://github.ibm.com/TT-ISV-org/operator/blob/main/BEGINNER_TUTORIAL.md#develop-and-deploy-a-memcached-operator-on-openshift-container-platform

**Red Hat OpenShift Certification Badges:**

Red Hat awards OpenShift Certification Badges to Kubernetes Operators built and tested for specific-use, cloud-native cases—like networking and storage—and comply with industry-standard specifications or domain best practices. Current OpenShift Certification Badges are:

• Container Storage Interface (CSI)—for providing and supporting a block/file persistent storage backend for OpenShift.

• Container Networking Interface (CNI)—for delivery of networking services through a pluggable framework.

• Cloud-Native Network Functions (CNF)—for implementation of Telco functions deployed as containers.

Other references:
- [Red Hat OpenShift Operator Certification](https://www.openshift.com/blog/red-hat-openshift-operator-certification) (blog)
- [Red Hat OpenShift Operator Certification for Red Hat Partners](https://connect.redhat.com/en/partner-with-us/red-hat-openshift-operator-certification)
- [Red Hat OpenShift Operator Certification](https://redhat-connect.gitbook.io/red-hat-partner-connect-general-guide/certification-offerings/red-hat-openshift-operator-certification-1) (Git Book)
- [Red Hat OpenShift Operator Certification Data Sheet](https://connect.redhat.com/sites/default/files/2020-07/RH-OpenShift-Operator-Cert-Datasheet-US_062020F4.pdf)
- [Red Hat Ecosystem Catalog: Certified OpenShift Operators](https://catalog.redhat.com/software/operators/explore)
- [OpenShift Certification Badges](https://www.openshift.com/blog/badge-announcement-blog) (blog)
- [Certify your Operator Image](https://redhat-connect.gitbook.io/partner-guide-for-red-hat-openshift-and-container/certify-your-operator/creating-an-operator-project)
- [Certified oprator build guide](https://redhat-connect.gitbook.io/certified-operator-guide/)
