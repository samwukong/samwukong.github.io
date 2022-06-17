---
description: Instructions to use the app
---

# DA6 Generator

[DA6 Generator](https://www.niis.io/da6\_gen)

## Generator for a DA6 Duty Roster

### Configuration options

#### Step 1:

Enter the data required, such as:&#x20;

* Nature of Duty (ex. "BDE Staff Duty")
* Organization
* From and To dates (can be almost any length from a few days to months)
* Number of people per day for duty

#### Step 2:

Select highlight weekends if you'd like.

#### Step 3:

Upload a .csv file with the following columns:

Rank, Name, Days Since Last

NOTE: A .csv file can be created either in Microsoft Excel, Apple Numbers, or even just on a text editor application. It must be saved as a .csv and only contain the required information with commas separating each piece of information. Examples:

For Rank - You can put something like SGT(P) with a comma at the end. That's fine.

For Name - You must spell the names without commas! If its Jane Doe, then "Doe Jane" is fine... "Doe, Jane" is NOT. You can add things like "Doe Jane (Section)".

For Days Since Last - You need to put some value from 1 to whatever.

#### Step 4:&#x20;

Click on the "Generate DA6 Roster".

This automatically creates a DA6 roster which can be copied to Excel for easy printing.

Each cell is 'clickable' to change the Service Member's status during that day between.

Available, 'A', 'D', or 'U'. A green box with triple slash means you're manually assigning duty of a given day. See AR 220-45 excerpt below for the meaning of these designators.

#### Step 5:

Once satisfied with the duty roster, click "Generate Memo". This will give you two columns below the DA6 data that you can copy and paste easily enough into a memo.

#### Step 6:

Click on the "Generate Final Duty Status".&#x20;

This button will prompt you to download a new .csv file with all of the personnel entered on the first .csv file, but it will also return their final recorded number of days since last duty.

This can then be used to upload the following month to create the new DA6. Pretty handy.



NOTE: If you refresh or close the page, all work is lost. This app DOES NOT remember or save your file anywhere. It processes the data right in the browser.



From AR 220-45

(1) Soldiers who are absent or otherwise not available because of leave, pass, special duty, temporary duty, illness in line of duty, or any other authorized reason (not due to misconduct) will be indicated by the letter "A." When a new DA Form 6 is initiated that carries over a nonchargeable status from the previous DA Form 6, a superscript number (for example, A3) will be manually added to the abbreviation "A" to indicate the last number charged, as shown on the previous DA Form 6, before the Soldier entered upon the nonchargeable status. Entering such a number in the first column of a new DA Form 6 eliminates the necessity for referring to the previous DA Form 6 when the Soldier returns to a chargeable status.  Note. Soldier on temporary duty travel that does not extend beyond regular duty hours will not qualify for an "A" for that day of temporary duty.

(2) Soldiers eligible for detail who could not be selected because of previous detail or other duty will be indicated by the letter "D."

(3) Soldiers not available because of being absent without leave, in arrest, in confinement, illness not in line of duty, or otherwise not available as a result of their own misconduct will be indicated by the letter "U."





### Technical Details

The data structure of the 'da6\_pers\_list' is the following

\- Rank

\- Name

\- Duty

\-- date: yyyy-mm-dd

\-- daysSinceLastDuty: Number

\-- dutyStatus: Number or Letter

The 'dutyStatus' is either the days since the last duty (if the Service Member is available for duty) or the 'A', 'U', or 'D'. Triple slashes "///" represents a duty day.



### Rank will prioritize in this descending order:&#x20;

If you're not a joint service organization, that's fine. It will ignore the unused ranks.

USA -> USN -> USAF

\- MAJ

\- LCDR&#x20;

\- Maj&#x20;

\- CPT

\- LT&#x20;

\- Capt&#x20;

\- 1LT&#x20;

\- LTJG&#x20;

\- 1st Lt&#x20;

\- 2LT&#x20;

\- ENS&#x20;

\- 2d LT

\- MSG&#x20;

\- SCPO&#x20;

\- SFC&#x20;

\- CPO&#x20;

\- MSgt&#x20;

\- SSG&#x20;

\- PO1&#x20;

\- TSgt&#x20;

\- SGT&#x20;

\- PO2&#x20;

\- SSgt&#x20;

\- CPL&#x20;

\- PO3&#x20;

\- SPC&#x20;

\- SrA&#x20;

\- PFC&#x20;

\- SN&#x20;

\- A1C&#x20;

\- PV2&#x20;

\- SA&#x20;

\- Amn&#x20;

\- PVT&#x20;

\- SR&#x20;

\- AB
