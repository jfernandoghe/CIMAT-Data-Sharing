# Calibration-Dataset

## Dataset for Eye Tracking calibration using all information from:

> Dalrymple, K.A., Manner, M.D., Harmelink, K.A., Teska, E.P., & Elison, J.T. (2018). An examination of recording accuracy and precision from eye tracking data from toddlerhood to adulthood. Frontiers in Psychology, 9(803), 1-12. doi: 10.3389/fpsyg.2018.00803.

This csv file columns contain:
**Participant x', y', x, y, CalPoint, Timestamp**
with these calibration points:
* 1- "TopLeft": [480.0, 270.0],
* 2- "TopRight": [1440.0, 270.0],
* 3- "Middle/Center ": [960.0, 540.0],
* 4-"BottomLeft": [480.0, 810.0],
* 5- "BottomRight ": [1440.0, 810.0]

Original csv with the columns:

.CSV Files:
All .csv files have the same columns:
- Column A: ParticpantName. This will match the file name and the name on the Participant Information spreadsheet.
- Column B: Fixation Filter. We used an I-VT Filter provided by Tobii Studio. The I-VT fixation filter was set to define the minimum fixation duration to 60 ms, with a velocity threshold of 30 °/s. A fixation filter is necessary so that the processing script can identify samples that should be grouped together when calculating precision.
- Column C: MediaName. We showed 5 stimuli at various locations on the screen. They were named “BottomRight”, “TopRight” “BottomLeft”, “TopLeft”, and “Middle” (or “Center”). The centroids of these stimuli were at known locations so that we could compute the difference between the calculated gaze location (columns H and I ) and the location of the stimulus. See below for stimulus location.
- Column D: RecordingTimestamp. Time from the beginning of the recording in increments of 3.3ms.
- Column E: FixationIndex. Numbers the fixations sequentially so you can determine when a new fixation began (defined by fixation filter)
- Column F: GazeEventType. Fixation, Saccade, or Unclassified, based on fixation filter
- Column G: GazeEventDuration. Duration of the fixation, saccade, or unclassified event, in ms.
- Column H: GazePointX(ADCpx). X axis screen location of detected gaze in pixels. Average of both eyes. Top left corner of the screen is 0,0.
- Column I: GazePointY(ADCpx). Y axis screen location of detected gaze in pixels. Average of both eyes. Top left corner of the screen is 0,0.
- Column J: DistanceLeft. Distance between left eye and eye tracker, in mm.
- Column K: DistanceRight. Distance between right eye and eye tracker, in mm.
- Column L: ValidityLeft. Tobii validity code for reliability of gaze data from left eye. 0=valid , 4=invalid.
- Column M: ValidityRight. Tobii validity code for reliability of gaze data from right eye. 0=valid , 4=invalid.

Locations of stimuli, in X,Y screen coordinates (pixels)
- "TopLeft": [480.0, 270.0],
- "TopRight": [1440.0, 270.0],
- "Middle/Center ": [960.0, 540.0],
- "BottomLeft": [480.0, 810.0],
- "BottomRight ": [1440.0, 810.0]
