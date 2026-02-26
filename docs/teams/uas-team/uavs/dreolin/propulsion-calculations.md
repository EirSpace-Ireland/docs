# Dreolin — Propulsion Calculations

Propulsion sizing summary derived from the eCalc propeller calculator output in `Batteries, Motors, ESCs.xlsx` for the EirSpace 1 configuration. Results cover two battery configurations for a twin-motor fixed-wing aircraft.

## Input assumptions

- Wingspan: 1340 mm
- Wing area: 30.418 dm^2
- Chord: 227 mm
- Reference mass input: 3000 g

## Power system configuration

- Battery: LiPo 10000 mAh (30/45C)
- ESC: max 40 A, 50 g
- Motor: T-Motor F90-1300 (1300 KV), 47 g
- Propeller: APC Electric E 7 x 4, 2 blades
- Wiring: AWG10 (5.27 mm^2) for battery and motor extensions

## Battery and flight time

| Metric | 4S1P | 4S2P |
| --- | --- | --- |
| Load (C) | 3.13 | 1.58 |
| Voltage (V) | 14.59 | 14.69 |
| Energy (Wh) | 148.0 | 296.0 |
| Total capacity (mAh) | 10000 | 20000 |
| Used capacity (mAh) | 8500 | 17000 |
| Min flight time (min) | 16.3 | 32.2 |
| Mixed flight time (min) | 24.5 | 39.7 |
| Battery weight (g) | 1004 | 2008 |

## Motor performance at maximum

| Metric | 4S1P | 4S2P |
| --- | --- | --- |
| Current (A) | 15.65 | 15.85 |
| Voltage (V) | 14.49 | 14.60 |
| RPM | 16551 | 16660 |
| Electric power (W) | 226.8 | 231.3 |
| Mechanical power (W) | 188.6 | 192.4 |
| Efficiency (%) | 83.2 | 83.2 |
| Estimated motor temp (C) | 50 | 51 |

## Propeller performance

| Metric | 4S1P | 4S2P |
| --- | --- | --- |
| Static thrust (g) | 1011 | 1025 |
| Thrust at 60 km/h (g) | 666 | 677 |
| Pitch speed (km/h) | 101 | 102 |
| Specific thrust (g/W) | 4.46 | 4.43 |

## Total drive metrics

| Metric | 4S1P | 4S2P |
| --- | --- | --- |
| Drive weight (g) | 1318 | 2422 |
| Power-weight (W/kg) | 207 | 145 |
| Thrust-weight (ratio) | 0.91 | 0.63 |
| Current at max (A) | 31.29 | 31.69 |
| P(in) at max (W) | 463.1 | 469.1 |
| P(out) at max (W) | 377.3 | 384.8 |
| Efficiency at max (%) | 81.5 | 82.0 |

## Aircraft performance estimate

| Metric | 4S1P | 4S2P |
| --- | --- | --- |
| Motors | 2 | 2 |
| All-up weight (g) | 2234 | 3238 |
| Wing load (g/dm^2) | 73.4 | 106.5 |
| Cubic wing load | 13.3 | 19.3 |
| Estimated stall speed (km/h) | 41 | 49 |
| Estimated level speed (km/h) | 91 | 92 |
| Estimated rate of climb (m/s) | 8.2 | 6.7 |

## Notes

- eCalc reports an accuracy of +/-15% for these estimates.
- Both configurations use the same propeller and motor; differences are driven by battery capacity and mass.
