# HoosList Course Data Scraping & Visualization

## Data Dictionary 


### Dataset Scope

This dataset contains all courses at the University of Virginia with a DS (Data Science) mnemonic for the selected semester.

Each row represents one scheduled instructional section (lecture, laboratory, discussion, independent study, or thesis research). Courses with multiple sections therefore appear multiple times.

Independent Study and Thesis Research sections are retained in the dataset to preserve completeness. These courses do not have scheduled meeting times and therefore contain missing values in time-related fields.

---

### Variables

#### Course Mnemonic
- **Type:** String  
- **Description:** Official course subject and number for Data Science courses (e.g., DS 1001).  
- **Example:** DS 4024  
- **Notes:** All DS courses for the selected semester are included.

---

#### Course Title
- **Type:** String  
- **Description:** Official title of the course as listed in the university catalog.  
- **Notes:** Repeated for each scheduled section of a course.

---

#### Instructor
- **Type:** String  
- **Description:** Name of the instructor assigned to the course section.  
- **Notes:** May contain “TBD” if an instructor has not yet been assigned. May be missing for Independent Study or Thesis sections.

---

#### Room
- **Type:** String  
- **Description:** Building and/or room where the course section meets.  
- **Notes:** Room information was obtained from the logged-in Hooslist interface. Sections that do not meet in a physical classroom (e.g., Independent Study, Master’s Level Thesis Research, Dissertation Research) do not have assigned rooms and are left blank. Web-based courses are labeled as "Web-Based Course."

---

#### Day(s) of the Week
- **Type:** String  
- **Description:** Abbreviated days on which the course section meets (e.g., MoWe, TuTh).  
- **Notes:** Independent Study and Thesis sections may have missing values.

---

#### Start Time
- **Type:** Time Object  
- **Description:** Scheduled start time of the class meeting.  
- **Format:** HH:MM:SS  
- **Notes:** Missing for courses without scheduled meeting times (e.g., Independent Study, Thesis Research).

---

#### End Time
- **Type:** Time Object  
- **Description:** Scheduled end time of the class meeting.  
- **Format:** HH:MM:SS  
- **Notes:** Missing for courses without scheduled meeting times.
