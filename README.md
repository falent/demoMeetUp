
please start:

WINDOWS:

1. Before we start you need to ensure that Git is properly configured to handle line endings.
`git config --global core.autocrlf true`

2. Clone our repository. Your repository will be saved automatically in your Documents in the directory googleHomeAssistantExpressNodeJS.
`git clone   C:\Users\%username%\Documents\demoMeetUp`

3. Create a new Docker network:
`docker network create myNetwork`

4. Start mongoDB container
`docker run -it --rm --name mongo_database --network myNetwork bitnami/mongodb:latest`

5. Run the _ngrok_ Docker container in your cmd terminal **and do not close this tab!**
`docker run --rm -it  --network myNetwork wernight/ngrok ngrok http myAssistant:5000`

6. Open a new cmd window and run an _Google Assistant_ Docker container in your created network.
`docker run -v //c/Users/%username%/Documents/welcome:/skill -it --rm --network myNetwork --name myAssistant falent/google_home_assistant_express_node_js_server`
