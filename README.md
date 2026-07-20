# Team-10-Fitness-Tracker

**THE HOOK**

FitTracker is Team 10's project under the Biomedical Efficiency mini-challenge. The question we aim to answer is whether or not a workout actually moved someone toward their specific fitness goal, despite feeling good about it. FitTracker turns raw wearable sensor data into a clear answer to that question. 

**THE AUDIENCE**

This application is designed for gym-goers to gain a better understanding of their workouts, and learn how to optimize each session.

**THE ENGINE**

This app imports wearable_sensor_data.mat, which contains raw accelerometer and heart rate readings collected during gym sessions, along with each person's stats and fitness goal. Before any metric is calculated, the raw signals are cleaned using fillmissing and movmean. From there, the app computes five metrics: calories burned (using the MET formula), time spent in each heart rate zone, a movement-intensity classification, a composite workout intensity score, and a goal-adjusted efficiency score.

**DASHBOARD FEATURES**
- Session dropdown to switch between workouts
- Zone dropdown that highlights a specific heart rate zone directly on the graph
- Heart rate line graph with zone boundaries
- Bar chart showing time spent in each heart rate zone
- Color-coded lamp (green/yellow/red) to provide a read on workout intensity
- Feedback box with advice personalized to the user's indicated fitness goal

**ACCESSING THE CODE**

To run this code, complete the following steps:
1. **[Click here.](https://drive.mathworks.com/sharing/76f1dbab-16be-47ef-a784-72d71b047028)** You will be redirected to MatLabs with all of the files attached.
2. At the top of the site, you will see a dropdown that says "Open in MATLAB". Click it, and then click "Open in MATLAB Online".
3. You will be asked to sign in to your MATLAB account. If you do not have one, you will need to create an account.
4. On the center-left, you will see a list of files. Double-click on the one named "FitnessTrackerApp.mlapp".
5. You will be redirected to the MATLAB app designer. At the top, you will see a green triangle labeled "Run". Click this.
6. The FitTracker should now be up and running. Click on the Load Data button, and select wearable_sensor_data.mat

From here, you can select each session with the Session drop-down bar. You'll be provided with information on calories burned, effeciency, and intensity metrics. Additionally, there is a
Highlight Zone for each significant heartrate range. You will also be presented with a feedback section that will provide advice on how to better optimize your next session.

**THE REALITY CHECK**
- The app assumes sensor data was collected at a consistent 10 Hz sampling rate.
- Heart rate zone thresholds are calculated from each person's estimated_max_hr_bpm, which is not a clinically measured maximum.
- Activity classification is simplified to a movement-intensity level (Low/Moderate/High) rather than stating the exact activity
- The app requires a .mat file specifically (no .csv files)
