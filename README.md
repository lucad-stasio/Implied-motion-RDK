**Overview**

This repository contains a JavaScript implementation of a Random Dot Kinematogram (RDK), a classic visual stimulus used in neuroscience to study motion perception. This project is built as a plugin for the JsPsych library, designed for easy integration into web-based behavioral experiments.

The primary purpose of this tool is to serve as a motion adaptor for experiments investigating the "implied motion" theory of social attention.


**Scientific Background**

This project is directly inspired by the work of Guterstam & Graziano (2020) in their paper, "Implied motion as a possible mechanism for encoding other people’s attention." The core hypothesis is that the human brain perceives social cues, like another person's gaze, as a form of "implied motion" that can influence our own perception.

To test this, a reliable motion adaptation stimulus is required. This RDK is a modernized, web-based replication of the stimulus used in classic motion perception studies (e.g., Kiani et al., 2008), designed to serve as the foundational tool for these new experiments.


**Key Features**

This RDK stimulus is highly configurable and replicates the key features of the original Matlab implementation, including:

Configurable Coherence: Easily set the percentage of dots moving in a coherent direction.

Dot Lifetime: Control the lifespan of each individual dot, measured in frames (dot_life), to force global motion perception.

3-Frame Interleaving: Implements the specific interleaved presentation logic (number_of_sets) to create an ultra-smooth and scientifically precise motion percept.

Full Parameter Control: Allows for customization of dot speed, density, size, color, and aperture properties.


**Technologies Used**

JavaScript

JsPsych Framework

HTML5 Canvas


**STATUS**

The project is currently in the validation phase. The core functionality is complete, and the stimulus is working. The current focus is on rigorously comparing the output of this JavaScript version to the original Matlab script to ensure a perfect 1-to-1 replication of the stimulus behavior.


**How to Use**

This stimulus is designed to be used as a JsPsych plugin. A basic trial can be configured as follows:

// A basic JsPsych trial using the RDK plugin
const rdk_trial = {
  type: jsPsychRdk.default, // The plugin type
  coherent_direction: 90,    // Motion direction in degrees (90 = up)
  coherence: 0.4,          // 40% of dots move coherently
  dot_life: 3,             // Each dot exists for 3 frames
  number_of_sets: 3,       // Use 3-frame interleaving
  trial_duration: 2000     // Show stimulus for 2 seconds
};
