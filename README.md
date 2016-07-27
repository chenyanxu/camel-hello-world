# Camel Log QuickStart
本工程用于演示https://github.com/chenyanxu/karaf-s2i.git,先git lone 源码，然后创建模板文件，再通过模板文件创建app。
This quickstart shows a simple Apache Camel application that logs a message to the server log every 5th second.

This example is implemented using solely the XML DSL (there is no Java code). The source code is provided in the following XML file `src/main/resources/OSGI-INF/blueprint/camel-log.xml`.

This example uses a timer to trigger every 5th second, and then writes a message to the server log.

The goals karaf:assembly and karaf:archive MUST be called to create the custom karaf assembly as shown in the command below -

    mvn clean install karaf:assembly karaf:archive 

# Running on OpenShift v3

If you would like to create an application template to start apps like this one on OpenShift v3, then just run the following OpenShift command:

   curl -s -L https://raw.githubusercontent.com/dhirajsb/camel-hello-world/master/os3-app-template.json | oc create -f -
   
This will add the 'fuse-karaf' App to the list of Apps that you can create in the OpenShift v3 console when you click the Add to project button.
