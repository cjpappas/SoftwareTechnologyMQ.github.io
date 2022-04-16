---
layout: page
title: "Getting Footage"
within: machine_learning
---

# Transfer Learning

We have been running existing models so far.  We would like to be able to create our own models.  Unfortunately that requires _a deep understanding of tensor networks_ and _thousands of labelled images_.  

unless....

If we use a technique called ["transfer learning"](https://youtu.be/kRpZ5OqUY6Y) we can adjust an existing model to perform a specialised task.  Watch the first six minutes of [this video](https://youtu.be/kRpZ5OqUY6Y) to get an idea of what we will be doing.

This all works much better if we use the same camera to capute the training data that we will use to run the predictor, so we need to capture data with the Pi camera and that is what we will do here

# Choose a specialised task.

Think of something you would like your Pi to detect for you, a simple on/off categorisation is easiest.  Here are some suggestions:
  * Is there someone with a red shirt?
  * Is there a coffee cup?
  * Is it day or night?
  * Has the Pi been inverted?
  * Is the Pi on its side?

# Capture footage that includes the "yes" and "no" state in multiple contexts

We've included a script to capture images from the camera attached to the pi called `capture.py`. It will capture an image approximately every 3 seconds and save it to the `images/captured_images` directory, saving the filename as the timestamp the image was taken. You can view these images through cyberduck. We recommend capturing between 20-100 images of each "state" that you are testing. For example if you were to do the "Is there a coffee cup?" example, it would be a good idea to capture between 20 and 100 images, with a coffee cup in the image and no coffee cup in the image. To run the script, make sure you are in the `pi_camera_detetction` folder and run:

```bash
python capture.py
```

# Split the footage into separate images.

This might not be relevant anymore since we capture images?

# Get the images off the Pi

You can access the images on the raspberry pi by using Cyberduck. To pull all captured images of the pi, you can simply download the `images/captured_images` folder to your local machine through Cyberduck.
