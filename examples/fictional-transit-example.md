# Fictional Example: Can Residents Reach Frequent Transit?

This example illustrates the framework using a fictional city. It is not an assessment of any real transit agency or community.

## Civic question

Can residents in each grouped planning area reach frequent transit during the weekday morning period?

## Intended audience

Residents, community organizations, planners, and elected officials seeking a screening view of where scheduled access appears stronger or weaker.

## Evidence contract

| Input | Evidence class | Use | Boundary |
| --- | --- | --- | --- |
| Published transit stops | Scheduled | Identify access points | Does not prove a vehicle arrived |
| Published trips | Scheduled | Determine service frequency | Does not prove trips operated |
| Pedestrian network | Estimated | Calculate representative walking paths | Does not describe every person's mobility needs |
| Grouped population | Contextual | Weight area-level access | Does not identify households or prove demand |

## Method

1. Select a weekday morning time window.
2. Count scheduled arrivals at each stop.
3. Mark stops meeting the documented frequency threshold.
4. Route privacy-screened representative area points to qualifying stops.
5. Classify a point as within the screen when the routed walk meets the documented time threshold.
6. Aggregate grouped population ranges rather than individual addresses.
7. Publish the result as an estimate with method, date, coverage, and limitations.

## Public statement

> This screening estimate shows the grouped share of residents represented within the selected walk and scheduled-frequency thresholds. It describes published access, not whether vehicles arrived on time or whether every resident can make the walk.

## Failure behavior

- If the pedestrian router is unavailable, preserve the previous valid result and label its date.
- Do not silently replace routed walking with straight-line distance.
- If schedule coverage is incomplete, mark the area unavailable rather than assigning zero access.

## Privacy

- Use grouped population evidence.
- Do not publish household coordinates.
- Suppress areas below the selected population threshold.
- Present community context as context, not proof of inadequate service.

## Publication gates

The result remains private until source coverage, routing quality, suppression, public wording, mobile display, and operating cost have been reviewed.
