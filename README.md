## Prepare Environment

1. create wls domain
2. modify bin/common_env.sh according to your environment
3. modify config/jms.properties & saf.properties according to your requirements
4. start wls domain
5. update domain with command: java -jar jms-saf-demo.jar -r i
6. generate saf client configuration file with command: ./main.sh c
7. generate  encrypted password with command: ./main.sh p
8. update saf client configuration file with password generated by above step.
9. generate full wls client jar with command: ./main.sh g
10. generate jms-saf-demo.jar via IntelliJ Idea "export jar" function.
11. modify config/app.properties according your requirements

## Usage

jms-saf-demo.jar is merged from  wlfullclient.jar & commmons-cli-1.3.1.jar & wls-api.jar & this project and this jar is generated by IntelliJ Idea.

PS: You have to generated this jar by yourself due it's size too large to upload to github.

Show help:

    java -jar jms-saf-demo.jar

Initialize domain with jms resources:

    java -jar jms-saf-demo.jar -r i

Cleanup all jms resources in domain:

    java -jar jms-saf-demo.jar -r u

Send messages:

    java -jar jms-saf-demo.jar -r s -n 100000

Cleanup destination:

    java -jar jms-saf-demo.jar -r c

Monitor:

    java -jar jms-saf-demo.jar -r m


Compact store:

    ./main.sh z
 
Tested on WLS12.2.1.1.0.

## Known Issues
1. paging setting doesn't work

## TODO
1. add stream support
2. add no-wait receiver
3. add welcome window

