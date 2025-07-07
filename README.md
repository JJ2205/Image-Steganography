Image Steganography

This project demonstrates **Image Steganography** using Python. Steganography is the practice of hiding secret data within an ordinary image. Here, I used **Least Significant Bit (LSB)** manipulation to hide and extract grayscale images.


 Project Structure
 
Image-Stegnography/
├── steganography.py # Hides secret image into cover image
├── reverse.py # Extracts secret image from steganographed image
├── Cover.png # Original cover image (grayscale)
├── Secret.png # Image to be hidden (grayscale)
├── steganographed_image.png # Output image with hidden data
├── extracted_secret_image.png # Extracted hidden image


---

 How It Works

 'steganography.py'
- Takes two grayscale images: `Cover.png` and `Secret.png`
- Embeds the **MSB of the secret image** into the **LSB of the cover image**
- Saves the result as `steganographed_image.png`

 'reverse.py'
- Reads `steganographed_image.png`
- Extracts the LSB from each pixel
- Reconstructs and saves the hidden image as `extracted_secret_image.png`



 Example

1. Before Steganography
   - `Cover.png` — Clean grayscale image
   - `Secret.png` — Image you want to hide

2. After Steganography
   - `steganographed_image.png` — Visually similar to cover image, but contains secret

3. After Extraction
   - `extracted_secret_image.png` — Recovered secret image


