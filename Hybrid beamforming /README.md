## Size of Antenna
 Size of Antenna depends on freqency of wave that should be transmitted
 if the freqeuncy is low ,the antenaa size is some what big and the applictaions are limited

 if the frequency is high (mmWaves),the antenna size is small,and we can fit large number of antenna in small applications

## Fully Digital Beamforming
 1. High Power Consumption

Every antenna requires its own RF chain.

For 64 antennas we use 64 RF chains

Each RF chain contains components such as:

DAC/ADC
Mixer
Amplifier
Filters

All consume electrical power.

2. High Hardware Complexity
More antennas require:

1.More RF chains
2.More converters
3.More circuits
4.More calibration

The hardware becomes increasingly complex.

## Hybrid Beamforming Solves This
Instead of 64 RF chains and 64 Antennas
Hybrid beamforming uses something like:

64 antennas

5 RF chains

↓

Phase Shifters

↓

64 antennas

## Why Is Designing Hybrid Beamformers Difficult?

The paper states that designing the analog and digital beamformers jointly is a hard optimization problem.

This is because:

The digital beamformer changes the optimal analog beamformer.
The analog beamformer changes the optimal digital beamformer.

They depend on each other.

This is why the authors use Alternating Minimization, updating one while keeping the other fixed.

It is also said that analog beamforming is implemented using phase shifters, which can only change the phase of the signal—not its amplitude.

## Least Squares Method
 In Alternating Minimization,we find digital beamformer or analog beamformer by keeping other fixed using Least Squares Method 
