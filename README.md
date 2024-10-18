import matplotlib.pyplot as plt
import numpy as np

# Sample grayscale image data (replace with your actual data)
image_data = np.random.randint(0, 256, size=(100, 100))

# Calculate histogram
histogram, bins = np.histogram(image_data.flatten(), bins=256, range=(0, 256))

# Plot the histogram
plt.figure(figsize=(8, 6))  # Adjust figure size if needed
plt.bar(bins[:-1], histogram, width=1, edgecolor='black')  # Use bar for histogram

# Set plot labels and title
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.title("Grayscale Histogram")

# Customize grid lines and appearance
plt.grid(True, linestyle='--', alpha=0.5)
plt.xlim(0, 256)  # Set x-axis range to 0-255
plt.tight_layout()

# Show the plot
plt.show()
