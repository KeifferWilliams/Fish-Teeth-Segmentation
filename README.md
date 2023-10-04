# Fish teeth segmentation tutorial using 3D Slicer

This tutorial will walk you through how to segment fish teeth in 3D Slicer. If you need more general instructions on how segmentation in 3D Slicer works, please review [Introduction to Image Segmentation in 3D Slicer](https://github.com/SlicerMorph/Tutorials/tree/main/Segmentation#readme). This tutorial also assumes you are familiar with importing data into Slicer. Please review the [ImageStacks](https://github.com/SlicerMorph/Tutorials/tree/main/ImageStacks) module if you are unfamiliar with importing data before starting this tutorial.
### Step 1: Visualize Data
As we are just interested in segmenting the teeth of, it is a good idea to crop out only the jaws in your region of interest (ROI) while importing your data. Here, I have made a segment called "Oral.Jaws" using the threshold tool that is cropped to include all components of the upper and lower jaws:
 <img src=https://raw.githubusercontent.com/KeifferWilliams/Fish-Teeth-Segmentation/main/Slide1.PNG >
### Step 2: Segment teeth
Start by adding a new segment that will be used to segment our teeth. I have named my segment "left.side.dentary.teeth". Switch your view to "Conventional". Select the paint tool. Under the paint tab, check the Sphere brush option. Under the masking tab, select "Inside all segments". 

Navigate your cursor with the sphere brush tool selected over the red panel. Once there, you should see your sphere appear on the 3D screen. Notice the size, if you want it larger, increase it under the paint tab. If you need it smaller, decrease it:

<img src=https://raw.githubusercontent.com/KeifferWilliams/Fish-Teeth-Segmentation/main/Slide2.PNG> 

 Once you are satisfied with the size, navigate to the anterior-most point of the lower jaw and start painting all teeth of interest. For this walk-through, I will only paint the left side dentary teeth. 

### Step 3: Separate teeth (if necessary)
Once you have finished segmenting, you may have upper and lower jaw teeth sticking together. You will need to separate these teeth using the scissor or erase tool if this is the case. In this example scan, we don't have any teeth sticking together so this step is not necessary: 

<img src=https://raw.githubusercontent.com/KeifferWilliams/Fish-Teeth-Segmentation/main/Slide3.PNG>

However, we do have a few partial upper jaw teeth that I segmented in addition to the left-side lower jaw teeth that I'm interested in. You can either remove these now in Slicer, or you can remove them downstream in your project pipeline using a different software (such as Meshlab). For the purposes of my work, I am fine keeping these extra pieces in, but if you needed only the teeth or lower jaw, you will want to remove them using the scissors and/or erase segment tool.

### Step 4: Export segment as .stl file

To export your segment of the lower jaws as a .stl file, click the green right-ward facing arrow next to the "Show 3D" tab. This will automatically take you to the Segmentations module. Scroll down and click on the "Export to files" tab. Select the directory you want to export to. Do not change any other settings! Finally, click "Export": 

<img src=https://raw.githubusercontent.com/KeifferWilliams/Fish-Teeth-Segmentation/main/Slide4.PNG>

When finished, the folder that you selected to export your .stl files should pop up. Notice that Slicer will export all segments you've created so it is very important to name them so you know which segment is which!

> Written with [StackEdit](https://stackedit.io/).
