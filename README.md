Jersey-enabled Tomcat on OpenShift
==================================

This quick start is built by using the openshift-tomcat-quickstart and adds the Jersey framework support to it.
You can immediately start developing REST-ful webservices using Jersey annotations and deploy it into this Tomcat on OpenShift PaaS Cloud.

Running on OpenShift
--------------------

Create an account at http://openshift.redhat.com/
or on any OpenShift Origin based PaaS Cloud

Create a DIY application:

      rhc app-create -t diy-0.1 -a tomcatj

Get Tomcat running:

      cd tomcatj
      git remote add upstream -m master git://github.com/eyaqub/os-tomcat-jersey-quickstart.git
      git pull -s recursive -X theirs upstream master

Then push the repo upstream to OpenShift:

      git push

That's it, you can now checkout your application at:

      http://tomcatj-$yourlogin.rhcloud.com

