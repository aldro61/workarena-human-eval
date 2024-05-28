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

Then, run the following command to verify that everything works:
```
workarena-human-eval --email YOUR_EMAIL --log human_eval.log --reset-log --curriculum random
```

If you see something like this, it works. You can kill the program for now (CTRL-C).
<img width="1719" alt="image" src="https://github.com/aldro61/workarena-human-eval/assets/2374980/b33e4e10-952c-430a-bfd5-8b9592a78e61">


## Step 2: Initial training
