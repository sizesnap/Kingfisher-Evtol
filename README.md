# EVTOL Mapping Aircraft

A 1.5 m span, 4-motor tilt-rotor VTOL built for aerial photogrammetry and in-flight water sampling. It takes off and lands vertically, transitions to efficient wing-borne cruise, and can hover over a lake or stream to lower a sampling winch (**Kingfisher**).

## Goals
- 20 mi range with a 0.5 kg payload
- Fast, efficient cruise for mapping missions
- Vertical takeoff and landing, with no runway needed
- Hover-and-dip water sampling with an onboard winch

## Design point (conceptual sizing)

| Parameter | Value |
| --- | --- |
| MTOW | 4.08 kg |
| Span | 1.5 m |
| Wing | 0.32 m², 213 mm chord, AR 7.0 |
| Stall speed | 13.0 m/s (CLmax 1.2) |
| Design cruise | 20 m/s |
| Estimated range | 38.6 mi at 20 m/s |
| Hover power | 473 W |
| Motors | 4 × T-Motor MN4014 KV330 |
| Props | Front APC 15×10E (tilting), rear 15×5 (locked in cruise) |
| Battery | 6S2P Molicel P50B, 216 Wh |

## Layout
- **Front:** 2 tilting motors for hover and cruise
- **Rear:** 2 fixed lift motors, props locked during cruise
- **Payload bay:** mapping camera or Kingfisher water-sampling winch

## Kingfisher water-sampling winch
The aircraft hovers above the water, lowers a sample bottle on a tether, fills it, and reels it back up before returning home. This lets you sample water where boats or waders can't easily reach.

## Repo structure
```
/cad          CAD models (airframe, mounts, winch)
/analysis     Sizing calculations and performance scripts
/electronics  Wiring, ESC and battery notes
/firmware     Flight controller config and winch control code
/docs         Write-ups, test logs, photos
```

## Status
- [x] Conceptual sizing
- [ ] Airfoil selection (CLmax ≥ 1.2 at Re ~170k)
- [ ] Bench-test front prop static thrust
- [ ] Confirm 4-motor vs tri-tilt layout
- [ ] Winch prototype
- [ ] First hover test

## Related
- Companion survey boat (in progress)
