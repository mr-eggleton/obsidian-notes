# Business Need

- Display exam details for mock and formal exams at UTC Sheffield Sites and an accurate clock on display screens.
- Show upcoming exams on other display screens
- Do it based on the report from SIMS and the exam board excel sheets
- Booster timing and locations
- Make the exam support staffs life easier with knowing where and when things are needed, with out getting in the way.

# Missing features

- Multi site
- SIMS file uploads
- Static build ?
- Validation
- Sticky but tweakable exam length in the timer
- Automated / assisted fetching of exam board spreadsheets
- Consistent layout
- Single start time by default
- Adhoc Timer
- Exam and booster times for each day of a season rendered to images for powerpoint?
- What rooms and exams today / tomorrow one page view
- Reader & Writer tracking

# Current Features

```mermaid
mindmap
	root((Exam Timer))
		Data Gathering
			Formal
				Spreadsheet from exam boards
					OCR
					Pearson
					Edxcel
					AQA
			Internal
				Lesson Time Override
				SIMS Report
				YAML
			One Offs
			Boosters
			Staffing
		Processing
			Normalise
				Exam Codes
					splitExamCodes
					createRange
				Sessions to am/pm
			getGroups
				groupOnDuration
			getOCRUnit
			getShortRoom			
			
		Displays
			Exam Timer
				Clock
				Editing
				Menu
				Keyboard input
			Table
			Boosters
			Index
			Today
			Calendar
			No Exams
			Staff
```

# Design
# Conceptual ERD

```mermaid
erDiagram
		EXAMFILE ||--o{ EXAM : contains
        EXAMFILE ||--o{ SEASON : contains
        SCHOOL ||--o{ SEASON : have
        SEASON ||--o{ EXAM : contains
        EXAM ||--o{ ROOM : uses
        EXAM }|--o{ TIME : at
        SCHOOL ||--o{ SCREEN : have
		SCREEN ||--o{ ROOM : uses
        SCREEN ||--o{ TIME : at
```
