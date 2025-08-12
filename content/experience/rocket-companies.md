+++
title = 'Data Engineer - Rocket Companies'
description = "Building event-driven data architecture and automated testing frameworks"
featured_image = "/images/rocket-new-fb.png"
date = 2024-07-01T00:00:00-00:00
draft = false
+++

### Los Angeles, CA | July 2024 – August 2025

Working at Rocket Companies in the Core Digital Media team has been a deep dive into building robust, event-driven data infrastructure that powers real-time decision making for a fintech giant. The scale and complexity here taught me that elegant data engineering isn't just about moving data—it's about creating systems that business teams can trust and rely on.

**Event Streaming Architecture That Actually Works**

One of the most challenging projects I tackled was designing an end-to-end event streaming pipeline that captures user interactions from QuickenLoans and RocketMortgage properties. The technical challenge was fascinating: how do you reliably stream campaign events, form submissions, and user behavior data through AWS Kinesis while maintaining data integrity and handling schema evolution?

We built this sophisticated flow where browser events hit our shared-BFF service, get validated through API Gateway with attached schemas, then flow through Lambda functions that validate the data payload against versioned schemas stored in S3. The beauty of this system is that new event types can be added without any backend pipeline changes—it's completely config-driven. Events flow from Kinesis to Firehose and land in Snowflake, with failed events automatically backed up to S3 for investigation.

The real engineering challenge was handling event versioning and idempotency. Every event carries version metadata and an idempotency ID, so downstream consumers (like our BI teams) can handle duplicates appropriately. This design philosophy of "duplicates are events too" was a mindset shift that made our data more trustworthy.

**Building Internal Tools That Scale**

What really made our team productive were the in-house libraries we developed. I worked extensively with "Piggy" for flattening complex JSON structures, "ETL Verify" for automated source-to-target validation, and "DB Launcher" for standardized Snowflake connections across all our Airflow DAGs. But the crown jewel was "Eagle Eye"—our alerting framework that monitors everything from CDC data consistency to Power BI SLA breaches, sending intelligent notifications via email and PagerDuty.

The most impactful work was probably the "Sentinel" automated regression testing framework I helped develop. When you're deploying to production weekly with critical financial data flowing through your pipelines, you need bulletproof testing. Sentinel runs three types of tests: SQL-based validation (think MINUS operations and count checks), process trigger tests that actually run DAGs with test data, and API reconciliation tests that compare our warehouse numbers against external APIs like Everflow.

**Solving Real Business Problems**

The daily reality involved more than just building pipelines—I was constantly troubleshooting production issues. Cost mismatches in our financial reporting, missing leads in final tables, Airflow DAG failures that blocked critical business reports. Each incident taught me something new about data lineage and the importance of observability.

One particularly satisfying project was redesigning how we consumed Google Analytics data in Power BI. The original approach was pulling raw data and calculating metrics at the user/session level in real-time, which was killing performance. I created pre-aggregated views that reduced data size significantly while maintaining the granularity business users needed. Sometimes the best engineering is just thinking differently about the problem.

**Database Migration and Modernization**

I also led a major database migration from Oracle to PostgreSQL using AWS DMS and SCT, which involved rethinking our entire data model for the new environment. This wasn't just a lift-and-shift—we optimized table structures, rewrote stored procedures as Snowflake functions, and implemented proper CDC patterns. The migration touched everything from our ETL processes to our Power BI semantic models.

Working with partners' APIs to automate data ingestion was another constant. Instead of manual file transfers, I built config-driven API integration workflows that could onboard new data sources in hours rather than days. The business impact was immediate—marketing teams could access fresh partner data within an hour instead of waiting for daily batch uploads.

**Technical Growth Through Real Problems**

This role deepened my understanding of how data engineering intersects with business operations. You're not just moving data; you're enabling revenue attribution, customer retention analysis, and marketing optimization. When a form submission fails to make it into our lead tables, that's potentially lost revenue. When our campaign attribution data is inconsistent, marketing can't optimize their spend.

The tech stack was modern and challenging—Airflow orchestrating everything, Snowflake as our analytical warehouse, Terraform for infrastructure as code, and a mix of AWS services for real-time and batch processing. But the real learning came from building systems that non-technical stakeholders could understand and trust.

Every production issue became a learning opportunity to build better monitoring, implement smarter error handling, or redesign workflows for resilience. The goal was always to make the system so reliable that business users could focus on insights rather than data quality questions.