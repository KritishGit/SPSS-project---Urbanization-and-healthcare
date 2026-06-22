# Urbanization & Health Outcomes

A hierarchical regression project I built to test something that gets assumed a lot in development economics: that urbanization improves health outcomes. Turns out it's more complicated than that.

## What this is about

The common story goes: cities have better hospitals, sanitation, and infrastructure, so more urbanized countries should have better health outcomes. I wanted to actually test that instead of taking it at face value - specifically, does urbanization still predict health outcomes once you control for how rich a country is (GDP)?

I used hierarchical regression in SPSS, entering GDP first and urbanization second, so I could see what urbanization adds on its own, after wealth is already accounted for.

## What I found

- Once GDP is in the model, **urbanization stops being a significant predictor** of health outcomes. Most of what looked like an "urbanization effect" was really just a wealth effect in disguise.
- The bigger surprise was the **Gini coefficient** (a measure of income inequality) - it stayed significant even after controlling for GDP and urbanization, predicting both life expectancy and infant mortality. So how evenly a country's income is spread out seems to matter more than how urbanized it is.

That second finding wasn't what I expected going in, which is honestly why I think it's the more interesting part of this project.

## How it's built

- **Design**: Hierarchical (sequential) multiple regression
- **Sample**: 177 countries
- **Predictors**: GDP per capita (step 1), urbanization rate (step 2), Gini coefficient
- **Outcomes**: Life expectancy, infant mortality rate
- **Tool**: SPSS

## What's in this repo

| File                   | What it is                                           |
| ---------------------- | ---------------------------------------------------- |
| SPSS_Master_Dataset    | Cleaned dataset, compiled from World Bank indicators |
| ---                    | ---                                                  |
| SPSS Project Propossal | The original research proposal                       |
| SPSS project.sav       | SPSS syntax file with the regression code            |
| Outputs                | Folder with all SPSS output and regression results   |

## Where the data's from

All variables come from World Bank country-level data - GDP per capita, urbanization rate, Gini coefficient, life expectancy, and infant mortality rate.

## Author

Kritish Sardar - B.Sc. Statistics (Honours), University of Delhi
