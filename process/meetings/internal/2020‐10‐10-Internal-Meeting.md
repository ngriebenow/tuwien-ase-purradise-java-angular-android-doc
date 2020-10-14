| Issue| #2 |
| ------ | ------ |
| Date | 2020-10-10 |
| Start | 16:00 |
| End | 18:30 |
| Attendees | G, L, M, N, S, T |

## Goals
- ex-post discussion of Individual Assignment
- decision of project idea
- decision of team roles
- date for first tutor meeting, date for weekly tutor meetings

# Internal Meeting

## Project idea
We decided to go for an animal sanctuary.

Entities for CRUD: animal, customer, keeper, administrator
user roles: keeper, administrators, customer

## Features

- The customer wants to adopt an animal. They can specify their preferences (animal type, ...). Animals have preferences too (garden, running). The systems gives recommendations.

- The customer wants to browse different animals that are available for going for a walk. Some animals (dogs, but other animals work as well) need to go for a walk (either customers (or keepers) do that), some animals need daily care, special case if animal is sick.

- The customer can have animal sponsorship (Tierpatenschaft)

## Optional Features
- The keeper wants to know which animals need vaccines or need to go to the vet

- The animal shelter system should give people who already have animals the possibility to register their own animals. If they are unable to go for a walk with them (due to sickness, travel, etc.), then other customers can take care of them for one or a few days.


## Advanced feature
Best Matching, Scheduling (Nurse Rostering Problem)

## Technology
- Architecture style: web application, 3-Tier architecture
- Technologies: Spring Boot, H2 (testing environment, developing environment), Angular (Typescript), Bootstrap
- Persistence: relational database (SQL)

## Roles and Responsibilities
Team Coordination: Nicolas
Test Manager: Günter
Technical Architect: Michael
Quality Assurance/Code Style Guides (Checkstyle, EsLint): Thomas
Continuous Integration: Michael
UI/UX/Corporate Design: Lisa
Security: Stefan
Risk Manager: Nicolas
Documentation: Stefan

## Meetings
first tutor meeting: monday 11:00-13:00, preferably 11:00 
weekly meeting: 09:00 thursdays

## Open questions
- How shall we document the project? gitlab wiki, markdown in SCM,
Answer: Gitlab Wiki



