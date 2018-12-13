
please start all commands but without the last one. We are going to code
together the first super easy Google Assistant App

## WINDOWS:

1. Before we start you need to ensure that Git is properly configured to handle line endings.
`git config --global core.autocrlf true`

2. Clone our repository. Your repository will be saved automatically in your Documents in the directory googleHomeAssistantExpressNodeJS.
`git clone https://github.com/falent/demoMeetUp.git  C:\Users\%username%\Documents\ga\demo`

3. Create a new Docker network:
`docker network create myNetwork`


4. Run the _ngrok_ Docker container in your cmd terminal **and do not close this tab!**
`docker run --rm -it  --network myNetwork wernight/ngrok ngrok http myAssistant:5000`

Lets finish code together before we execute point 5!

5. Open a new cmd window and run an _Google Assistant_ Docker container in your created network.
`docker run -v //c/Users/%username%/Documents/ga/demo:/skill -it --rm --network myNetwork --name myAssistant falent/google_home_assistant_express_node_js_server`


## LINUX:

1. Clone our repository. Your repository will be saved automatically in your Documents in the directory googleHomeAssistantExpressNodeJS.
`$ git clone https://github.com/falent/demoMeetUp.git  ~/Desktop/Template/Google_Assistant_universal_skill_template_demo`

2. Create a new Docker network:
`$ sudo docker network create myNetwork`


3. Run the _ngrok_ Docker container in your cmd terminal **and do not close this tab!**
`$ sudo docker run --rm -it  --network myNetwork wernight/ngrok ngrok http myAssistant:5000`

Lets finish code together before we execute point 4!

4. Open a new cmd window and run an _Google Assistant_ Docker container in your created network.
`docker run -v ~/Desktop/Template/Google_Assistant_universal_skill_template_demo:/skill -it --rm --network myNetwork --name myAssistant falent/google_home_assistant_express_node_js_server`
