# Data-Science-Practicum-1
# Who Is About to Withdraw: an early warning for distance learning tutors
Akshaya Chevva, MSDS 692 Practicum I, Regis University

## The question

Among students still enrolled at day 28 of a distance learning course, which students should a tutor phone first to reach those who will later withdraw?

## Main finding

Students who had submitted no marked work by day 28 withdrew at 36.4 percent, against 17.6 percent for students who had (a ratio of 2.07). For the same number of contacts (2,946 students), a list of students with no marked work captured 23.8 percent of later withdrawals, against 16.8 percent for a list of the least active students. This project shows who is at risk. It cannot show whether contacting them helps, because the data has no record of any contact.

## What is in this repository

- `practicum_master.ipynb`: the whole analysis in one notebook, organised by week (checking the data, finding the signal, comparing models, redesigning the chart and fixing the banked-marks problem, checking the slide numbers, preparing for questions). The first cell is a setup cell.
- `requirements.txt`: the Python packages the notebook imports.
- `studentInfo.csv`, `studentRegistration.csv`, `studentAssessment.csv`, `assessments.csv`: four of the five data files the notebook reads. `courses.csv` and `OULAD.names` come with the original dataset.
- `Practicum 1_Final ppt.pptx`: the final presentation deck.

## Data

The data is the Open University Learning Analytics Dataset (CC BY 4.0). The notebook reads five files: `studentInfo.csv`, `studentRegistration.csv`, `studentAssessment.csv`, `assessments.csv` and `studentVle.csv`.

`studentVle.csv` (about 10.6 million rows) is too large for GitHub and is **not** in this repository. Download it from either:

- https://archive.ics.uci.edu/dataset/349/
- https://analyse.kmi.open.ac.uk/open_dataset

and put it in the same folder as the notebook.

## How to run it

1. Install Python 3, then the packages: `pip install -r requirements.txt`
2. Download this repository and add `studentVle.csv` next to the notebook, as described above.
3. Start Jupyter with `jupyter notebook` and open `practicum_master.ipynb`.
4. Choose Kernel, then Restart and Run All. The first cell creates the folders the notebook saves charts into and copies the data files into `Week 1/data/`, where the rest of the notebook reads them. Loading `studentVle.csv` takes a while.

## Notes for reading the notebook

- The notebook is in week order. Sections before Week 5 give numbers from before the banked-marks fix (marks carried over from an earlier attempt and dated day -1). The final numbers are from Week 5 onward and in the paper and deck.
- The random forest and gradient boosting models are each fitted with five random seeds.
- Training uses the presentations 2013B, 2013J and 2014B, and testing uses 2014J. The analysis is repeated with 2014B held out.
