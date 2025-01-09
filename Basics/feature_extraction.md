# Feature Extraction

## Time Domain Features

### Amplitude Envelope
The Amplitude Envelope (AE) aims to extract the maximum amplitude within each frame and string them all together. It is important to remember that the amplitude represents the volume (the loudness) of the signal. First, we split up the signal into its constituent windows and find the maximum amplitude within each window. From there, we plot the maximum amplitude in each window along time.

We can use the AE for onset detection or the detection of the beginning of a sound. In various speech processing applications this could be someone speaking or external noise, whereas in Music Information Retrieval (MIR) this could be the beginning of a note or instrutment.

The drawback of AE is that it's not as robust to outliers as RMS (root mean square energy).

### Root Mean Square Energy (RMS)
It is quite similar to the Amplitude Envelope (AE). As opposed to onset detection, however it attempts to preceive loudness, which can be used for event detection. Futhermore, it is much more robust against outliers, meaning if we segment audio we can detect new events (such as a new instrument, someone speaking etc) much more reliably

As we window across our wave form, we square the amplitudes within the window and sum them up. Once that is complete, we will divide by the frame length, take the square root and that will be RMS energy of that window.

### Zero-Crossing Rate (ZCR)
The Zero-Crossing Rate (ZCR) aims to study the rate in which a signal's amplitude changes sign within each frame. 

For Music Information Retrieval (MIR) this is feature is relevant for identifying a percussion sound as they often have fluctuating signals that ZCR can detect quite well as well as pitch detection. 


## Frequency Domain Features

### Fourier Transform (FFT)

The Fourier Transform decomposes an audio signal into its constituent frequencies revealing the underlying spectral characteristics. **It breaks down a complex audio signal into a series of simple sinusoidal waves** each with its own unqiue frequency, amplitude and phase. It's basically used to convert time-domain signals into frequency-domain representations, enabling sophisticated feature extraction.

### Spectograms

It's a visual representation of audio signals that reveals how frequencies evolve over time. It transforms complex audio data into an intuitive, multi-dimensional visualization. The key characteristics are: Time (progresses horizontally from left to right), Frequency (Represented vertically with low frequencies at the bottom and high frequencies at the top), Amplitude (Indicated by color intensity or brightness, where brighter/more intense colors represent louder sounds)

### Mel-Frequency Cepstral Coefficients (MFCCs)

MFCCs transforms raw audio signals into a compact, meaningful representation that mimics human auditory perception. They are specialized coefficients designed to capture the essential spectral characteristics of audio signals. They convert complex audio data into a reduced-dimensional feature vector that preserves critical sound information.

As per pplx:
The MFCC extraction involves several key stages:
1. Pre-Emphasis
- Enhances higher frequency components
- Increases signal energy at higer frequencies
2. Framing and Windowing
- Divides audio signal into short, overlapping segments
- Prepares signal for frequency analysis
3. Fast Fourier Transform (FFT)
- Converts time-domain signal to frequency domain
- Reveals spectral characteristics
4. Mel Filter Bank
- Applied non-linear mel scale transformation
- Mimics human auditory system's frequency perception
5. Discrete Cosine Transform (DCT)
- Decorrelates filterbank coefficients
- Reduces redundancy
    - Highlights most significant sound features