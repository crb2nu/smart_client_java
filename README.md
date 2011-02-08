#SMArt Java Client Library v0.2
Nate Finstein, Children's Hospital Informatics Program

## Obtaining the code, building a sample app

0.  To get started with the SMArt Java Client Library, you'll need

 * git
 * java
 * ant >= 1.7.0

1.  Obtain the code, build the client library from the SMArt ontology,
and automatically build a sample servlet:

    git clone https://github.com/chb/smart_client_java.git
    cd smart_client_java/bin
    sh ./build.sh

2.  If all goes according to plan, you should be able to run the
`RxReminder` sample servlet now:

 * Copy `build/smartapp.war` to `<tomcat-directory>/webapps`
 * Start up tomcat (on port 8000)
 * Follow instructions at http://dev.smartplatforms.org

---
## Building your own app

When you're ready to build your own app, you'll find the required
dependencies in:

    build/SMArtClient-0.2.jar
    lib/*.jar

The sample servlet is a good place to start:
    src/org/smartplatforms/client/tests/Reminder.java

---
## Specifying a SMArt ontology file

By default, the client library is built against the current
cloud-hosted SMArt ontology file at:

    http://sandbox-api.smartplatforms.org/ontology.

This is probably what you want!  But if you'd like to point to a
different location, just change the `ontology_location` parameter in
`bin/build.sh` to point to any URL or local file.
(e.g. -Dontology_location="/home/me/smart.owl")