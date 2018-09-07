# Messaging Demo

## Install and Run AMQ and Fuse
### Get the Binaries
The `dist/readme.txt` file contains the list of binaries needed for
this demo.  Please go to the [Red Hat customer service portal](https://access.redhat.com/) and
download the binaries to the `dist` directory.

### Check the Configuration
Please review the `demo.conf` configuration file.  If you change
any of the variables for the distribution versions, make sure that
they match the binaries in the `dist` folder.

### Start AMQ
In a terminal window, install and start AMQ using the commands:

    ./install-amq.sh
    ./start-amq.sh

AMQ is fully started when you see a line in the log output similar
to the following:

    2018-06-18 09:48:53,359 INFO  [org.apache.activemq.artemis] AMQ241004: Artemis Console available at http://localhost:8161/console

### Start Fuse
In a separate terminal window, install and start Fuse using the commands:

    ./install-fuse.sh
    ./start-fuse.sh

Fuse is fully started when you see the prompt `karaf@root()>`.

### Hawtio Console
You can browse to http://localhost:8181/hawtio and login using
the credentials `admin/admin` (unless you changed them in the
`demo.conf` file).  Next, select `Camel` on the left hand side to
see the live metrics for routes as the messages are processed.

### AMQ Console
You can browse to http://localhost:8161/console and login using the
credentials `admin/admin1jboss!` (unless you changed them in the
`demo.conf` file).  Next, examine the destination addresses.

## Shutdown and Clean Up
Simply `CTRL-C` in the window where you started AMQ.  For Fuse,
type `shutdown` in the console.  To reset everything, run the
command:

    ./clean.sh

