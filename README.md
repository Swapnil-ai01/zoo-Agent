# zoo-Agent
This is my Gen AI project where i use and learn multi agent AI LLM model integration and cloud tools. This is the good example of multi agent project where i use ( Google ADK, Google Cloud console, artifacts ).

<h4>How to run this project.</h2>
<ul>
  <li>Make a project in google cloud console.</li>
  <li>Activate Cloud Shell.</li>
  <li>git clone https://github.com/Swapnil-ai01/zoo-Agent.git</li>
  <li>Make .env file in zoo-Agent.</li>
  <li>Write PROJECT_ID, PROJECT_NUMBER from Navigation menu > Cloud overview > Project info.</li>
  <li>Write SA_NAME what you set your service name.</li>
  <li>Now write SERVICE_ACCOUNT from Navigation menu > IAM & Admin > Service Accounts. If you don't have create it.</li>
  <li>And write MODEL="gemini-2.5-flash"</li>
  <li>For example (.env):-<br>
  PROJECT_ID=zoo-agent-XXXX<br>
PROJECT_NUMBER=123456789<br>
SA_NAME=zooService<br>
SERVICE_ACCOUNT=abc@developer.com<br>
MODEL="gemini-2.5-flash"</li>
  <li>Now we have to do deployment:- Run this code in terminal<br>
  uvx --from google-adk==1.14.0 \<br>
adk deploy cloud_run \<br>
  --project=$PROJECT_ID \<br>
  --region=europe-west1 \<br>
  --service_name=zoo-guide \<br>
  --with_ui \<br>
  . \<br>
  -- \<br>
  --labels=dev-tutorial=codelab-adk \<br>
  --service-account=$SERVICE_ACCOUNT<br>
</li>
  <li>Use your agent.</li>
  <li>If you want to do clean up environment:- Run this code in terminal<br>
  gcloud run services delete zoo-guide --region=europe-west1 --quiet<br>
gcloud artifacts repositories delete cloud-run-source-deploy --location=europe-west1 --quiet</li>
</ul>
