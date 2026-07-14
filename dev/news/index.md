# Changelog

## ypr 0.6.0.9014

### Continuous integration

- Install binaries from r-universe for dev workflow
  ([\#119](https://github.com/poissonconsulting/ypr/issues/119)).

## ypr 0.6.0.9013

### Continuous integration

- Fix reviewdog and add commenting workflow
  ([\#117](https://github.com/poissonconsulting/ypr/issues/117)).

## ypr 0.6.0.9012

### Chore

- Auto-update from GitHub Actions
  ([\#112](https://github.com/poissonconsulting/ypr/issues/112)).

### Continuous integration

- Use workflows for fledge
  ([\#115](https://github.com/poissonconsulting/ypr/issues/115)).

- Sync ([\#114](https://github.com/poissonconsulting/ypr/issues/114)).

- Use reviewdog for external PRs
  ([\#113](https://github.com/poissonconsulting/ypr/issues/113)).

- Cleanup and fix macOS
  ([\#111](https://github.com/poissonconsulting/ypr/issues/111)).

- Format with air, check detritus, better handling of `extra-packages`
  ([\#110](https://github.com/poissonconsulting/ypr/issues/110)).

- Enhance permissions for workflow
  ([\#108](https://github.com/poissonconsulting/ypr/issues/108)).

- Permissions, better tests for missing suggests, lints
  ([\#107](https://github.com/poissonconsulting/ypr/issues/107)).

- Always use `_R_CHECK_FORCE_SUGGESTS_=false`
  ([\#106](https://github.com/poissonconsulting/ypr/issues/106)).

- Correct installation of xml2
  ([\#105](https://github.com/poissonconsulting/ypr/issues/105)).

- Sync ([\#104](https://github.com/poissonconsulting/ypr/issues/104)).

### Testing

- Skip if packages missing
  ([\#109](https://github.com/poissonconsulting/ypr/issues/109)).

## ypr 0.6.0.9011

- Merge branch ‘main’ of github.com:poissonconsulting/ypr.

- Have parameter description NA if documentation corrupted.

## ypr 0.6.0.9010

### fledge

- Bump version to 0.6.0.9009
  ([\#91](https://github.com/poissonconsulting/ypr/issues/91)).

## ypr 0.6.0.9009

### fledge

- Bump version to 0.6.0.9008
  ([\#89](https://github.com/poissonconsulting/ypr/issues/89)).

## ypr 0.6.0.9008

### fledge

- Bump version to 0.6.0.9007
  ([\#87](https://github.com/poissonconsulting/ypr/issues/87)).

## ypr 0.6.0.9007

### fledge

- Bump version to 0.6.0.9006
  ([\#86](https://github.com/poissonconsulting/ypr/issues/86)).

## ypr 0.6.0.9006

### fledge

- Bump version to 0.6.0.9005
  ([\#85](https://github.com/poissonconsulting/ypr/issues/85)).

## ypr 0.6.0.9005

### fledge

- Bump version to 0.6.0.9004
  ([\#84](https://github.com/poissonconsulting/ypr/issues/84)).

## ypr 0.6.0.9004

### fledge

- Bump version to 0.6.0.9003
  ([\#83](https://github.com/poissonconsulting/ypr/issues/83)).

## ypr 0.6.0.9003

### fledge

- Bump version to 0.6.0.9002
  ([\#81](https://github.com/poissonconsulting/ypr/issues/81)).

## ypr 0.6.0.9002

### fledge

- Bump version to 0.6.0.9001
  ([\#80](https://github.com/poissonconsulting/ypr/issues/80)).

## ypr 0.6.0.9001

### Continuous integration

- Fetch tags for fledge workflow to avoid unnecessary NEWS entries
  ([\#78](https://github.com/poissonconsulting/ypr/issues/78)).

- Use larger retry count for lock-threads workflow
  ([\#77](https://github.com/poissonconsulting/ypr/issues/77)).

- Overwrite from actions-sync
  ([\#76](https://github.com/poissonconsulting/ypr/issues/76)).

### Documentation

- Register poissontemplate usage ([@maelle](https://github.com/maelle),
  [\#71](https://github.com/poissonconsulting/ypr/issues/71)).

### Uncategorized

- Merge pull request
  [\#75](https://github.com/poissonconsulting/ypr/issues/75) from
  poissonconsulting/reqName.

  replaced [`requireNamespace()`](https://rdrr.io/r/base/ns-load.html)
  with
  [`rlang::check_installed()`](https://rlang.r-lib.org/reference/is_installed.html)

- Merge pull request
  [\#72](https://github.com/poissonconsulting/ypr/issues/72) from
  poissonconsulting/before.

## ypr 0.6.0.9000

- Same as previous version.

## ypr 0.6.0

CRAN release: 2022-08-29

- `Rk` is now the egg to tR survival if between 0 and 1.

## ypr 0.5.2

CRAN release: 2021-07-03

- Internal changes only.

## ypr 0.5.1

CRAN release: 2020-07-10

- House-keeping.

## ypr 0.5.0

CRAN release: 2020-03-18

- Pass yield parameters Ly, harvest and biomass to ypr_report().
- Removed suggests dependency on checkr.

## ypr 0.4.0

CRAN release: 2020-01-13

### Major Features

### Population Parameters

Replaced parameters

- `M` (annual instantaneous natural mortality rate)
- `Mb` (annual instantaneous natural mortality rate (as a function of
  length) scaling exponent)
- `A0` (initial post age tR density independent mortality probability)

with

- `n` (annual natural mortality rate from age tR to length Ln)
- `nL` (annual natural mortality rate from length Ln)
- `Ln` (length at which the natural mortality rate switches from n to
  nA)

And

- Added parameters `k2`, `Linf2` and `L2` to allow for biphasic growth.
- Set `Lp` value to be 1000 as opposed to Linf.
- Set `Ls` and `Lv` arguments to be 50 as opposed to `Linf/2`.
- Allow `L2`, `Ln`, `Ls` and `Lv` to also take ages (as negative
  values).

### Population(s)

- Added `expand = TRUE` argument to
  [`ypr_populations()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_populations.md)
  to allow control over all combinations.
- Added
  [`ypr_populations_expand()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_populations_expand.md)
  to create all combinations of parameters.
- Added `ypr_populations_update()` (as well as `update.ypr_population()`
  and `update.ypr_populations()`).
- `ypr_populations` no longer requires names.
- Added
  [`ypr_population_names()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_population_names.md)
  to allow user to generate names.
- Added
  [`as_ypr_populations.data.frame()`](https://poissonconsulting.github.io/ypr/dev/reference/as_ypr_population.md).
- Added `data.frame.ypr_population()` and
  `data.frame.ypr_populations()`.
- Added
  [`ypr_age_at_length()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_age_at_length.md)
  to get ages at specific lengths for a given population.
- Added
  [`ypr_length_at_age()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_length_at_age.md)
  to get lengths at specific ages for a given population.

### Population Reports

- Added `description = ""` argument to
  [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md)
  to allow user to describe report.
- [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md)
  now starts with table of parameter values with parameter descriptions.
- Added `view = FALSE` argument to
  [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md)
  to allow user to view report in browser.
- Added `ask = TRUE` argument to
  [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md)
  to ask before overwriting or creating a file.
- Deprecated requirement to provide file extension in
  [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md).
- Soft deprecated
  [`ypr_schedule()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_schedule.md)
  for
  [`ypr_tabulate_schedule()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_schedule.md).

### Plots

- Added plot of biomass and eggs to report.
- Added `percent = FALSE` argument to
  [`ypr_plot_fish()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_fish.md)

### Tables

- Added
  [`ypr_tabulate_biomass()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_biomass.md)
  to easily calculate total biomass and eggs.
- Renamed column `HandlingMortality` to `HandlingMortalities` in
  [`ypr_tabulate_fish()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_fish.md)
  and
  [`ypr_plot_fish()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_fish.md).
- Renamed column `Spawning` to `Spawners` in
  [`ypr_tabulate_fish()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_fish.md)
  and
  [`ypr_plot_fish()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_fish.md).

### Bug Fixes

- Improved handling of unsustainable populations (no longer negative
  fish numbers).

## ypr 0.3.1

CRAN release: 2019-04-26

- [`ypr_populations()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_populations.md)
  now generates names
- Fixed Quesnel Lake Trout and Rainbow Trout mix up

## ypr 0.3.0

CRAN release: 2018-11-26

- Now uses `q` instead of `Ea` and `Eb` for effort
- Parameter `Rk` now has to be greater than \>= 1

## ypr 0.2.0

- Added
  [`ypr_exploitation()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_exploitation.md)
  to convert capture probabilities to exploitation probabilities.
- Added
  [`ypr_report()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_report.md)
  to generate Rmd file for population.
- Can now pass Rk as egg to recruit survival (at low density).
- Set default value of `Wa` to be 0.01.
- Added
  [`ypr_populations()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_populations.md)
  to generate all combinations of parameters.
- Made
  [`ypr_tabulate_sr()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_sr.md),
  [`ypr_tabulate_yield()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_yield.md),
  [`ypr_tabulate_yields()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_yields.md),
  [`ypr_plot_yield()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_yield.md)
  generic with definitions for `ypr_population` and `ypr_populations`
  objects.
- Added scaling parameter `A0` for initial interval mortality of
  recruits.
- Added scaling parameters `Ea` and `Eb` to allow plots of yield per
  effort.
- Added `Age`, `Length`, `Weight` and `Effort` to
  [`ypr_tabulate_yield()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_yield.md)
  and added
  [`ypr_tabulate_yields()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_yields.md)
- Added `y` arg to
  [`ypr_plot_yield()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_yield.md)
  to allow plotting of mean age, length, weight, effort or yield per
  effort by exploitation or capture probability.
- Added `ypr_plot_histogram()` to plot frequency distributions of catch,
  spawners and in lake by age, length or weight bins.
- Added
  [`ypr_tabulate_parameters()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_parameters.md)
  to get table of parameters, values and descriptions and
  [`ypr_detabulate_parameters()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_detabulate_parameters.md)
  to convert back to a population object.
- Added
  [`ypr_tabulate_sr()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_tabulate_sr.md)
  to get table of eggs and recruits at unfished, actual and optimal
  rates.
- Added `print.ypr_population()`.

## ypr 0.1.0

- Added `Mb` to scale mortality by length and `BH` to distinguish
  between Beverton-Holt and Ricker curves and `es` for probability of a
  mature fish spawning and `Sm` for spawning mortality probability and
  `Sp` for spawning power and vulnerability power `Vp` and slot limit
  non-complicance parameter `Nc` and scaling parameter `R0`.
- Added
  [`ypr_population_update()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_population_update.md)
  to update population parameters.
- Added `ypr_yield_tabulate()` to tabulate actual and optimal yields.
- Added
  [`ypr_sr()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_sr.md)
  to get stock recruitment parameters and
  [`ypr_plot_sr()`](https://poissonconsulting.github.io/ypr/dev/reference/ypr_plot_sr.md)
  to plot.
- Added `ypr_inst2inter()` and `ypr_inter2instant()` to convert
  mortality rates.
- Switched `nu` for `M` and `R0` for `Rmax`.
- Switched yield parameters `harvest` and `biomass` to `FALSE` by
  default.
- Renamed `a` to `Wa` and `b` to `Wb` and `eta` to `Hm` and `mu` to `pi`
  and `Rt` to `tR`.
- Removed `Capture` (as covered by single value) and `TotalMortality`
  from schedule and added `Spawning`.

## ypr 0.0.1

- Initial Release
