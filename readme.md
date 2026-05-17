# Part 2: CNN Computer Vision — Surface Defect Classification

## Task 6: CNN Concept Explanation

### What is Convolution?
Convolution is the core operation in a CNN. A small filter (e.g. 3x3)
slides across the image and computes dot products with local patches of
pixels. This extracts features like edges, textures, and patterns.
Early layers detect simple edges; deeper layers detect complex shapes.

### Why is Pooling Used?
Pooling (MaxPooling) reduces the spatial size of feature maps after
convolution. This reduces computation, controls overfitting, and makes
the model more robust to small shifts or distortions in the image.

### Why is ReLU Commonly Used in CNNs?
ReLU (Rectified Linear Unit) sets all negative values to zero.
It is preferred because it is computationally fast, avoids the
vanishing gradient problem, and introduces non-linearity which
allows the network to learn complex patterns.

### Why CNNs Beat Regular Neural Networks for Images?
A regular dense network treats each pixel independently, ignoring
spatial relationships. CNNs use shared filters that slide across
the image, so they learn local patterns efficiently and with far
fewer parameters. They are translation-invariant — the same pattern
is detected regardless of where it appears in the image.

---

## Task 7: Business Use Case — Manufacturing Quality Control

This CNN model can be directly applied in a manufacturing production line:

- **Problem:** Manually inspecting products for surface defects
  (scratches, dents, stains) is slow and error-prone.
- **Solution:** Install cameras on the conveyor belt. Feed each
  product image through the CNN model in real-time.
- **Output:** The model classifies each item as normal or defective
  (scratch/dent/stain) and triggers an alert or rejection arm.
- **Impact:**
  - Reduces human inspection cost by up to 80%
  - Increases inspection speed (milliseconds per image)
  - Consistent accuracy — not affected by fatigue or shift changes
  - Can be retrained as new defect types emerge
