# pwir-template

## Color thresholding

Use `src/threshold.py` to threshold colors. Run `python src/threshold.py` and enter the color
name to configure in the terminal. Then adjust the sliders for the color and press `q` to exit
and save.

Color ranges are saved as dicts in this format:
```python
color_range = {
    "min": (int, int, int), # h_min, s_min, v_min
    "max": (int, int, int)  # h_max, s_max, v_max
}
```
This can be used to filter a HSV image using OpenCV:
```python
filtered_image = cv2.inRange(hsv_image, color_range["min"], color_range["max"])
```

## Configuration

Use the config module (`src/config.py`) to save and load settings and color ranges. There is a
`config.ini` file where your settings are saved.

You can use the `src/config.py` module for saving any settings you need. You can save native Python
objects such as string, int, dict, list, tuple. Example:
```python
import config

# Usage: config.set(section, key, value)
config.set("competition", "robot_id", "A")
config.set("colors", "red", )

# Usage: config.get(section, key)
config.get("competition", "robot_id")
```
