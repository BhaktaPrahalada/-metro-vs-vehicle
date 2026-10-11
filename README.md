# Metro vs Vehicle

A commute comparison tool for Hyderabad. Enter a trip distance and your vehicle type, and see the CO₂ and money you would save by taking the metro, plus tips for avoiding metro crowding.

Built for **Environmental Hacks** (WeMakeDevs x AWS Builder Center, Bharat Builds Tour), **Air track**, by a solo participant with no coding background.

## The problem

Indian cities are getting more polluted, and many households run two or three petrol or diesel vehicles. Talking to commuters, the reason many skip the metro is not that they don't care. It is **overcrowding**: people try the metro, then go back to their own vehicles when it is packed. Fewer personal vehicles means cleaner air, smoother traffic and safer roads.

## What it does

- Takes trip distance (0.5 km steps) and vehicle type (two-wheeler, petrol car, diesel car, auto-rickshaw)
- Shows CO₂ saved per trip, percentage saved, and a weekly figure (5 trips)
- Compares trip cost (fuel + parking vs metro fare) with a bar chart and hover details
- Explains the traffic and road-safety benefit of fewer vehicles
- Gives crowding tips for three crowding levels, plus general peak-hour tips
- Lists every assumption in a footnote

## How AWS is used

- **AWS PartyRock** (no-code generative AI app builder, listed under "Build It" in the hackathon tool list): the app was designed and prototyped here by describing it in plain English.
- No AWS cloud services are deployed for this project.

## How it was built

1. Chose the Air track and researched the problem by asking commuters.
2. Prototyped the app in AWS PartyRock.
3. Exported the PartyRock handoff bundle (`app-handoff.zip`: `Requirements.md`, `Steering.md`, `src/App.tsx`).
4. Used Claude (an AI assistant) to turn that exported prototype into a standalone file, `metro-vs-vehicle.html`, using the same constants, tips and layout, so the app can run in any browser.

## Run it

Download `metro-vs-vehicle.html` and open it in a browser. No install needed.

## Assumptions and limits

All figures are rough, hard-coded estimates, not measured data: CO₂ factors in g/km (bike 35, petrol car 120, diesel car 140, auto 100, metro 15), fuel about ₹107/L petrol and ₹97/L diesel, fuel economy and parking costs per vehicle type, and metro fare about ₹2.5/km (₹10 minimum, ₹60 maximum). Real values vary by vehicle, route and station. There is no live crowding data yet.

## Early feedback

Three commuters tried the idea. All found it helpful; one said it shows how much we personally pollute the city, and one suggested better public transport could lower both costs and pollution. This is a tiny pilot, not proof.

## Next steps

Connect real crowding data from the metro operator, add saved routes, and add more cities.
