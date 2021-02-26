# Notes from OpenShift Workshop back in Feb 2021.
Welcome to OpenShift Advanced Application Deployment 
Location: Virtual
Instructors:   Judd Maltin
Dates and Times: Jan 04th - 08th, 2021
Monday to Thursday 0900 1700 Central TIme


BlueJeans Meeting Link: https://bluejeans.com/
Slack:  #
https://red-hat-gpte.slack.com/archives/C01J95V7L0G

Agenda (all times SGT time - Subject to Change based on Class Progress)

Monday
Welcome and Introductions
Slides - Course Introduction
Break
Slides - Twelve Factor App
Break 
Controllers
Lunch
Lab
Operators
Lab
Tuesday
Lab
CI/CD
Lunch
Lab
Builds
Wednesday
Lab
Lunch
Pipelines
Lab
Thursday
Lab
Lunch
Final Lab and fill out the Survey
Check if you received survey email (see slack)
Request Final Lab environment (see slack)
Final Lab Review (NEEDED FOR CREDITS)
OpenShift Pipelines (OPTIONAL)
Start working on Final Lab
Class finishes


Class Attendees 
Your full name, role, e-mail, student# - REQUIRED FOR ATTENDANCE:
student1, Judd Maltin, Principal Architect, judd@redhat.com 
student2, Lázaro Miguel Coronado Torres, Middleware Consultant, lazaro.coronado@redhat.com
student3, Alfredo Pizarro Villalobos, Software maintenance engineer , apizarro@redhat.com
student5, Ezequiel Iglesias, Monitoring & Event Management, ezmaig@ar.ibm.com
student7, Puppo Martin, SRE , puppomartin@ar.ibm.com
student8 Heber Romero Tellez, Architect, psehgaft@redhat.com
Student9 Gabriel Scheffer de Souza, Technical Support Engineer, gscheffe@redhat.com
Student4, Johny Jiménez, Presales Engineer, jjimenez@licenciasonline.com
Student6, Felipe Carrasco, Consultant, felipe.carrasco@entelgy.com
Student10, Oscar Andres Noce, Consultant, anoce@redhat.com
Student11, Marco Braga, Support Engineer, mrbraga@redhat.com
student12, Iván Pinto, IT Solutions Architect, pintoid@globalhitss.com
Student13, Ana Cecilia Ruiz Gallardo, Solutions Architect, aruizgal@redhat.com
Student 15. Nestor Martinez Alvarado, Solution Architect, nmartine@redhat.com
student16. Paulo Bernal, Presales Engineer, pbernal@compusoluciones.com



Classroom Environment
Get yourself the OPENTLC OpenShift 4 Labs / OpenShift 4 Student VM from https://labs.opentlc.com
      USERNAMES: student[1-30] PASSWORD: ocp4_student
      Login to cluster:  oc login -u <student1> https://api.cluster-a433.a433.sandbox1884.opentlc.com:6443
      
      Openshift Master Console: https://console-openshift-console.apps.cluster-a433.a433.sandbox1884.opentlc.com
Openshift API for command line 'oc' client: https://api.cluster-a433.a433.sandbox1884.opentlc.com:6443
Download oc client from http://d3s3zqyaz8cp2d.cloudfront.net/pub/openshift-v4/clients/ocp/4.6.4/openshift-client-linux-4.6.4.tar.gz

Cheat Sheets and Reference Cards (bash, git, oc, vim, Docker, Jenkins, etc.)
https://github.com/redhat-gpte-devopsautomation/reference

Day 1 - Introductions & Controllers
   
Twelve Factor:
    Slides: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/02_12_Factor_Applications/AllSlides.html
    
Controllers:
    Slides: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/03_Controllers/AllSlides.html
    Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/03_Controllers/03_1_Controllers_Lab.html
    Solution: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/03_Controllers/03_1_Controllers_Solution_Lab.html
    
    Resources: 
        Deployments vs. Deployment Configs: https://docs.openshift.com/container-platform/4.6/applications/deployments/what-deployments-are.html
        CAP theorem: https://en.wikipedia.org/wiki/CAP_theorem
        More Deployment Types: https://dev.to/mostlyjason/intro-to-deployment-strategies-blue-green-canary-and-more-3a3
               
Operators:
    Slides:  http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/04_Operators
    Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/04_Operators/04_1_Operators_Lab.html
    Lab Solution: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/04_Operators/04_1_Operators_Solution_Lab.html
    

Day 2 -  CI/CD Tools and Building Applications

CI/CD Tools:
    Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/05_CICD_Tools/05_1_CICD_Tools_Lab.html
    Lab Solution: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/05_CICD_Tools/05_1_CICD_Tools_Solution_Lab.html
    
Building Applications:
    Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/06_Building_Applications/06_1_Building_Applications_Lab.html
    Lab Solution: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/06_Building_Applications/06_1_Building_Applications_Solution_Lab.html
    
OpenShift Builds (Developer Preview in 4.4): https://github.com/redhat-developer/build

OpenShift Plugin for Jenkins:
    https://github.com/openshift/jenkins-client-plugin

White Paper on CICD with OCP and Jenkins (with the tagging strategy we use)
    https://access.redhat.com/documentation/en-us/reference_architectures/2017/html/application_cicd_on_openshift_container_platform_with_jenkins/

Jenkins in a Nutshell: https://dzone.com/articles/jenkins-in-a-nutshell
Jenkins using PVC (mount at .m2/repository, NOT .m2):  on AWS) we only have RWO volumes - so parallel builds won't work with a volume.
    https://blog.openshift.com/decrease-maven-build-times-openshift-pipelines-using-persistent-volume-claim/ 
Jenkins Day 2: https://access.redhat.com/articles/3714291

Jenkins Pipeline examples: https://github.com/jenkinsci/pipeline-examples
OpenShift Pipeline Library: https://github.com/redhat-cop/pipeline-library

OpenShift integration with external Jenkins:
    http://uncontained.io/articles/external-jenkins-integration¿

Running Jenkins Builds in Containers:
    https://itnext.io/running-jenkins-builds-in-containers-458e90ff2a7b

Trick to make starting pipelines faster (don't look for already running agent pods - there are never any anyway):
oc set env dc/jenkins JENKINS_JAVA_OVERRIDES="-Dhudson.slaves.NodeProvisioner.initialDelay=0 -Dhudson.slaves.NodeProvisioner.MARGIN=50 -Dhudson.slaves.NodeProvisioner.MARGIN0=0.85 -Dorg.jenkinsci.plugins.durabletask.BourneShellScript.HEARTBEAT_CHECK_INTERVAL=300"

    
Day 3 -  Pipelines
Slides: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/07_Pipelines/AllSlides.html
Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/07_Pipelines/07_1_Pipelines_Lab.html
Lab Solution: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/07_Pipelines/07_1_Pipelines_Solution_Lab.html


OpenShift Pipelines Lab: https://github.com/redhat-cop/openshift-lab-origin/blob/master/OpenShift4/OpenShift_Pipelines_Lab.adoc 


Day 4 - Final Lab
Lab: http://slides-8080-app-appd.apps.shared-dev4.dev4.openshift.opentlc.com/08_Final_Lab/08_1_Final_Lab.html

Day-by-Day Notes:
Notes - Day 1 - Introductions & Controllers
        oc edit or oc set env is easiest way to set environment variables
-but, if you love jsonpatch...
oc patch dc/green  -p '{"spec": {"template": {"spec": {"containers": [{"name": "green", "env": [{"name": "SELECTOR", "value": "pets"}]}]}}}}'
 
OpenShift Docs for route based deployments strategies:
https://docs.openshift.com/container-platform/4.2/applications/deployments/route-based-deployment-strategies.html#deployments-blue-green_route-based-deployment-strategies

Kubernetes Liveness and Readiness Probes: How to Avoid Shooting Yourself in the Foot https://blog.colinbreck.com/kubernetes-liveness-and-readiness-probes-how-to-avoid-shooting-yourself-in-the-foot/
Kubernetes Liveness and Readiness Probes Revisited: How to Avoid Shooting Yourself in the Other Foot https://blog.colinbreck.com/kubernetes-liveness-and-readiness-probes-revisited-how-to-avoid-shooting-yourself-in-the-other-foot/

Relationship between deployments and replicasets:
https://www.ibm.com/cloud/architecture/content/course/kubernetes-101/deployments-replica-sets-and-pods

DeploymentConfig -> Deployment conversion:

-apiVersion: apps.openshift.io/v1
-kind: DeploymentConfig
+apiVersion: apps/v1
+kind: Deployment
 metadata:
   labels:
     app: httpd-example
@@ -9,16 +9,11 @@
 spec:
   replicas: 1
   selector:
-    name: httpd-example
+    matchLabels:
+      name: httpd-example
   strategy:
     resources: {}
-    rollingParams:
-      intervalSeconds: 1
-      maxSurge: 25%
-      maxUnavailable: 25%
-      timeoutSeconds: 600
-      updatePeriodSeconds: 1
-    type: Rolling
+    type: RollingUpdate
   template:
     metadata:
       creationTimestamp: nullIndex of /pub/linux/centos/7/isos/x86_64
@@ -64,13 +59,3 @@
       securityContext: {}
       terminationGracePeriodSeconds: 30
   test: false
-  triggers:
-  - imageChangeParams:
-      automatic: true
-      containerNames:
-      - httpd-example
-      from:
-        kind: ImageStreamTag
-        name: httpd-example:latest
-    type: ImageChange
-  - type: ConfigChange

CronJob Example:
    https://github.com/redhat-cop/openshift-management/tree/master/jobs
    
Design patterns for container-based distributed systems
  -  https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45406.pdf  
  
  
    Book: Kubernetes Patterns - Bilgin Ibryam and Roland Hub
    
Declarative OpenShift/k8s options:
    OpenShift templates - https://docs.openshift.com/container-platform/4.3/openshift_images/using-templates.html
    Kustomize (not templates) - https://kustomize.io/
    Helm Charts (v3 only, no tiller) - https://helm.sh/
    
    Higher level tools:
    https://argoproj.github.io/argo-cd/
    https://github.com/redhat-cop/openshift-applier
    https://github.com/redhat-cop/k8s_config
    
    Notes - Day 2 - Operators & CI/CD Tools:
    Other Example Operators:
User Quota Operator: https://github.com/redhat-gpte-devopsautomation/userquota-operator 
Project Deletion Operator: https://github.com/redhat-gpte-devopsautomation/project-cleanup-operator
Namespace configuration Operator: https://github.com/redhat-cop/namespace-configuration-operator 
Gogs Operator: https://quay.io/repository/nissessenap/gogs-operator
Python Operator Framework: https://github.com/zalando-incubator/kopf

Nexus 410 error work-around:
    https://support.sonatype.com/hc/en-us/articles/360045220393-Scripting-Nexus-Repository-Manager-3#how-to-enable

[user-redhat.com@bastion ~]$ NEXUS_POD=$(oc get pod -l deploymentconfig=nexus -o jsonpath='{.items[0].metadata.name}')
[user-redhat.com@bastion ~]$ oc rsh $NEXUS_POD
sh-4.4$ echo nexus.scripts.allowCreation=true >> /nexus-data/etc/nexus.properties 
sh-4.4$ exit
exit
[user-redhat.com@bastion ~]$ oc delete pod $NEXUS_POD

Blog Post on using Persistent Volumes in Jenkins Agent Pod:
    https://blog.openshift.com/decrease-maven-build-times-openshift-pipelines-using-persistent-volume-claim/
    One correction: Mount the volume in /home/jenkins/.m2/repository, NOT /home/jenkins/.m2 (otherwise you overwrite the stock settings.xml - we don't notice it because we always use a -s settings.xml from the repo anyway....)
    Realize that in OCP4 (on AWS) we only have RWO volumes - so parallel builds won't work with a volume...

oc get templates -n openshift | grep <search>
oc get template <template-name> -n openshift -o yaml > template
oc get crd.yaml
 
How to find something in OpenShift resources (e.g. emptyDir):
    for r in $(oc api-resources | cut -f1 -d" ") ; do echo $r ; oc explain $r --recursive=true | grep emptyDir ; done


Notes - Day 3 - Builds
Build process documented including creating GitLab tokens and build secrets:
https://gitlab.com/2020-summit-labs/bookbag-template

Controlling namespaces for pods (setup build namespace)
https://blog.openshift.com/deploying-applications-to-specific-nodes/


Notes - Day 4 - Pipelines
https://plugins.jenkins.io/hashicorp-vault-plugin/

oc create serviceaccount -n user0-test automation
oc policy add-role-to-user edit system:serviceacount:user0-test:automation -n user0-test
clusterrole.rbac.authorization.k8s.io/edit added: "system:serviceacount:user0-test:automation"
oc serviceaccount get-token -n user0-test automation

Tekton Pipelines
https://github.com/tektoncd/pipeline


*****NOTE: you may need to uncheck "Lightweight checkout" when you change from using your pipeline script to "SCM" in the pipelines lab.  I was not able to use a jenkinsfile from the gogs repo until this was unchecked.


Interesting blogs in developers.redhat.com
https://developers.redhat.com/blog/2020/01/23/how-to-maintain-stable-build-and-deployment-performance-on-red-hat-openshift/
https://developers.redhat.com/blog/2020/01/17/deploying-applications-in-the-openshift-4-3-developer-perspective/

Declaritive vs Groovy (Scripted)
https://jenkins.io/doc/book/pipeline/syntax/#compare




Notes - Day 5 - Homework and Extras:
    

OpenShift Pipelines based on Tekton:
    Tekton Overview (Red Hat Internal Only): https://docs.google.com/presentation/d/1E6FChdbIrMHlynF-yvEMrTiAnR8rwMdvebBxPgdcmrE/edit?usp=gmail
    OpenShift Pipelines Documentation: https://openshift.github.io/pipelines-docs
    OpenShift Pipelines Tutorial: https://github.com/openshift/pipelines-tutorial/
    OpenShift Pipelines Examples: https://github.com/siamaksade/openshift-pipelines-examples
    Tekton Pipelines Documentation: https://github.com/tektoncd/pipeline/tree/master/docs
    Download Tekton CLI: https://github.com/tektoncd/cli#getting-started
    
    OpenShift Pipelines Demo: https://youtu.be/0Nzg-qI2KH0
    What's new in OCP 4.2: https://www.youtube.com/watch?v=0Nzg-qI2KH0&authuser=0
    Building Images with S2I and Tekton: https://www.youtube.com/watch?v=VblUusADGuQ&authuser=0
    What is Tekton: https://www.youtube.com/watch?v=TWxKD9dLpmk&authuser=0
    Mario's Adventures in Tekton Land: https://www.youtube.com/watch?v=LdXXtDYxD-0&authuser=0
    How to build Cloud Native CI/CD Pipelines with Tekton: https://www.youtube.com/watch?v=-ji5Z0qJmJs&authuser=0
    Plumbing Kubernetes Builds with Tekton: https://www.youtube.com/watch?v=q5P2V_YShjA&authuser=0
    
    Check out different example pipelines for jenkins and tekton: https://github.com/redhat-cop/container-pipelines
    
    Openshift Pipeline Builder: https://github.com/openshift/console/pull/4031    
    
    K8s troubleshooting guide with excellent diagram to help the workflow downloadable as a PDF: https://learnk8s.io/troubleshooting-deployments

Script to export all projects to files

projects=$(oc get projects --output=jsonpath={.items..metadata.name})
for project in $projects; do
    echo "exporting project $project"
    oc get -o yaml deploymentconfigs,routes,svc,pvc,buildconfigs,secrets,configmap -n $project > $project.yaml
done


Even MORE Extras:



Python Operators with kopf [xxxxxxxx]
Kopf Source-to-Image:
https://github.com/jkupferer/kopf-s2i
https://github.com/jkupferer/kopf-s2i-example
Other Examples:
https://github.com/jkupferer/openshift-deployment-operator/
https://github.com/redhat-gpte-devopsautomation/user-namespace-operator
https://github.com/redhat-cop/poolboy

https://pypi.org/project/pykube-ng/
https://github.com/kubernetes-client/python

pip3 install --user --upgrade kopf kubernetes

Creating an Source-to-Image Build
https://blog.openshift.com/create-s2i-builder-image/

apiVersion: apiextensions.k8s.io/v1
kind: CustomResourceDefinition
metadata:
  name: widgets.myapp.example.com
spec:
  conversion:
    strategy: None
  group: myapp.example.com
  names:
    kind: Widget
    listKind: WidgetList
    plural: widgets
    singular: widget
  scope: Namespaced
  versions:
  - name: v1
    served: true
    storage: true
    subresources:
      status: {}
    schema:
      openAPIV3Schema:
        type: object
        properties:
          apiVersion:
            description: 'APIVersion defines the versioned schema of this representation
              of an object. Servers should convert recognized schemas to the latest
              internal value, and may reject unrecognized values. More info2: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources'
            type: string
          kind:
            description: 'Kind is a string value representing the REST resource this
              object represents. Servers may infer this from the endpoint the client
              submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds'
            type: string
          metadata:
            type: object
          spec:
            type: object
            additionalProperties: true

Kopf Exercise:

Start with https://github.com/jkupferer/kopf-s2i-example, get it built and runvim 
Add the following to operator/operator.py:
@kopf.on.create('gpte.opentlc.com', 'v1alpha1', 'gogs')
def watch_gogs_create(spec, name, namespace, logger, **_):
    logger.info('Gogs Create %s', name)

@kopf.on.update('gpte.opentlc.com', 'v1alpha1', 'gogs')
def watch_gogs_update(spec, name, namespace, logger, **_):
    logger.info('Gogs Update %s', name)

@kopf.on.delete('gpte.opentlc.com', 'v1alpha1', 'gogs')
def watch_gogs_delete(spec, name, namespace, logger, **_):
    logger.info('Gogs Delete %s', name)
Add access to the role in the deploy-template.yaml for gogs
      - apiGroups:
          - gpte.opentlc.com
        resources:
          - gogs
        verbs:
          - get
          - list
          - patch
          - update
          - watch
Build test and run...




Twelve Factor App Revisit [xx]
https://www.redhat.com/en/resources/cloud-native-container-design-whitepaper

External Image Repository Integration and Controls [xxxxx]
Mapping ImageStreams to Remote Registries
Image Pull Secrets (direct pull from remote registry)
Using skopeo to push images into the registry

Writing OpenShift Templates and Helm Charts [xxxxx]
https://docs.openshift.com/container-platform/4.3/openshift_images/using-templates.html
https://kustomize.io/
https://helm.sh/docs/intro/quickstart/
https://helm.sh/docs/chart_template_guide/getting_started/

Convert template openshift httpd-example to a helm chart:

oc get template -n openshift httpd-example -o yaml

https://github.com/redhat-cop/template2helm
- FYI, some of the CoP members have also started work on a tool which will allow you to create a Helm Chart from a Namespace: https://github.com/infosec812/namespace2chart

https://github.com/redhat-cop/k8s_config

Tekton [xxx]
https://github.com/tektoncd/pipeline/blob/master/docs/tutorial.md
https://www.youtube.com/watch?v=pMDiiW1UqLo
https://blog.openshift.com/pipelines_with_tekton/

odo - OpenShift do [xx]
https://docs.openshift.com/container-platform/4.3/cli_reference/openshift_developer_cli/understanding-odo.html
https://docs.openshift.com/container-platform/4.3/cli_reference/openshift_developer_cli/installing-odo.html
https://docs.openshift.com/container-platform/4.3/cli_reference/openshift_developer_cli/creating-a-single-component-application-with-odo.html

How to add Let's Encrypt Certificates to a cluster running on AWS:
    https://github.com/redhat-cop/openshift-lab-origin/blob/master/OpenShift4/Lets_Encrypt_Certificates_for_OCP4.adoc
    
Recommended Courses:
    Red Hat Container Management And Image Builds https://learning.redhat.com/enrol/index.php?id=1857
    Red Hat OpenShift Container Platform 4 Installation https://learning.redhat.com/course/view.php?id=1806
    Red Hat OpenShift Container Platform 4 Resources and Tools https://learning.redhat.com/course/view.php?id=1825
    Red Hat OpenShift Container Platform 4 Configuration https://learning.redhat.com/enrol/index.php?id=1798





