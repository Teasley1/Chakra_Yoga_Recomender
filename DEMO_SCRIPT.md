# Recorded demo and paper review — suggested 4–6 minutes

**0:00–0:40 | Introduction.** "My project is a personalized chakra-based yoga pose recommender. It uses rule-based ranking rather than training a machine-learning model. My question is whether preferences improve top-pick matches over chakra-only filtering."

**0:40–1:30 | Data and code.** Open the Colab notebook. Show the 21-pose DataFrame and its fields, including pose source links. Explain that metadata is manually organized and not medically validated.

**1:30–2:40 | Three methods.** Show baseline_recommend, personalized_recommend, and weighted_recommend. Explain filtering by chakra and scoring for level, body focus, and goal; weighted scores use 1/2/3.

**2:40–3:40 | Live demonstration.** Select Runtime > Run all (or show already-executed cells and rerun a sample). Show Profile 1: baseline Mountain Pose, personalized Child's Pose. Explain why the top pick changes.

**3:40–4:40 | Results.** Show the comparison chart: 2.0/3 baseline versus 3.0/3 for both personalized methods. Point out that list match rates are the same, and weighting did not outperform equal weighting.

**4:40–5:30 | Limitations and paper review.** Show the Solar Plexus weak case (only three poses). Explain small dataset, manually labeled fields, five fixed profiles, and that reviewer responses are simulated examples rather than human-study data. Briefly scroll through the paper sections and references.

**Closing.** "The prototype improves preference matching of the top-ranked pose on these test profiles. It does not establish health benefits or generalize to all users."

Record the screen and your voice, verify playback and permissions, then paste the video URL into the supplemental page.
