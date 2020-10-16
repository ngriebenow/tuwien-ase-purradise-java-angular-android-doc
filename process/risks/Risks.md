
| Issue |  #15 |
| ----- | --- |
| author       | Nicolas Griebenow |
| released by  | |
| release date | 2020-MM-DD |

# Risks
We categorize risks in two different dimensions:
- Severity on a scale from 1 to 10
- Probability on a scale from 1 (10%) to 10 (100%)
We define risk as the product of severeness times the probability.

![image](uploads/62db0937303466abdd6baade69b57537/image.png)
[Risk_Evaluation.xlsx](uploads/790bec86e2770f9b0a49be8c3248f392/Risk_Evaluation.xlsx)

# Detailed Analysis

## R1: Software ill defined
| Risk Score | 21 |
| ----- | --- |
| Severity | 3 |
| Probability | 7 |

The artefacts that we create could be ill defined, meaning they can have bugs (faults). The software does not behave in the way we want it to. It is very likely that there will be bugs in our software, however they should not ultimately lead to the failure of the project.

**Countermeasures:**
- An extensive test suite (Unit tests, Integration Tests, System Tests, E2E Tests)
- Quality Assurance measures (Code style guides)
- Code Reviews for criticial code parts
- Pair Programming for critical code parts

## R2: Inaccurate Time Estimations
| Risk Score | 48 |
| ----- | --- |
| Severity | 6 |
| Probability | 8 |

Although estimations are often unavoidable in software development, they can create risk if the estimations create expectations that can't be met. Inaccurate estimations occur when the length of a project, milestone or iteration is underestimated by the project group. Ultimately, they can lead to delay or project failure.

**Countermeasures:**
- Constant monitoring of the deviation between time estimated and time spent
- Prioritize issues
- Add a time buffer before deliverables (MR1, MR2, MR3)
- Plan with more work than it is planned (e.g. plan for a workload of 120%)

## R3: Requirements ill defined
| Risk Score | 20 |
| ----- | --- |
| Severity | 4 |
| Probability | 5 |

Requirements could be specified poorly or contradict themselves, which may lead to different perceptions and misunderstandings.

**Countermeasures:**
- Collect requirements as User Story Cards to clearly identify them


## R4: Lack of knowledge
| Risk Score | 24 |
| ----- | --- |
| Severity | 3 |
| Probability | 8 |

It could be the case that we do not have sufficient knowledge about the different technologies we use. Hence, learning these new technologies might take some time that leads to delay of the deliverables. Additionally, with insufficient knowledge about the technology we might use features in a more complicated way than it is intended to be.

**Countermeasures:**
- Plan time for tutorials of new technologies
- Throw away number one pattern (have a prototype, at least for the advanced feature)

## R5: Architecture & Design misplanning
| Risk Score | 25 |
| ----- | --- |
| Severity | 5 |
| Probability | 5 |

Architecture and Design might be badly conceptualized such that we are required to refactor it multiple times.

**Countermeasures:**
- 4-Eyes Principle and Review of all documents including Architecture and Design

## R6: Team conflicts
| Risk Score | 18 |
| ----- | --- |
| Severity | 6 |
| Probability | 3 |

Although we know each other quite well and we have successfully completed SEPM, it might be the case that conflicts between two people or one person and the team occur.

**Countermeasures:**
- Open communications (Discord channel)
- Team event (Escape Room, Volunteering, less suited due to competing charachter: Paintball, Mario-Kart, Go-Kart)

## R7: Work Organization due to COVID-19 pandemics
| Risk Score | 12 |
| ----- | --- |
| Severity | 2 |
| Probability | 6 |

Due to the current COVID-19 pandemics, it might be the case that there is a second lockdown that harms our way of work. E.g. university could be shut down such that the project and deliverable dates need to be postponed.

**Countermeasures:**
- None, we cannot mitigate this risk because we have no impact on the way how the university is organized in a second lockdown period and how the Austrian government will deal with restrictions on public institutions such as the TU Wien.

## R8: Illness of a team member
| Risk Score | 24 |
| ----- | --- |
| Severity | 4 |
| Probability | 6 |

In winter, the immune system is weaker than in summer, leading to catching a cold or getting the flu. Additionally, due to the current COVID-19 situation a team member might get infected as well. This harms our project because the affected team member might not be able to do a task assigned to them.

**Countermeasures:**
- Prefer virtual over presence meetings and communications to mitigate the risk of infection within the group.
- Have an At-Least-2 principle, meaning that if there is a new technology, then at least two team members should work on that.

## R9: Temporal unavailability (1-3 weeks) except for illness of a team member
| Risk Score | 12 |
| ----- | --- |
| Severity | 4 |
| Probability | 3 |

It might be the case that due to personal or familar circumstances, a team member is unavailable for a short period of time (up to three weeks).

**Countermeasures:**
- Have a time buffer in place
- Communicate potential unavailabilites as soon as they occur

## R10: Permanent unavailability (>4 weeks) of a team member
| Risk Score | 7 |
| ----- | --- |
| Severity | 7 |
| Probability | 1 |

It might be the case that a team member passes away or have a serious illness (cancer, ... ) that is related to a longer hospital stay.

**Countermeasures:**
- Have permanent meetings with all team members to ensure that all members are in good shape and health.
- Communicate potential unavailabilites as soon as they occur

## R11: Lack of ownership
| Risk Score | 16 |
| ----- | --- |
| Severity | 4 |
| Probability | 4 |

Ownership is important to ensure there is always someone in the team who takes responsibility for a specific topic and not just the whole team. They are also accounted for failure or success.

**Countermeasures:**
- Set responsibilites (have roles not only for team coordination, technical architect and testing manager, but also for UI/UX experience, Quality Assurance, Continuous Integration, Risk Management and Documentation)

## R12: Poor Code Quality
| Risk Score | 35 |
| ----- | --- |
| Severity | 7 |
| Probability | 5 |

Poor Code Quality leads to error injections, bugs and documentation inconsistencies that all delay the project or harm project success.

**Countermeasures:**
- Have static code analysis tools in place (Checkstyle, ESLint)
- Merge requests for 4-Eyes Principle
- Proper documentation of our Git workflow
- Code Reviews, Pair Programming

## R13: Poor Productivity
| Risk Score | 30 |
| ----- | --- |
| Severity | 6 |
| Probability | 5 |

Analysis Paralysis and Death by Planning might lead to poor productivity such as that time is mostly spent for internal meetings or revising documents without actually improving or extending the software.

**Countermeasures:**
- Agile iterative methodology (Scrum), including Scrum Poker for time estimations
- Use reporting tools such as Burn Down Charts to document the progress of the project

## R14: Advanced Feature
| Risk Score | 49 |
| ----- | --- |
| Severity | 7 |
| Probability | 7 |

The Advanced Feature is the core functionality and most important feature of ASE. Hence, it must be outstanding and should use advanced technologies. Since we agreed on Augmented Reality as our advanced feature using the Android ARCore library, there exists a multiple range of risks:
- We have no experience with the framework and the API and hence cannot estimate the time needed to deep dive into it.
- We have little to no experience in Visual 3D computing and OpenGL (shaders, etc.). Only two members have very little prior knowledge.
- We do not know whether our desired features can be satisfied with using this framework.

**Countermeasures:**
- Have someone who tests the ARCore framework by using a sample application and building a prototype (Throw away version one pattern)

## R15: Technical breakdown
| Risk Score | 12 |
| ----- | --- |
| Severity | 3 |
| Probability | 4 |

It might be the case that our inventory (notebooks, CI server) breaks down.

**Countermeasures:**
- Make all deliverables self-contained
- Commit early, commit often
- Have a personal backup strategy for personal/not yet published documents that are not pushed to our code and wiki repository

