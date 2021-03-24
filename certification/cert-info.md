# Info about operator certification


 Red Hat OpenShift Certified Operators allow customers to use the operational expertise of application providers, reducing configuration drift and driving better consistency and supportability.

 At a high level the Operator certification steps include:
 1. Confirming that the application’s container images and Operator image is Red Hat   certified. Certified images must be:
    1. Built using Red Hat Enterprise Linux or Red Hat Universal Base Image as the base layer.
    2. Comply with Red Hat Container Certification requirements.
    3. Submit to Red Hat to verify and publish.
    4. Provide product information for publishing in the Red Hat Container Catalog.
2. Then the Operator and Application container images are packaged and submitted through the Red Hat Partner Connect website along with additional metadata. The Operator metadata allow it to be deployed using the Operator Lifecycle Manager and to render the Operator’s detail page in OperatorHub.
3. The Operator and Application images then undergo a security health check.
4. Once they complete the health checks the RH team will post the Operator in the embedded OperatorHub.

Check out the detailed guide to OpenShift Operator Certification
- [Partner Guide for OpenShift Operator and Container Certification](https://redhat-connect.gitbook.io/partner-guide-for-red-hat-openshift-and-container/)

In general, to have a Certified Operator, you must first complete the Container Application Certification for all the applications you will be deploying with your operator. 
Focus areas:
1. Operator Certification workflow 
    ![Certification workflow](../images/Cerification-workflow.png)


Other references:
- [Red Hat OpenShift Operator Certification](https://www.openshift.com/blog/red-hat-openshift-operator-certification) (blog)
- [Red Hat OpenShift Operator Certification for Red Hat Partners](https://connect.redhat.com/en/partner-with-us/red-hat-openshift-operator-certification)
- [Red Hat OpenShift Operator Certification](https://redhat-connect.gitbook.io/red-hat-partner-connect-general-guide/certification-offerings/red-hat-openshift-operator-certification-1) (Git Book)
- [Red Hat OpenShift Operator Certification Data Sheet](https://connect.redhat.com/sites/default/files/2020-07/RH-OpenShift-Operator-Cert-Datasheet-US_062020F4.pdf)
- [Red Hat Ecosystem Catalog: Certified OpenShift Operators](https://catalog.redhat.com/software/operators/explore)
