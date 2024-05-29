# WorkArena - Human Evaluation Study

Welcome to the WorkArena human evaluation study.

## Step 1: Fill out consent form and survey

Thank you for agreeing to participate in our study. Before continuing, please fill out:
1. The [consent form](https://forms.gle/edJ1QbvwAGQZ7VKw8)
2. The [demographics survey](https://forms.gle/2ENTNj9SARAc82FW6)

## Step 2: Setup your environment

*If you are being provided a preconfigured laptop, skip this step*

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
```bash
workarena-human-eval --email YOUR_EMAIL --log test.log --curriculum random
```

If you see something like this, it works. You can kill the program for now (CTRL-C).
<img width="1719" alt="image" src="https://github.com/aldro61/workarena-human-eval/assets/2374980/b33e4e10-952c-430a-bfd5-8b9592a78e61">


## Step 3: Training: Introductory presentation

Listen to the following presentation, which is meant to bring everyone up to speed on our project, the ServiceNow platform, and our evaluation console.

**TODO: put talk video**
<img width="814" alt="image" src="https://github.com/aldro61/workarena-human-eval/assets/2374980/8bd574fa-6cfd-49f2-8468-db7c3e4a9b22">




## Step 4: Training: Self-exploration in a real instance

Now, you will spend **15 minutes** experimenting with a real ServiceNow instance. Feel free to navigate the menus, create entries in lists, fill out forms, delete records, etc.

* Navigate to: [https://researchuicopilotdemo.service-now.com/](https://researchuicopilotdemo.service-now.com/)
* Username: `admin`
* Password: `Ask the session lead`


## Step 5: Human evaluation

Now that you've undergone our standardized training, you may start solving tasks from the benchmark.

**Rules** 
Please help us standardize the study by following these rules:
* You may use a note-taking app to keep track of any information you need
* You may use multiple tabs, but please use the provided button (+) to open them
* We will log the time taken to solve the tasks so please make sure to remain focussed as much as possible. If you need a break, kill the program and restart it when ready.

Run the following command to start the evaluation tool:
```bash
workarena-human-eval --email YOUR_EMAIL --log LASTNAME.log --reset-log --curriculum YOUR_CURRICULUM_FILE
```

**Important Notes:**
* `YOUR_CURRICULUM_FILE` should point to the curriculum file that was provided by the session lead. This contains the list of tasks assigned to you.
* Checkpoints are made. You may kill the program at any time and restart from where you left off.
* If, for any reason, the page does not properly or appears to have crashed, please restart the program.


## Step 6: Hand in your results

If you get to this point, thank you so much! We are very grateful for your contribution and will make sure to acknowledge it in the paper. Please send the `LASTNAME.log` file to alexandre.drouin@servicenow.com. You are done!
