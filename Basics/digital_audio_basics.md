# Digital Audio Basics

This has theory about Sampling rate, bit depth, waveforms, frequency.

## What is Digital Audio

It's the representation of sound, recorded or converted into a string of binary digits - or bits - that can be stored, processed and played back on a computer.
During the analog to digital conversion process, the amplitude of an analog sound wave is captured at a specified interval, known as the sampling rate. It's then "quantized" to one in a set of discrete levels determined by the bit depth.

## Sampling rate

The sample rate in digital audio is a lot like the frame rate in video. It's the number of samples per second that are taken of a waveform to create a discrete digital signal. The higer the sample rate, the more snapshots you capture of the audio signal. The audio sample rate is measured in Kilohertz (kHz) and it determines the range of frequencies captured in digital audio.

The sample rate of digital audio determines the higest frequency you can capture and reproduce and that's it.

The average sampling rates are - 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz - this may seem a bit random but they aren't!

The relationship between sample rate and the highest frequency that can be captured and reproduced is in fact quite simple: to a capture a given frequency - let's call it $f$ - the sample rate just need to be $2*f$. So if we accept that the upper limit for human hearing is 20 kHz (although for most people it's atleast 40 kHz)

### Sample rates and aliasing
one of thhe fundamental laws of digital audio is related to that $2*f$ thing. If the higest frequency we want to record - $f$, sometimes called the Nyquist Frequency - requires a sample rate of $2*f$, what happens if we try to record a frequency _higher_ than $f$ with that sample rate? In short, something called aliasing. It's a type of digital distortion and the way to avoid it is by "bandlimiting" the audio signal before we convert it to a digital. Bandlimiting just means restricting the range of frequencies in a signal to a set upper limit and it is done by using a low-pass filter to remove frequencies above that limit, $f$. If we wanted to record frequencies up to 20 kHz but choose 40 kHz as out sample rate, we would have to instantly eliminate all frequencies above 20k using a so-called "brick wall" low-pass filter.

## Bit Depth

The audio bit-depth of a file determines a few things. Most directly, it determines the number of possible discrete amplitude values we can utilize for each audio sample. The higher the bit depth, the more amplitude values are available per sample. More to the point though, it determines the noise floor of the system.

The bit-depth of digital audio determines how low the noise floor is. Not how detailed the recording is, or how big the "stair-steps" in the digital signal are - those don't actually exist, despite a lot of images that suggest they do. 

In digital audio, there are two types of bit-depth: fixed point and floating-point. The most common fixed-point bit depths are 16-bit and 24-bit, and the most common floating point format is 32-bit.

## Waveforms

A waveform is a graphical representation of a sound wave as it mvoes through a medium over time. It has four fundamental characteristics: Wavelength, Amplitude, Frequency, Velocity.

The wavelength of a wave is the length in meters from the start ot the end of one full cycle of the waveform eg from crest-to-crest.

The amplitude is the maximum displacement of a wave from centerline to the peak, not from peak-to-peak. The greater the distance from the centerline of a waveform, the more intense the pressure variation will be withing a mediu, hence the louder it is preceived.

The frequency is how many complete waves there are per second passing a certain point. The frequency indicates the rate of pressure variations or cycles per second of a wave. (Lower frequency sound waves have longer wavelength and lower pitch, higher frequency sound waves have shorter wavelength and higher pitch)

The velocity is the speed and direction of a soundwave. Soundwaves travel at different speeds through different mediums. Generally speaking the denser the medium the faster sounds travels through it.