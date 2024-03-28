# ML 23/24-04 Implement the Spatial Pooler SDR Reconstruction 

# Implementation
The project Implement the Spatial Pooler SDR Reconstruction is developed using C# .Net Core in Microsoft Visual Studio IDE (Integrated Development Environment) and is used as a reference model to understand the functioning of the reconstruction method. 
  
Methods added:  
# RunRustructuringExperiment()
Snippet of method added in-order to achieve the reconstruct functionality for integer input.
[Refer code in Git for RunRustructuringExperiment method](https://github.com/MusabChishti/neocortexapi/blob/cbc59dfd55ff85788915e9f2ac7d262aba9281a5/source/Samples/NeoCortexApiSample/SpatialPatternLearning.cs#L277)
~~~csharp
         private void RunRustructuringExperiment(SpatialPooler sp, EncoderBase encoder, List<double> inputValues)
        {
            // Create a directory to save the bitmap output.
            string outFolder = nameof(RunRustructuringExperiment);

            // Check if the directory exists, delete it if it does, then recreate it.
            if (Directory.Exists(outFolder))
            {
                Directory.Delete(outFolder, true);
            }
            Directory.CreateDirectory(outFolder);
~~~
      

  
   
# Steps to run the project.
1)Clone [this](https://github.com/MusabChishti/neocortexapi.git) repository to your local machine.

2)Ensure you have the necessary dependencies installed, including:

Daenet.ImageBinarizerLib
LearningFoundation
NeoCortex
3)Open the solution in your preferred C# IDE.

4)Build the solution to ensure all dependencies are resolved.

5)Before running the experiment, make sure to check for the input image path and specify the output folder where the generated images will be saved.

	Input Image Path: Ensure that the path to the input image is correctly specified in the code. This is typically set in the BinarImage().
	Output Folder: Specify the path to the folder where the generated images will be saved.This is typically set in the BinarImage().
	Bitmap Output Path: The bitmap images generated during the experiment will be saved in the output folder specified. You can find the generated bitmap images in the below mentioned folder after running the experiment.
	neocortexapi\source\Samples\NeoCortexApiSample\bin\Debug\net8.0\RunRustructuringExperiment.
6)Run the SpatialPatternLearning class to start the experiment.

7)Follow the on-screen prompts to choose between integer and image inputs.

8)Review the output to see the results of the experiment, including similarity metrics.

# RunRustructuringExperimentImage()

Snippet of method added in-order to achieve the reconstruct functionality for Image input.
[Refer code in Git for RunRustructuringExperimentImage method](https://github.com/MusabChishti/neocortexapi/blob/cbc59dfd55ff85788915e9f2ac7d262aba9281a5/source/Samples/NeoCortexApiSample/SpatialPatternLearning.cs#L408C29-L408C60)
~~~csharp
         private static void RunRustructuringExperimentImage(SpatialPooler sp1)
        {
            // Create a directory to save the bitmap output.
            string outFolder = nameof(RunRustructuringExperiment);
            Directory.Delete(outFolder, true); // Delete existing directory if exists
            Directory.CreateDirectory(outFolder); // Create new directory

~~~

# BinarImage()

Snippet of method added in-order to Binarize Image.
[Refer code in Git for BinarImage method](https://github.com/MusabChishti/neocortexapi/blob/cbc59dfd55ff85788915e9f2ac7d262aba9281a5/source/Samples/NeoCortexApiSample/SpatialPatternLearning.cs#L359C30-L359C42)
~~~csharp
         private static int[] BinarImage()
        {
            // Binarize the image (Assuming this function works correctly)
            NeoCortexUtils.BinarizeImage("D:\\Code-X\\Capture.PNG", "D:\\Code-X\\abcs.txt", 130, "");

            // Path to the text file containing binary data
            string file = "D:\\Code-X\\abcs.txt";
~~~
Before running the experiment, make sure to check for the input image path and specify the output folder where the generated images will be saved.

	Input Image Path: Ensure that the path to the input image is correctly specified in the code. This is typically set in the BinarImage().
	Output Folder: Specify the path to the folder where the generated images will be saved.This is typically set in the BinarImage().


## Input and Reconstructed Output 
Sample of a input and reconstructed output bitmap: The bitmap images generated during the experiment will be saved in the output folder specified. You can find the generated bitmap images in the below mentioned folder after running the experiment.
	neocortexapi\source\Samples\NeoCortexApiSample\bin\Debug\net8.0\RunRustructuringExperiment

  

  
  
## Testing

The Below figure 1 shows a snippet from Input of integer 8. Figure 2 is reconstructed output image with the similarity.

![figure 1](https://github.com/MusabChishti/neocortexapi/assets/148814256/55e00cf7-991c-4d54-9413-79895c7b8ea7)


![Figure 2 - similarity=80.5](https://github.com/MusabChishti/neocortexapi/assets/148814256/cef94afb-1908-4e11-8595-b302a65f862c)

Below Image also represent input as an integer and reconstructed output image.

![Multiple Integer Input and reconstructed output Image ](https://github.com/MusabChishti/neocortexapi/assets/148814256/61309e4f-dca6-4c42-847f-966e30c8b2d6)


The Below figure 3 shows a snippet from input of Image. Figure 4 is reconstructed output image.

![figure 3](https://github.com/MusabChishti/neocortexapi/assets/148814256/d75d399e-8573-4983-8ed2-dc599b155d7b)

![Figure 4- with 36.71 similarity](https://github.com/MusabChishti/neocortexapi/assets/148814256/4bfae777-0913-4298-8100-35f204c7ce4c)


#
Program Link: https://github.com/MusabChishti/neocortexapi/blob/CodeX/source/Samples/NeoCortexApiSample/SpatialPatternLearning.cs  
Forked from: https://github.com/ddobric/neocortexapi


#### Team Contribution Links:  
Consolidated commits and changes of all members available at -->  [ Team CodeX Branch ](https://github.com/MusabChishti/neocortexapi/commits/CodeX/)


