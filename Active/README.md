1. Download atlassian-agent.jar and place it anywhere you will not delete it. The jar package can be downloaded from Cloud Disk: https://pan.baidu.com/s/1ufRvA0wF1bUad0-xltW8gw
2. Set environment variables
Global settings:

tailf -1 /etc/profile
export JAVA_OPTS="-javaagent:/path/to/atlassian-agent.jar ${JAVA_OPTS}"
source /etc/profile

Or:
You can put: export JAVA_OPTS = "-javaagent: /path/to/atlassian-agent.jar $ {JAVA_OPTS}" into the setenv.sh or setenv.bat (for windows Using.

Or:
You can also execute it directly from the command line: JAVA_OPTS = "-javaagent: /path/to/atlassian-agent.jar" /path/to/start-confluence.sh to start your service.
3. Restart the service
4. Check if the configuration is successful, use ps -ef | grep java to see if it has the -javaagent parameter

Activation steps
1. Under the premise of confirming that the environment is configured, execute the following command. Here is an example of the Mohamicorp-render-markdown plugin for confidence.

java -jar atlassian-agent.jar -p mohamicorp-render-markdown -m admin@chuangyue.cn -n name   -o https://mohami.io/  -s B93T-TNVL-Q1QC-LZ3N

For parameter details, you can run java -jar atlassian-agent.jar to view.
-p refers to the application key / plugin keyword, here mohamicorp-render-markdown


-m refers to the mailbox, just fill in it.
-n refers to the name, and you can fill in
-o to refer to the developer who provided the product, specifically the developer in the picture above.
-s No doubt, this is your server-id, which can be viewed in the authorization details.

