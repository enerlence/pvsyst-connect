# Example prompts

Once the connector is on, talk to the assistant as you would to a colleague
who has PVsyst open. Replace the project names with yours.

## Explore

> List my PVsyst projects and tell me which ones already have simulation results.

> Summarise the system of project "Warehouse", variant VC0: modules, inverters,
> peak power, orientation and the main losses.

> Audit the parameters of variant VC1 of "Warehouse" and point out anything
> unusual (soiling, mismatch, thermal factor, albedo).

## Simulate

> How many PVsyst license runs do I have left?

> Run the simulation of variant VC0 of "Warehouse" and show me the monthly
> production and the loss diagram.

> Compare tilts of 15°, 20°, 25° and 30° for "Warehouse" in a single batch and
> tell me which one gives the highest specific yield.

> I want to see this same system in Geneva and in Madrid. Create both sites
> and simulate with synthetic weather.

## Report

> Prepare a results report of "Warehouse" VC0 with charts and give me the
> PDF download link.

> Give me the hourly results of the last simulation as CSV.

## PV*SOL (read only)

> List my PV*SOL projects and show me the self-consumption, grid feed-in and
> solar coverage of "House Smith".

> Show me the loss cascade of my PV*SOL project "House Smith", from
> horizontal irradiation to delivered energy.

## Good to know

- A batch of simulations costs a single license run, however many cases it
  contains; the assistant uses it for comparisons.
- Workflows such as "optimise the orientation", "compare two variants" or
  "evaluate several locations" come built in: ask *"What workflows do you
  have for PVsyst?"*.
- If a request is blocked by your permissions, the assistant will say so. Only
  you can change them, in Suntropy Connect.
