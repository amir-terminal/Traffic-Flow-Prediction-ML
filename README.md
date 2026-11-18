# M4 Traffic Flow Prediction

A group project for CSMAD coursework on forecasting traffic flow on the M4. The analysis combines traffic counts, weather observations, and a school-calendar feature to compare regression and time-series models.

**Group 02:** Yassine, Amir, and Ahmed.

## Explore the analysis

The [HTML report](02_CSMAD_CW2.html) provides a saved view of the coursework. Download it and open it in a browser, or run the [notebook](02_CSMAD_CW2.ipynb) from the repository root. The repository records Python 3.11.7 in [`.python-version`](.python-version).

~~~bash
python -m venv .venv
source .venv/bin/activate
python -m pip install notebook numpy pandas matplotlib seaborn scikit-learn statsmodels
python -m notebook 02_CSMAD_CW2.ipynb
~~~

| Path | Contents |
| --- | --- |
| [data/traffic/](data/traffic/) | Traffic counts from two sites spanning 2021 through September 2024 |
| [data/weather/](data/weather/) | Annual weather observations and format references |
| [data/dates/](data/dates/) | Reading school-term calendars |
| [modules/preprocessing.py](modules/preprocessing.py) | Traffic and weather cleaning and alignment |
| [modules/features.py](modules/features.py) | Time and calendar features |
| [modules/regression.py](modules/regression.py) | Linear regression, Ridge, and Lasso |
| [modules/timeseries.py](modules/timeseries.py) | Time-series diagnostics, ARIMA, and seasonal models |
| [modules/visualization.py](modules/visualization.py) and [modules/audit.py](modules/audit.py) | Plots and data quality checks |

## Contributions

Work on a branch and submit a pull request to `main`. Put analysis logic in [modules/](modules/) and use the notebook to show results. Coordinate edits to the shared notebook to avoid merge conflicts. Use `timestamp` for time and `total_volume` for the traffic target. The preprocessing merge defaults to 15-minute intervals and accepts a configurable frequency.
