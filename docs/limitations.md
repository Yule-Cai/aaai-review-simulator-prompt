# Limitations

This prompt is useful for structured self-assessment, but it has several important limitations.

## It is not an acceptance predictor

The output is a simulated review, not a real program-committee decision. Real decisions depend on reviewer expertise, competition, discussion dynamics, venue fit, and year-specific policies.

## It can miss technical issues

LLMs may fail to detect subtle mathematical errors, implementation bugs, statistical flaws, or missing assumptions.

## It can over-penalize or under-penalize novelty

Novelty assessment requires current field knowledge. If the model has no web search or literature access, it should not name specific missing papers.

## It depends on input completeness

If the user only provides an abstract or partial paper, the review should be treated as low-confidence.

## It may reflect model bias

Different models may produce different score calibrations. Running the prompt with multiple models or asking human experts is recommended.
