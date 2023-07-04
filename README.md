# 2023_UNIST_BTS(Beyond The Society)_코빼기(CO2 빼기)

## About us

| 이름 | 구분 |
| ----- | ----- |
| 복영규 | 팀장 |
| 송유진 | 팀원 |
| 김영진 | 팀원 |
| 김보민 | 팀원 |
| Artem Kim | 팀원 |

## Problem Description

<div align=center>
  <img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/2240a322-6552-402c-a4f6-8d579774d8f0" alt="map" width="75%"/>
</div>

### Goal

- Establishing Pareto-optimal urban greening plans in Nam-gu, Ulsan that **maximize the number of covered heat vulnerable people** and **carbon sequestration**, and **minimize infrastructure installation costs**

### Assumption

- All possible sites belong to **type 0, 1, 2**, and each type refers to **empty site (original state)**, **site filled only with grass**, and **site filled with grass and trees**, respectively.
- Heat vulnerable people are covered **when there are type 2 site(s) within 1,000m**.

<div align=center>
  <img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/9e85a7fe-6d52-4bef-9475-4f3e3a152143" alt="table" width="60%"/>
</div>

### Notation

<img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/d06a994f-8831-4331-ad9f-2d2e473284d7" alt="sets" width="45%"/>

<img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/98284c09-c8f3-4ceb-851e-14c994605935" alt="parameters" width="55%"/>

<img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/13a5ab8e-cebc-4dfc-8a31-3b4b99e06af8" alt="decision variables"/>

### Mathematical Formulation

<div align=center>
  <img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/d9e7e405-0ba2-4b2c-b227-5f1d2adc0770" alt="mathematical formulation" width="75%"/>
</div>

The proposed model is an **integer programming (IP)** consisting with 3 objectives. **Objective (1)** maximizes the number of covered heat vulnerable people. **Objective (2)** maximizes carbon sequestration of sites. **Objective (3)**  minimizes the total infrastructure installation cost. **Constraint (4)** ensures that $x_i$ is covered if and only if there are type 2 site(s) within 1,000m. **Constraint (5)** ensures the possible site should be among type 0, 1, 2.

## Solution Approach

We are going to find optimal urban greening plans for Nam-gu, Ulsan using **NSGA-II**.

### Solution Representation

<div align=center>
  <img src="https://github.com/duckbankbok/2023_BTS_CO2-Subtraction/assets/64826387/32e6ae0e-1ddd-4661-9ca0-93f9f16a176d" alt="solution representation" width="40%"/>
</div>

- Each index of solution representation means index of possible site, and integer number means type of possible site.
