+++
title = 'Software Engineer - Data Platform'
description = "Modernizing academic data infrastructure and research analytics"
featured_image = "/images/Hoosiers wallpaper.png"
date = 2023-01-01T00:00:00-00:00
draft = false
+++

### Indiana University, Bloomington, IN | January 2023 – May 2024

My role as a Software Engineer on the Data Platform team at Indiana University was where I first learned to build production-grade data systems that actually matter to people's daily work. Working in an academic environment meant dealing with incredibly diverse data sources—from student information systems to research datasets—while maintaining the security and compliance standards of a major university.

**Building Academic Data Infrastructure**

The technical challenge was fascinating: how do you create a unified data platform that serves both administrative needs and research requirements? We built automated pipelines using Airflow hosted on EC2, pulling data from dozens of campus systems into Redshift. The scale was significant—over 1TB of multi-source data flowing through our systems weekly, but the real complexity came from the variety of data formats and the need for rock-solid reliability.

I spent a lot of time designing ETL workflows that could handle everything from clean CSV exports to messy XML feeds from legacy academic systems. Using Docker for containerization and implementing proper CI/CD with Jenkins and GitLab, we created a deployment process that let us push updates confidently without breaking research workflows that professors depended on.

**Learning Data Modeling at Scale**

One of my biggest learning experiences was redesigning our Redshift data models to serve diverse use cases efficiently. Academic data is tricky—you need to support everything from enrollment reporting to longitudinal research studies. I implemented star schema designs with slowly changing dimension logic that unified campus data while preserving the historical context that researchers need.

The performance improvements were dramatic—dashboard query times dropped by 50%, but more importantly, we enabled researchers to ask questions they couldn't before. When a professor can run a complex enrollment trend analysis in seconds instead of hours, it changes how they approach their research.

**Security and Access Control**

Working with student data meant learning about FERPA compliance and implementing robust access controls. Using AWS IAM and CloudWatch, I built a system where researchers could access anonymized datasets while administrators maintained full visibility into sensitive information. The challenge was creating role-based access that was secure but not cumbersome for day-to-day work.

**Real Impact on Campus Operations**

What made this role rewarding was seeing how better data infrastructure improved actual university operations. Admissions officers could track application trends in real-time, student services could identify at-risk students earlier, and researchers could focus on analysis instead of data wrangling.

The technical stack was modern but had to integrate with decades-old campus systems. Working with legacy data taught me patience and the importance of robust error handling—when your source system was built in the 1990s, you learn to expect the unexpected.

This experience taught me that good data engineering isn't just about the latest technologies—it's about understanding your users' workflows and building systems that make their work easier and more effective.