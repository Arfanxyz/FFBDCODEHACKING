# FFBDCODEHACKING
this is only for ff diamond use only 1 time
/**
 * Converts an image from one format to another.
 * 
 * @param inputImagePath Path to the image to be converted.
 * @param outputImagePath Path to the output image.
 * @param outputFormat The format of the output image.
 * @throws IOException If an I/O error occurs while reading the input image.
 */
public void convertImageFormat(String inputImagePath, String outputImagePath, String outputFormat) throws IOException {
    // Read the input image
    BufferedImage inputImage = ImageIO.read(new File(inputImagePath));
    
    // Create an output image
    BufferedImage outputImage = new BufferedImage(inputImage.getWidth(), inputImage.getHeight(), BufferedImage.TYPE_INT_RGB);
    
    // Copy the input image to the output image
    Graphics2D g2d = outputImage.createGraphics();
    g2d.drawImage(inputImage, 0, 0, null);
    g2d.dispose();
    
    // Write the output image to the specified path
    ImageIO.write(outputImage, outputFormat, new File(outputImagePath));
}
