# Matlab omr-toolbox

![omr-toolbox](https://github.com/wagner-lab/omr-toolbox/blob/master/docs/omr-toolbox-github.gif)

Matlab optical mark recognition (OMR) toolbox for scoring scanned forms. Requires Matlab's image processing toolbox. 

The general framwork for this toolbox is as follows:

1. Perform image registration to a pre-specificed "clean" template. This step cleans up the scanned-in image which can often be crooked, skewed and scaled differently than the template image.
2. Automatically determines location of "bubbles" and scores bubbles according to user specified thresholds (i.e., looks for bubbles with filled in pixels above some threshold). This ocassionally needs to be tweaked depending on the quality of the scans and of the image registration.
3. Cleanup scoring errors (missing data, duplicate responses). 

This toolbox was written for a specific use case and is not fully documented. Moreover, it generally requires that the user create forms that have the same registration marks as this toolbox was developed to analyze. See [template.pdf](https://github.com/wagner-lab/omr-toolbox/blob/master/docs/template.pdf) image for an example. An adobe illustrator file [template.ai](https://github.com/wagner-lab/omr-toolbox/blob/master/docs/template.ai) is also provided that can be edited to create forms that should work with the toolbox.
