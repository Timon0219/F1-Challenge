# Formula 1 Racing Challenge: 2024 Strategy Analysis 

This repository contains all the code for the armchair strategist [dashboard](https://joiner-for.vercel.app) as well as engineered data for F1 races from the 2018 season onwards.

The dashboard and visualizations in this README are updated every Monday at midnight to reflect the latest race.

## Visualizations of the Most Recent Race

<details>
    <summary>
        <b>Pit Stop Strategies</b>
    </summary>
    <img src="Docs/visuals/strategy.png", alt="strategy">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>strategy_barplot(season, event)</code>
    </details>
</details>

<details>
    <summary>
        <b>Position Changes</b>
    </summary>
    <img src="Docs/visuals/position.png" alt="position">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>driver_stats_scatterplot(season, event, drivers=10)</code>
    </details>
</details>

<details>
    <summary>
        <b>Point Finishers Race Pace</b>
    </summary>
    <img src="Docs/visuals/laptime.png" alt="laptime">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>strategy_barplot(season, event)</code>
    </details>
</details>

<details>
    <summary>
        <b>Podium Finishers Gap to Winner</b>
    </summary>
    <img src="Docs/visuals/podium_gap.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        See <code>f1_visualization/readme_machine.py</code>
    </details>
</details>

<details>
    <summary>
        <b>Teammate Pace Comparisons</b>
    </summary>
    Boxplot visualization:
    <img src="Docs/visuals/teammate_box.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>driver_stats_distplot(season, event, violin=False, swarm=False, teammate_comp=True, drivers=20)</code>
    </details>
    Violinplot with all laptimes:
    <img src="Docs/visuals/teammate_violin.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>driver_stats_distplot(season, event, violin=False, swarm=False, teammate_comp=True, drivers=20)</code>
    </details>
</details>

<details>
    <summary>
        <b>Team Pace Comparisons</b>
    </summary>
    <img src="Docs/visuals/team_pace.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        See <code>f1_visualization/readme_machine.py</code>
    </details>
</details>

## Build
Build with `pip install -e .` Using a Python virtual environment is highly recommended.

Run dashboard locally with `python3 app.py`. Debug mode can be enabled by setting `app.run(debug=True)` in `app.py`.

## Contributing
You should install pre-commit hooks with `pre-commit install`.

## Data Source

All data sourced from the [FastF1](https://github.com/theOehrly/Fast-F1) package.

## Data Availability

Data from all grand prixs and sprint races beginning in the 2018 season, excluding test sessions, are available. This repository will be automatically updated during the F1 season.

## Metrics Definitions

See `SCHEMA.md` for details on the columns provided in `Data/all_laps_*.csv` and `Data/transformed_laps_*.csv` files.

## Additional Examples
<details>
    <summary>
        <b>Tyre Degradation Lineplot</b>
    </summary>
    <img src="Docs/examples/tyre_line.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>compounds_lineplot(seasons, events)</code>
    </details>
</details>

<details>
    <summary>
        <b>Tyre Degradation Distribution Plot</b>
    </summary>
    <img src="Docs/examples/tyre_dist.png">
    <details>
        <summary>
            <b>Function call:</b>
        </summary>
        <code>compounds_distplot(seasons, events)</code>
    </details>
</details>
