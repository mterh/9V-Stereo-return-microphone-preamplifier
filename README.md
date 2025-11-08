# 9V-Stereo-return-microphone-preamplifier
A simple microphone preamplifier in the standard guitar pedal format designed for live usage.

This circuit is a microphone preamplifier designed to make dynamic microphones usable with guitar-pedals. It provides sufficient gain to bring a microphone-level signal up to typical pedal operating levels while maintaining low noise performance. Since it is designed for live usage I decided not to add 48V phantom power, which also would have required a more sophisticated power section, as well as a power supply differing from the standard 9V dc found in other guitar effect pedals.

The pedals has a balanced XLR input, a 6.3 mm send, stereo 6.3 mm return inputs, and balanced stereo XLR outputs. A led on the front is used to indicate when the preamp clips, with the threshold adjustable via an onboard trimmer. Gain configuration is handled by a 3-position DIP switch on the PCB, allowing selection of the maximum available gain. This enables precise control of gain for different sources (e.g., vocals, trumpet) without the need for additional panel controls.

A ground-lift function is included. The input connector (Neutrik NC3FBH1) ties pin 1 directly to the chassis. For ground-lift operation, the output XLR connectors (Neutrik NC3MAH-S) route pin 1 to a PCB ground plane associated with the XLR output section, rather than directly to the enclosure, resulting in a serial star-grounding topology. This allows the output ground to be lifted while maintaining a proper chassis bond at the input.

Additionally, a selectable low-cut filter is available on the send path, allowing low-frequency attenuation (e.g. for vocal processing) to reduce potential muddiness in downstream effects.

The send can be turned On/Off with a footswitch. Another footswitch is used to bypass the pedal entirely, indicated by a led. The switching is done using two small signal relais which are controlled with a H-bridge and an ATTiny-85.

The 3 main controlls are a Gain pot, a Dry/Wet Mix pot and a output volume pot. The last one was added so that the user can adjust the volume of the whole signal live to control the volume of louder passages.
