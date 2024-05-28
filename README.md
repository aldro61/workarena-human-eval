# WorkArena - Human Evaluation Study

Welcome to the WorkArena human evaluation study.

## Step 1: Setup your environment

Open up a new terminal. Ask the session lead for the password and replace it in the following command. Then, run the command to setup the environment:
```bash
pip install --upgrade browsergym-core && \
pip install --upgrade https://alexdrouin.com/workarena.zip && \
playwright install && \
export SNOW_INSTANCE_URL="https://dev248934.service-now.com/" && \
export SNOW_INSTANCE_UNAME="admin" && \
export SNOW_INSTANCE_PWD="" && \
echo "Installation complete."
```

## Step 2: Initial training
