# Paper Link

https://arxiv.org/pdf/2506.09254v2

# 📄 Paper Overview

**"Machine learning-based correlation analysis of decadal cyclone intensity with sea surface temperature: data and tutorial"** — Jingyang Wu & Rohitash Chandra (UNSW Sydney), arXiv 2506.09254, June 2025.

**One-liner:** The authors built an open dataset linking 40+ years of tropical cyclone records to sea surface temperature (SST), and used simple ML models to show that warmer SST correlates with stronger cyclones — especially Category 5 storms in the Indian Ocean basins.

---

## 🗣️ Suggested 5-minute talk structure

**1. Motivation (~1 min)**
- Tropical cyclones cause massive damage (~13,000 deaths/year on average historically); destructive power roughly quadruples per Saffir-Simpson category.
- Global warming raises SST, a key energy source for cyclones — but the link between SST and cyclone *genesis and intensity* isn't well quantified.
- Gap: no comprehensive, open dataset combining cyclone tracks and SST to study this relationship.

**2. What they built (~1.5 min)**
- A **Cyclone-SST dataset** merging two sources:
  - **JTWC** (US Navy) "best-track" cyclone records (position, wind speed every 6 hours) since 1981.
  - **NOAA OI-SST** daily satellite-based sea surface temperatures (0.25° grid).
- Covers **2,030 cyclones in 4 basins**: South Indian (670), North Indian (564), Northwest Pacific (405), South Pacific (391).
- For each cyclone: location, time, season, Saffir-Simpson category (1–5), wind speed, and **SST for 15 days before and after genesis**. All open-source (GitHub + Zenodo), with a full tutorial to reproduce everything.

**3. Key findings (~1.5 min)**
- **SST rises before a cyclone forms, then drops sharply after** (ocean mixing by the storm) — cooling typically bottoms out 3–7 days post-event, modeled with Generalized Additive Models. Strongest in the Southern Hemisphere basins.
- **Positive correlation between SST and cyclone intensity in all basins** (linear regression + Support Vector Regression):
  - Strongest signal for **Category 5 cyclones in the South Indian and North Indian Oceans** — Cat 5 storms occur almost exclusively above **28°C SST**.
  - Threshold-like behavior: below ~25–26°C, intensification is rare.
  - SVR captures nonlinearities at temperature extremes that linear regression misses.
- Decadal trends: proportion of high-intensity cyclones increased in the 1990s and 2010s.

**4. Limitations & future work (~30 sec)**
- Few cyclone features; 6-hour recording interval may miss rapid changes.
- Future: real-time automated data pipelines, finer (hourly) resolution, more SST sources for uncertainty quantification.

**5. Take-home message (~15 sec)**
> Warmer seas mean stronger cyclones — this open dataset and code give researchers a reproducible foundation for studying and forecasting cyclone intensity in a warming world.
