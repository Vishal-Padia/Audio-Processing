# Basics of Audio PreProcessing

This has theory about Normalization, Resampling, Noise Reduction and filtering

## Why does Audio PreProcessing Matters?

It's essential for transforming raw audio signals into a high-quality standardized data that ML models can effectively utilize.

## Normalization

Normalization is the process of adjusting the volume of an audio recording to a target level.

Normalization scales the amplitude of audio signals to ensure:
- Consistenet signal magnitudes across datasets
- Prevention of bias towards high or low energy signals
- Improved model performance by standardizing input ranges

## Resampling

It involves:
- Standardizing sample rates across different audio files
- Improving computation efficiency
- Ensuring compatibility with specifc ML model requirements

## Noise Reduction

It includes:
- Filtering out background noise
- Removing audio artifacts
- Enhancing signal clarity for more accurate analysis

## Filtering

Some of the filtering techiques in audio preprocessing:
- Frequency filtering: Removing specific frequency ranges
- Psychoacoustic modeling: Leveraging human auditory system characteristics
- Critical Band filtering: Processing signals acorss different frequency bands
