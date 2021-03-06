# Building a box with pyRouterJig
## Introduction
pyRouterJig is a powerful application that allows you to create templates that are compatible with the Incra LS positioner. The Incra LS positioner is essentially a fence control sytem that constrains movements to 1/32" (or 1 mm in the metric version).  By using a template, you can guide the fence to exact and repeatable locations. This in turn allows you to cut box and dovetail joints with a very high degree of preciusion.  These templates will also work with older versions of Incra positioners and the JoinTech IPM
## What is a Template?
In this context, a template is used to guide the positioning of a LS router fence to allow a cut to be made with a router in a specific location.  Box Joints and Dovetail Joints are easily created using  these templates.
## Installing and Using pyRouterJig
Go to the [pyRouterJig website](http://lowrie.github.io/pyRouterJig/) and follow the instructions on the “installation” page for your specific computer type. Once it is installed, run the application and you will see the following screen.
<figure>
<a name="figure1"></a>
<img src="{{ site.baseurl }}/images/opening_screen_shot.png" alt="Opening screenshot">
<figcaption>
<b>Figure 1.</b>  Opening screenshot. The screenshot doesn't show the
mouse pointer, which is located over the <b>Bit Width</b> input box so that its tooltip appears.
</figcaption>
</figure>
The default template is for an equally spaced box joint with a 7 ½” x 3/4” board, using a ½” straight bit. 
Hardware parameters are in the lower left.  You can select a board width, board thickness (bit depth) and bit width.  To make a dovetail template, you specify the bit angle, this should match your dovetail bit. Template parameters are in the lower right. There are 3 tabs: fixed, variable and edit.  
For more details on the various options and controls, see the documentation.
Creating Templates
We will start with a simple template project.  We are going to make a box that 6” wide, 8” long and 4” tall with 3/8” box joints. The material is ½” hardwood.  So, we plug in 4” for the board width, 3/8 for the bit width, ½ for the cut depth and 0 for the bit angle.  This yields a template that has shorter fingers on either end. 
<screen shot>
Note that each finger has the number of 1/32” increments written on it. So the two end fingers are 10/32”(5/16”) while the rest of the fingers are 12/32” (3/8”, our bit width). If this is ok you can proceed to printing your template out.  However, we wanted to have all fingers to be the same size so we need to widen the board by 4/32” (1/8”).
<screen shot>
This is essentially the same as Incra’s BOXD <double check> template and we would normally not bother making this one.  
Once you are satisfied with your template, you should first save it and then print it out.
Printing and using Templates
Printing is very simple.  Select File/Print and click on the printer icon to print. But, not all printers are accurate so you will need to verify your printout.  Print out your template and then, using a known accurate ruler, measure the distance between the two gray end parts of the template. If is within 1/32” of your board width then your printer is accurate enough.  If it is not, see the appendix “Compensating for Inaccurate Printers”.
For the best results, you should use a heavier paper.  90 lb paper is recommended but in a pinch you can use as thin as standard 20 or 24 lb paper. In general, thicker is better for stability. After printing, do not try to correct for paper curl - paper is fairly stretchable and you can distort your template. You will need to stabilize the template quickly.  Use regular sticky tape (Scotch brand) and tape over the top of the template.  Do not stretch the tape or you will distort the template. Now cut out the template and leave about 1/4“ on either side. Turn the strip over and apply tape to the back.  Now trim the template to the edge. It’s now stable enough to insert in the LS positioner. I prefer satin finish tape to avoid any reflections.
<insert  3 pix of taping and cutting>
To insert the template in the LS Positioner, you will need to “cup” the end slightly.  Then side it in a bit.  Use a combination of push and pull to get it where you want. Be gentle as you slide in, especially if you have used thinner paper.
A slightly more complex example.
Take the example we used earlier: 6” X 8” x 4 1/8”.  Let’s add a top and bottom of 3/8” thick wood and have the top 2 fingers be part a hinged lid. We will assemble the box with it’s top and bottom glued on and then cut the lid off on the table saw.  We want all the fingers to be the same size when we are done so we need to make the finger where we will cut wider by the width of our saw kerf.  If you have a thin kerf blade, you will need to add 3/32” and a standard kerf blade requires 4/32” (1/8”). If you are using a band saw to cut the lid off, determine how thick your blade kerf is and add enough to compensate. Note that you should factor in cleaning up the usually rough band saw cut.  We’ll add 1/8” to the board width and then use the editor to make room for the kerf.
So, make the board 4 ¼” wide and leave all the other parameters the same.  Then click on the editor tab.  You will see this
<insert screen shot>
The left slot (5A) is selected. Click on the left Move button twice to move it 2 increments to the left.  That makes the slot with cuts 5B and 6B wider by 1/16. 
<insert screen shot>
Now, click on the All button and then click on the Toggle button. This has the effect of selecting all but the left slot.  Now press the right Move button twice.
<insert screen shot>
Now we have a template that will give us a ½” finger in the 3rd position.  When the box is cut apart just below the 2nd finger position, all the fingers will have the same size. Note: be sure to read up on how to cut the tops off of boxes like this, it can be a safety hazard.
Aligning your template
We have included 2 ways to align the template on your positioner.  Incra recommends setting the fence so the bit is centered on your board. To do that, they recommend you make two cuts in a thicker piece of the same width wood and use that to find the center. We have included a center line (or point out the cut that is at the center) so you can continue to use that approach.
However, because pyRouterJig knows your board width there is a faster, easier and more accurate way to align your template. You will notice there is a mark to right of the template marked “align”.  This is 1/2 the bit width from the right end of the board. You just make the positioner fence flush with the bit and then move the template’s align mark under the cursor. Now you are perfectly aligned.  If you are using a straight 2 flute bit, you will want to rotate it so a cutting edge is pointing directly away from the positioner base before making the fence flush with the bit. Using the micropositioning capability of the Incra product, you can get very accurate alignment with this technique. This way you avoid the extra piece of thicker wood and the cuts of the centering scheme described above. In addition, this approach can be more accurate than the centering scheme because it doesn’t rely on visually finding the center.
<some pix showing this>
Status API Training Shop Blog About Pricing
© 2016 GitHub, Inc. Terms Privacy Security Contact Help
