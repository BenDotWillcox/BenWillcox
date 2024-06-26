---
title: "Valorant Map Elo Dashboard"
excerpt: "
I developed a custom Elo rating system for the professional Valorant league VCT, adapting the traditional chess Elo system to account for Valorant's unique aspects, such as different maps, available margin of victory information, and no possibility of draws. This system separates each team's Elo rating by map and incorporates factors like win margins and skill variance. Through A/B testing, I refined the model for accurate match predictions. The result is a dynamic Streamlit dashboard showcasing live leaderboards, Elo changes, and an interactive match prediction tool.<br/>"
collection: portfolio
---

<div style="text-align: center;">
  <img src="https://bendotwillcox.github.io/BenWillcox//images/valorant_app.PNG" alt="valorant_app" style="width: 800px;"><br>
</div>

[Check the live dashboard out here](https://valorant-map-dashboard-489cd7b1350b.herokuapp.com/)

I created a custom Elo rating metric for the professional Valorant league VCT. Inspired by the chess Elo system I wanI created a custom Elo rating metric for the professional Valorant league VCT. Inspired by the chess Elo system I wanted to capture team strength using a similar method but with the specific considerations for the nature of a valorant match. The first interesting deviation from chess is that Valorant is played on a number of different maps (7 rotating maps selected from a pool of 9 total maps). Each team plays very uniquely on each map causing teams to be strong on a given map while weak on another. This inspired me to separate each team's Elo rating by the map that they are playing. That way we can make interesting observations about the likelihood of team X beating team Y depending on the maps to be played in their match. The second interesting difference is inside the Elo calculation itself. There are key differences that force us to alter the generic chess Elo formula. These include the availability of a win margin which gives us extra information to infer a teams skill level, higher degree of variance in skill level for a team in any given match, and the fact that you can not draw in a professional valorant match. All of these differences impacted the variables that make up the final elo calculation. With these considerations in mind I picked initial variables I thought were relevant and A/B tested various tweaks to these variables until they accurately predicted match outcomes. The culmination of developing a proper elo rating metric was devising a dynamic Streamlit dashboard to display a variety of visualizations of these ratings including live leaderboards, elo changes over time, and an interactive match prediction tool.
