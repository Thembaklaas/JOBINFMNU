# JOBINFMNU

## Overview

`JOBINFMNU` is an IBM i CLLE job information utility with an interactive display menu.

The program accepts a job number, user, and job name, then provides menu options for viewing information about the selected job.

## Features

1. Display job information using `DSPJOB`
2. Display the job log using `DSPJOBLOG`
3. Display job messages using `DSPMSG`
4. Retrieve job status using the IBM i `QSYS2.JOB_INFO` service
5. Exit the application

## IBM i technologies demonstrated

- CLLE
- DDS display files
- `DCLF`
- `SNDRCVF`
- `DSPJOB`
- `DSPJOBLOG`
- `DSPMSG`
- `RUNSQL`
- `QSYS2.JOB_INFO`
- `OVRDBF`
- `RCVF`
- `MONMSG`
- IBM i message handling

## Project structure

```text
JOBINFMNU/
├── README.md
├── JOBINFMNU.CLLE
└── JOBINFMNU.DSPF
```

## Processing flow

The program:

1. Receives the job number, user, and job name as parameters.
2. Builds the job identifier in the format `number/user/name`.
3. Displays the interactive `JOBMENU` display format.
4. Processes the user's menu selection.
5. Executes the corresponding IBM i job command or SQL query.
6. Returns to the menu until the user selects Exit.

## Job status processing

The job status option clears the `JOBSTATUS` work file, retrieves `JOB_STATUS` from `QSYS2.JOB_INFO`, reads the resulting record with `RCVF`, and displays the status to the user.

The original source contained environment-specific library, user, and job values. Those values have been anonymized in this portfolio version.

## Current status

**Work in Progress**

This repository is a portfolio version of the project and is intended to demonstrate IBM i / AS400 development techniques and document the project's progression.
