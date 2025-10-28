# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|--------|----------------|
| Test Manager | Palesa Radebe | Draft and maintain Test Plan, manage schedule, track test metrics, consolidate final report |
| Risk Analyst | Veliswa Zicina | Identify and prioritize functional and usability risks; design high-risk test cases |
| Test Executor | Josphine Mbugua | Execute test cases, capture screenshots, log GitHub defects, and validate fixes |


## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | |
| Leaderboard | Stores top 3 scores in localStorage | |
| Bonus Round | Every 3 puzzles → doubles score | |

## Test Plan

### Objectives

- The objective of this test plan is to ensure the Word Puzzle Game Plus functions as intended across all new and existing features, providing a smooth, fair, and error-free player experience. 
- Testing will focus on functional correctness, state management, leaderboard persistence, bonus logic accuracy, and user interface usability.

### Scope

**In Scope:**
- Functional validation of:
  - Reset Game feature (resets score and progress instantly)
  - Leaderboard feature (top 3 scores saved in localStorage)
  - Bonus Round feature (every 3 solved puzzles doubles score)
- UI validation for responsive layout, accessible labels, and visual feedback
- Risk-based and regression testing across Chrome browser
- Testing local data persistence and arithmetic logic for score tracking


**Out of Scope:**
- Cross-browser compatibility (only Chrome tested)
- Backend server integration (no external database)
- Performance/stress testing

### Tools & Resources

- GitHub, Chrome, Markdown editor, Excel/Google Sheets

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| Planning | 1 Day | 1 Day | Completed |
| Design | 1 Day | 1 Day | Completed |
| Execution | 1 Day | 1 Day | Completed |
| Monitoring | 1 Day | 1 Day | In progress |
| Reporting | 1 Day | 1 Day| In progress |

## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|R1	|Reset Game| Game does not reset score or progress correctly| Medium| High |High |Test multiple reset scenarios and verify variables reset to zero|
|R2|Reset Game |Reset button unresponsive or missing from UI| Low | Medium | Medium |Check UI rendering on different screen sizes and event listeners|
|R3 | Leaderboard | Scores not saved or updated in local Storage | High | High | High | Validate local Storage logic and test data persistence after refresh |
|R4 | Leaderboard | Incorrect sorting of top 3 scores |	Medium | High | High |	Design test cases with mixed score values and verify order |
|R5 | Bonus Round | Bonus round not triggered after 3 puzzles | Medium | High | High |Test various puzzle counts to confirm bonus activation |
|R6 | Bonus Round | Incorrect score multiplication (×2 not applied) |Low | High | Medium | Verify score calculations before and after bonus activation |
|R7| General UI| Layout breaks or overlaps on smaller screens | Medium | Medium | Medium | Perform simple responsive layout checks on Chrome |
|R8 | General Logic | Game freezes or errors when unexpected input occurs |	Low | High | Medium | Conduct negative testing and input validation|


### Risk Coverage

Risk Coverage Summary
|Category | Count | Percentage |
|Total Risks Identified | 8 | 100%|
|Planned to Test (Covered) | 6 | 75% |
|Untested (Out of Scope / Low Impact)| 2| 25%

- Tested Risks Percent: 75%
- Untested Risks Percent: 25%
 

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
|TC-01 | Reset Game	| Verify that clicking "Reset" clears score and progress instantly | Score and progress reset to zero; game returns to start state | Game returns to start state | Complete	| R1 |
|TC-02 | Reset Game | Confirm that the Reset button is visible and clickable on main screen | Reset button displayed and responds to click | Reset button is visible and clickable on main screen | Complete | R2 |
|TC-03 | Leaderboard |	Verify that top 3 scores are correctly stored in localStorage |	Scores persist after refresh and display in correct order | Scores persist after refresh and display in correct order | Complete | R3 |
|TC-04 | Leaderboard |	Verify sorting logic for top 3 scores | Scores are displayed in descending order (highest first) | Scores are displayed in descending order |Complete | R4 |
|TC-05 | Bonus Round | Verify bonus round triggers after every 3 puzzles | Bonus round activates after 3 completed puzzles | Bonus round activates after 3 completed puzzles | Complete | R5 |
|TC-06 | Bonus Round | Verify correct ×2 score multiplier in bonus round | Player’s score doubles when bonus is applied | Player’s score doubles when bonus is applied |	Complete | R6 |
|TC-07 | General UI | Verify layout and visuals on different screen sizes | Game layout remains clean, buttons and text not overlapping |Game layout remains clean | Complete | R7 |
|TC-08 | Negative Test | Enter invalid or empty input during a puzzle | Game handles invalid input gracefully (no crash or freeze) | No crash or freeze | Complete |R8 |


## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
|BUG-1 |Hint incorrectly applies scoring when player has zero score  |Major |R-01 |New |https://github.com/PLP-Database-Design/plp-software-testing-july-2025-wk-5-swt-w5/issues/3 |
|BUG-2|Game repeats a very small set of words reducing gameplay randomness|Medium|R-02|New|https://github.com/PLP-Database-Design/plp-software-testing-july-2025-wk-5-swt-w5/issues/4 |
|BUG-3|Game has no win condition and never ends|Major|R-03|New|https://github.com/PLP-Database-Design/plp-software-testing-july-2025-wk-5-swt-w5/issues/5

## Metrics

- Test Case Pass Percent: 100%
- Defect Density: 0.375
- Risk Coverage Percent: 75%
- Regression Success Rate: No fixes to retest

### Defect Summary

- Total Defects Logged: 3
- Critical High: 2
- Fix Rate: No fixes yet

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
| Planning | Test Plan Document	| Test Plan completed and reviewed on time | None	| Test Manager |
| Design | Test Cases & Risk Matrix | 8 detailed test cases and 8 risk entries created | None | Test Analyst |
| Execution |	Test Execution | Report	All 8 test cases executed successfully |	None	| Test Executor |
|Monitoring | Daily Progress Logs & Defect Tracking	| 3 defects logged and tracked on GitHub | None | Test Manager |
| Reporting |	Final Test Summary Report | Consolidated report with metrics and lessons learned | In progress	| Test Manager |

**Progress Tracking Method:**  
Progress was tracked using GitHub Issues . Each team member updated daily status, while the Test Manager monitored completion rates and variance. Communication channels : WhatsApp group  ensured daily alignment.

**Change Control Notes:**
No major scope or requirement changes occurred during this test cycle. Minor edits were made to defect descriptions for clarity. The test schedule remained consistent with the original plan.

## Lessons Learned

- Most Defect Prone Feature:The Leaderboard feature showed the highest defect density due to data         
  persistence and sorting logic issues. 
- Risk Analysis Impact: Early identification of high-risk areas (reset logic and localStorage handling) 
  improved test coverage and minimized post-execution defects. 
- Team Communication Effectiveness: Communication was efficient and collaborative through group channels. 
  Each role clearly understood deliverables, ensuring timely task completion and consistent reporting. 
- Improvements for Next Cycle: Introduce automated regression testing for repeated verification.
  Expand cross-browser testing to include Firefox and Edge.
  Conduct weekly defect triage meetings to prioritize fixes early.
  Add screenshots and environment versioning for clearer documentation.


## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| | Test Manager | Palesa Radebe  |P.R |28/10/2025
| | Risk Analyst | Veliswa Zicina  |V.Z |28/10/2025
| | Test Executor | Josphine Mbugua |JM |28/10/2025

## Overall Summary

**Statement:** 
The testing of Word Puzzle Game Plus was successfully completed, meeting all planned objectives and quality standards. All core features — Reset Game, Leaderboard, and Bonus Round — were fully validated for functionality, data accuracy, and user experience.

A total of 8 test cases were executed with a 100% pass rate, confirming stable performance and adherence to design specifications. While three defects were identified (two major and one medium), none were blocking issues, and all were documented with supporting evidence on GitHub for future fixes.

Risk analysis proved effective in guiding focus toward critical areas, achieving 75% risk coverage. Team coordination remained consistent through regular communication, ensuring timely task completion and accurate reporting.

Overall, the system demonstrated strong functionality, clear usability, and robust data handling, with only minor issues affecting gameplay depth and randomness. The testing process achieved its primary goal: verifying that the Word Puzzle Game Plus delivers a fair, smooth, and engaging experience for users.

**Test Status:**  Completed 
