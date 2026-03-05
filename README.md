# Experiment 13: PCM Decoding

## Objectives
- Observe how a **PCM digital bitstream** is converted back into a **PAM signal**.
- Understand the importance of **clock and frame synchronization** in PCM decoding.
- Reconstruct the original message or speech signal using a **low-pass filter**.

---

## Materials
- Emona Telecomms-Trainer 101 with power supply
- Dual-channel 20 MHz oscilloscope
- Modules: PCM Encoder, PCM Decoder, Tuneable LPF, Buffer, VCO, Speech, Variable DCV
- Oscilloscope leads and patch cables

---

## Procedure

### Part A: Setting Up the PCM Encoder
1. Set the **PCM Encoder to PCM mode** and connect the setup with the **Variable DCV module** as the input.
2. Observe the **PCM DATA** and **Frame Sync (FS)** signals on the oscilloscope.
3. Adjust the **DC voltage** and confirm that the binary output increases or decreases accordingly.
4. Replace the DC input with a **sine wave from the VCO module**.

### Part B: Decoding the PCM Data
1. Connect the **PCM DATA, Clock, and FS signals** from the encoder to the **PCM Decoder**.
2. Observe the decoder output on the oscilloscope along with the original message signal.
3. Add a **Buffer module** and listen to the decoded signal using headphones.

### Part C: Encoding and Decoding Speech
1. Replace the sine input with the **Speech module output**.
2. Speak or sing and observe the PCM data and decoded signal on the oscilloscope.

### Part D: Message Reconstruction
1. Connect the **decoder output** to the **Tuneable Low-Pass Filter (LPF)**.
2. Slowly increase the **cut-off frequency** until the original signal is reconstructed.
3. Use the **Buffer module and headphones** to compare the reconstructed signal with the original.

---

## Results and Discussion
The PCM decoder produced a **stepped waveform**, indicating a **Pulse Amplitude Modulation (PAM)** signal where each voltage level represents a sampled value. By using the **clock and frame synchronization signals from the encoder**, proper decoding was achieved. Passing the PAM signal through a **low-pass filter** smoothed the steps and reconstructed the original analog signal.

---

## Key Observations
- The decoder output appears as a **staircase waveform** due to the sample-and-hold process.
- A **low-pass filter** is required to recover the smooth analog signal.
- Proper **clock and frame synchronization** are essential for accurate decoding.

---

## Learnings
This experiment demonstrated how **PCM digital data is converted back into an analog signal**. It highlighted the importance of **synchronization** between encoder and decoder and showed how **quantization limits signal accuracy**, meaning the reconstructed signal is similar but not perfectly identical to the original.
