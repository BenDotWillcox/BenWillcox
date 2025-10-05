---
title: "Valorant Map Elo Dashboard"
excerpt: "
I developed a custom Elo rating system for the professional Valorant league VCT, adapting the traditional chess Elo system to account for Valorant's unique aspects, such as different maps, available margin of victory information, and no possibility of draws. This system separates each team's Elo rating by map and incorporates factors like win margins and skill variance. Through A/B testing, I refined the model for accurate match predictions. The result is a dynamic Streamlit dashboard showcasing live leaderboards, Elo changes, and an interactive match prediction tool.<br/>"
collection: portfolio
---

<div style="text-align: center;">
  <img src="https://bendotwillcox.github.io/BenWillcox//images/valorant_app.PNG" alt="valorant_app" style="width: 800px;"><br>
</div>

[Check the live dashboard out here](https://www.valomapped.com/)

Valorant ELO Dashboard
A comprehensive analytics platform for competitive Valorant esports data
Built a full-stack web application that tracks and analyzes professional Valorant tournament data, featuring sophisticated ELO rating calculations, team performance metrics, and predictive match simulations. The platform processes data from 30+ major tournaments including VCT Champions, Masters, and regional competitions.
Key Features:
Advanced ELO Algorithm: Custom mathematical model that calculates team ratings using:
Logarithmic margin-of-victory scaling: marginFactor = scale × ln(5.95 × √(scoreDiff + 1))
Expected probability calculation: P = 1 / (1 + 10^((loserRating - winnerRating) / 1000))
Dynamic K-factor adjustments based on team form and class
Map-specific ELO tracking for nuanced performance analysis
Interactive Analytics: Live charts showing team performance trends, map statistics, and player ratings over time
Match Predictions: AI-powered simulations for upcoming matches using historical data and ELO ratings
Tournament Bracket Visualization: Dynamic bracket displays with real-time updates and probability calculations
Comprehensive Data Pipeline: Automated web scraping from VLR.gg, data processing, and database management
Technical Stack:
Frontend: Next.js 14, TypeScript, Tailwind CSS, Recharts
Backend: Node.js, Drizzle ORM, PostgreSQL
Data Processing: Custom ELO calculator, web scraping with Puppeteer
Deployment: Vercel with automated CI/CD
Mathematical Highlights:
30+ tournaments tracked across 3+ years of competitive play
Map-specific ELO calculations with configurable parameters
Margin-of-victory scaling using logarithmic functions
Real-time rating updates with sophisticated probability modeling
This project demonstrates expertise in full-stack development, mathematical modeling, and creating user-friendly interfaces for complex statistical analysis.
Shorter version:
Valorant ELO Dashboard
A full-stack analytics platform featuring advanced ELO calculations with logarithmic margin-of-victory scaling and map-specific rating systems. Built with Next.js, TypeScript, and PostgreSQL, processing 30+ tournaments to provide insights for esports analysts and fans.
Mathematical highlights: Custom ELO algorithm with P = 1/(1 + 10^((R₂-R₁)/1000)) probability calculations and marginFactor = scale × ln(5.95 × √(scoreDiff + 1)) victory margin scaling.
