---
title: "Valorant Map Elo Dashboard"
excerpt: "
Valorant ELO Dashboard
A full-stack analytics platform featuring advanced ELO calculations, ML-based player ratings (VPM), and Monte Carlo tournament simulations. Built with Next.js, TypeScript, and PostgreSQL.
Technical highlights- Custom ELO with logarithmic margin scaling, 7-component EMA with Ridge regression for player ratings, 1D Kalman filtering for time-series smoothing, and 10,000+ iteration Monte Carlo simulations for tournament predictions.<br/>"
collection: portfolio
---

<div style="text-align: center;">
  <img src="https://bendotwillcox.github.io/BenWillcox//images/valorant_app.PNG" alt="valorant_app" style="width: 800px;"><br>
</div>

[Check the live dashboard out here](https://www.valomapped.com/)

# Valorant ELO Dashboard

A comprehensive analytics platform for competitive Valorant esports data

Built a full-stack web application that tracks and analyzes professional Valorant tournament data, featuring sophisticated ELO rating calculations, advanced player rating systems, and Monte Carlo tournament simulations. The platform processes data from 30+ major tournaments including VCT Champions, Masters, and regional competitions.

## Key Features:

**Custom ELO Algorithm**: Mathematical model that calculates team ratings using:

- Logarithmic margin-of-victory scaling: `marginFactor = scale × ln(5.95 × √(scoreDiff + 1))`
- Expected probability calculation: `P = 1 / (1 + 10^((loserRating - winnerRating) / 1000))`
- Map-specific ELO tracking for nuanced performance analysis

**VPM (Valorant Plus Minus) Player Rating System**: Advanced ML-based player evaluation using:

- 7-component EMA (Exponentially Weighted Moving Average) with component-specific decay rates
- Ridge regression model combining: `VPM = w₁×EMA_kpr + w₂×EMA_dpr + w₃×EMA_apr + w₄×EMA_fk_att_rate + w₅×EMA_fk_win_rate + w₆×EMA_adr + w₇×EMA_kast`
- 1D Kalman filtering for time-series smoothing and noise reduction
- L2 regularization to prevent overfitting and ensure generalization

**Monte Carlo Tournament Simulations**: Large-scale statistical modeling using:

- 10,000+ simulation runs per tournament prediction
- Probabilistic match simulation with map-specific ELO integration
- Round-by-round probability calculations for complex tournament formats
- Real-time probability updates as matches complete

**Interactive Analytics**: Live charts showing team performance trends, map statistics, and player ratings over time

**Automated Data Pipeline**: Web scraping from VLR.gg, data processing, and database management

## Technical Implementation:

- **Frontend**: Next.js 14, TypeScript, Tailwind CSS, Recharts
- **Backend**: Node.js, Drizzle ORM, PostgreSQL
- **Data Processing**: Custom ELO calculator, web scraping with Puppeteer
- **Deployment**: Vercel with automated CI/CD

## Mathematical Highlights:

- 30+ tournaments tracked across 3+ years of competitive play
- Map-specific ELO calculations with configurable parameters
- Advanced time-series modeling with Kalman filters and EMA components
- Ridge regression for player skill estimation with 7 statistical components
- Monte Carlo simulations with 10,000+ iterations for tournament predictions

This project demonstrates expertise in full-stack development, machine learning, mathematical modeling, and creating user-friendly interfaces for complex statistical analysis.
