# ibllib.io
################################### up to and including load_camera_data on https://int-brain-lab.github.io/iblenv/_autosummary/ibllib.io.raw_data_loaders.html?highlight=raw%20data%20loader#
## ibllib.io.raw_data_loaders

### Methods & Functions

get_port_events
- Returns all event timestamps from pod raw data trial that match ‘name’
- Looks in *trial[‘behavior’][‘Events timestamps’]*
- Parameters: trial
- Return data: sorted list of event timestamps
	- Return type: list 
- How will/could/is this help(ing) us?


load_ambient_sensor
- Loads ambient sensor data from session
- Parameters: session_path
- Return data: list of dicts where keys are the environmental details collected by the ambient sesnor (env'l vars stored are: temp, air pressure, and rel. humidity)
	- Return type: list
- How will/could/is this help(ing) us?


load_bpod
- Load both settings and data from bpod (.json and .jsonable)
- Parameters: session_path
- Return data:
	- Settings dict and lists of dicts data
	- Return type: dict
- How will/could/is this help(ing) us?


load_bpod_fronts
- Loads BNC1 and BNC2 bpod channels times and polarities from *session_path*
- Parameters: session_path, data (opt'l) – pre-loaded raw data dict which defaults to false
- Return data: List of dicts BNC1 and BNC2 w/ structure of {'times':np.array, 'polarities':np.array}
	- Return type: list of dicts with numpy array values
- How will/could/is this help(ing) us?


load_camera_frameData
- Loads binary frame data from Bonsai camera recording workflow
- Parameters:
	- session_path (StrPath)
	- camera (str, optional, defaults to left)
	- raw (bool, optional, defaults to false) – whether to return raw or parsed data
	- collections (str, optional, defaults to folders starting with raw_video_data)
- Return data:
	- raw = False
		- pandas.DataFrame, 4 int64 columns, with the following data
			- timestamp
			- float64 embeddedTimeStamp (seconds from start)
			- float64 embeddedFrameCounter (seconds from start)
			- int64 embeddedGPIOPinState (a list of numpy boolean arrays)
	- Return type:
- How will/could/is this help(ing) us?


load_camera_frame_count
- Load the embedded frame count for a given session
- Parameters: session_path, label, raw
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


load_camera_gpio
- Load the GPIO for a given session
- Parameters: session_path, label, as_dicts (T/F), collection
- When as_dicts is false, then the returned raw data are in a boolean array with shape (n_frames, n_pins), otherwise GPIO is returned as a list of dictionaries with keys ('indices', 'polarities')
- Return data: n by 4 boolean array where columns represent state of GPIO pins 1-4
	- Return type:
- How will/could/is this help(ing) us?


load_camera_ssv_times
- Load the Bonsai frame and camera timestamps from *Camera.timestamps.ssv*
- Parameters: session_path, camera (defaults left ?), collection (defaults w/ collection = 'raw_video_data' ?)
- Return data:
	- Array of datetimes
	- Array of frame times in seconds
	- Return type: Arrays
- How will/could/is this help(ing) us?


load_data
- Load PyBpod data files (.jsonable)
- Parameters:
	- session path
	- (optional) time = ...
- Return data:
	- List of len ntrials, where each trial is a dictionary
	- Return type: list of dicts
- How will/could/is this help(ing) us?


load_embedded_frame_data (see documentation for more on this one's output type)
- Load the embedded frame count and GPIO for a given session
- Parameters: session_path, label (e.g. left), raw
	- When raw = True, raw data are returned without processing
	- When raw = False, frame count is returned starting from 0 and the GPIO is returned as a dict of indicies
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


load_encoder_events
- Load rotary Encoder (RE) events raw data file
- Parameters: session_path, settings (defaults to False)
- Events number correspond to the following bpod states:
		1. Correct / hide_stim
		2. stim_on
		3. closed_loop
		4. freeze_error / freeze_correct
- Return data: dataframe with three columns and (ntrials * 3) lines
	- Return type: pd.DataFrame
- How will/could/is this help(ing) us?


load_encoder_positions
- Load Rotary Encoder (RE) positions from raw data file within a session path
- Parameters: session_path, settings (opt'l, defaults to False)
- Positions are RE ticks where :
	- ±512 corresponds to ±180º
	- 0 corresponds to trial stim init position
	- Positive numbers corresponds to rightward mvmt and vice versa
- Raw datafile columns are: position, RE timestamp, RE position, Bonsai timestamp
- Return data: df with 3 columns and N positions
	- Return type: pd.DataFrame
- How will/could/is this help(ing) us?


load_encoder_trial_info
- Load Rotary Encoder (RE) trial info from raw data file
- Parameters: session_path
- Return data: dataframe w/ 9 columns and ntrial rows
	- Return type: pd.DataFrame
- How will/could/is this help(ing) us?


load_mic
- Load microphone wav file to *np.array* of len nSamples
- Parameters: session_path
- Return data: An array of values of the sound waveform
	- Return type: numpy.array
- How will/could/is this help(ing) us?


load_settings
- Load PyBpod settings files (.json)
- Parameters: session_path
- Return data: settings
	- Return type: dict
- How will/could/is this help(ing) us?


load_stim_position_screen
- No description, look into it ?
- Parameters:
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


save_bool
- No description, look into it
- Parameters:
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


sync_trials_robust
- Attempt to find matching timestamps in 2 time-series that have an offset, are drifting, and are most likely incomplete: sizes don’t have to match, some pulses may be missing in any series
- **this part of the documentation seems incomplete**
- Parameters:  t0, t1, diff_threshold, drift_threshold_ppm, max shift
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


trial_times_to_times
- Parameters:
	- raw_trial
- Return:
	- dict of trial data w/ modified timestamps
- Parse and convert all trial timestamps to ‘absolute’ time
- Parameters:
- Return data:
	- Return type:
- How will/could/is this help(ing) us?


# Data
- raw_trial
	- dict
	- raw trial data
