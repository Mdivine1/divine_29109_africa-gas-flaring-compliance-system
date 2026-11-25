
# divine_29109_africa-gas-flaring-compliance-system
Oracle PL/SQL system for monitoring gas flaring and detecting non-compliant operators in Africa.
Africa Gas Flaring Compliance System

Student Name: Divine Mahoro
Student ID: 29109

An Oracle PL/SQL database that compares satellite and operator-reported gas flaring volumes in Africa, estimates CO2 emissions and lost revenue, and flags non-compliant operators.

Problem Statement

Routine gas flaring at oil fields wastes energy and releases carbon dioxide. Nigeria, Algeria and Libya are among the nine countries that account for most of the world's flaring (World Bank, n.d.). Flare volumes are estimated from satellite observations, while operators report their own figures, and the two often differ. Regulators therefore find it hard to verify real flaring, quantify the emissions and lost revenue, and detect operators that breach flaring rules.

Proposed Solution

A centralized Oracle database that stores countries, oil fields, flare sites, operators, yearly flare volumes from satellite and operator sources, permits and violations. PL/SQL code will reconcile the two volume sources, convert flared gas into emissions and lost revenue, and flag non-compliant operators, so that regulators can act on evidence instead of manual comparison.

Objectives
Design a normalized Oracle schema for flare sites, operators, volumes, permits and violations.
Load real World Bank flaring data for African countries into the database.
Reconcile satellite and operator-reported volumes and flag large gaps.
Calculate CO2 emissions and lost revenue from flared gas volumes.
Detect permit breaches and record graded penalties automatically.
Provide summary reports by country, field and operator.
Data Source

Site-level flare volumes and country indicators come from the World Bank's Global Flaring and Methane Reduction Partnership:

Global Gas Flaring Data: https://www.worldbank.org/en/programs/gasflaringreduction/global-flaring-data

The data is filtered to African countries and loaded with SQL Developer or SQL*Loader. Operator-reported volumes, permits, gas prices and penalties are not published at site level, so they are simulated and labelled as such.

Innovation

A PL/SQL engine that automatically compares satellite and operator-reported flare volumes, calculates CO2 emissions and lost revenue, and flags non-compliant operators with graded penalties.

Planned Tables

COUNTRY, OIL_FIELD, OPERATOR, FLARE_SITE, SATELLITE_VOLUME, REPORTED_VOLUME, EMISSION_FACTOR, GAS_PRICE, FLARING_PERMIT, PENALTY_RULE, VIOLATION and AUDIT_LOG.

Primary and foreign keys, check constraints and indexes keep the data consistent.

Planned PL/SQL Features
Packages and procedures: data loading and cleaning, volume reconciliation and violation processing.
Functions: CO2 emissions, lost revenue and compliance-score calculations.
Triggers: permit validation, violation creation and audit logging of changes.
Cursors, exception handling and analytic functions: batch processing, error control and trend detection with LAG and RANK.
Materialized views: summaries of flaring and violations by country, field and operator.
Keywords

Gas Flaring, Emissions Compliance, Energy Waste Monitoring

References

World Bank. (n.d.). Global gas flaring data. Global Flaring and Methane Reduction Partnership. https://www.worldbank.org/en/programs/gasflaringreduction/global-flaring-data

World Bank. (2022). Global gas flaring volumes [Data set]. World Bank Data Catalog. https://datacatalog.worldbank.org/search/dataset/0037743

World Bank. (2025). 2025 global gas flaring tracker report. https://www.worldbank.org/en/programs/gasflaringreduction/publication/2025-global-gas-flaring-tracker-report
