# ibllib.io

## ibllib.io.raw_data_loaders

### Methods & Functions

get_port_events
- Returns all event timestamps from pod raw data trial that match ‘name’
- Looks in *trial[‘behavior’][‘Events timestamps’]*
- Data ret types:
- How will/could/is this help(ing) us?

load_ambient_sensor
- Loads ambient sensor data from session
- Data ret types:
- How will/could/is this help(ing) us?

load_bpod
- Load both settings and data from bpod (.json and .jsonable)
- Data ret types:
- How will/could/is this help(ing) us?

load_bpod_fronts
- Loads BNC1 and BNC2 bpod channels times and polarities from *session_path*
- Data ret types:
- How will/could/is this help(ing) us?

load_camera_frameData
- Loads binary frame data from Bonsai camera recording workflow
- Data ret types:
- How will/could/is this help(ing) us?

load_camera_frame_count
- Load the embedded frame count for a given session
- Data ret types:
- How will/could/is this help(ing) us?

load_camera_qpio
- Load the GPIO for a given session
- Data ret types:
- How will/could/is this help(ing) us?

load_camera_ssv_times
- Load the Bonsai frame and camera timestamps from *Camera.timestamps.ssv*
- Data ret types:
- How will/could/is this help(ing) us?

load_data
- Load PyBpod data files (.jsonable)
- Data ret types:
- How will/could/is this help(ing) us?

load_embedded_frame_data
- Load the embedded frame count and GPIO for a given session
- Data ret types:
- How will/could/is this help(ing) us?

load_encoder_events
- Load rotary Encoder (RE) events raw data file
- Data ret types:
- How will/could/is this help(ing) us?

load_encoder_positions
- Load Rotary Encoder (RE) positions from raw data file within a session path
- Data ret types:
- How will/could/is this help(ing) us?

load_encoder_trial_info
- Load Rotary Encoder (RE) trial info from raw data file
- Data ret types:
- How will/could/is this help(ing) us?

load_mic
- Load microphone wav file to *np.array* of len nSamples
- Data ret types:
- How will/could/is this help(ing) us?

load_settings
- Load PyBpod settings files (.json)
- Data ret types:
- How will/could/is this help(ing) us?

load_stim_position_screen
- No description, look into it
- Data ret types:
- How will/could/is this help(ing) us?

save_bool
- No description, look into it
- Data ret types:
- How will/could/is this help(ing) us?

sync_trials_robust
- Attempt to find matching timestamps in 2 time-series that have an offset, are drifting, and are most likely incomplete: sizes don’t have to match, some pulses may be missing in any series
- Data ret types:
- How will/could/is this help(ing) us?

trial_times_to_times
- Parameters:
	- raw_trial
- Return:
	- dict of trial data w/ modified timestamps
- Parse and convert all trial timestamps to ‘absolute’ time
- Data ret types:
- How will/could/is this help(ing) us?

# Data Types
raw_trial
- dict
- raw trial data
