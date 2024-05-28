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



## Step 4: Training: Self-exploration in a real instance

Now, you will spend **15 minutes** experimenting with a real ServiceNow instance. Feel free to navigate the menus, create entries in lists, fill out forms, delete records, etc.

* Navigate to: [https://researchuicopilotdemo.service-now.com/](https://researchuicopilotdemo.service-now.com/)
* Username: `admin`
* Password: `Ask the session lead`


## Step 5: Human evaluation

Now that you've undergone our standardized training, you may start solving tasks from the benchmark. Note that we will log the time taken to solve the tasks as well as your success rate.
Please make sure to remain focussed as much as possible to avoid over-inflating the time to completion measurements.

Run the following command to start the evaluation tool:
```bash
workarena-human-eval --email YOUR_EMAIL --log LASTNAME.log --reset-log --curriculum YOUR_CURRICULUM_FILE
```

**Notes:**
* `YOUR_CURRICULUM_FILE` should point to the curriculum file that was provided by the session lead. This contains the list of tasks assigned to you.
* You may kill the program at any time and restart from where you left off
