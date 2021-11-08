# Organizers
This workshop is organized by CREATE staff and students, and features Andreas Refsgaard. 

Andreas Refsgaard is an artist and creative coder based in Copenhagen. He uses algorithms, coding and machine learning to explore the creative potentials of emerging digital technologies. He also offers workshops: <https://andreasrefsgaard.dk/workshops/>, in which, Andreas provides an introduction into how machine learning models can be productively integrated into existing workflows, integrated into websites and used for professional client projects. Through creative examples and hands-on exercises, he rolls out the many creative and technical possibilities machine learning brings to the field such as offering new and effective ways of prototyping and testing ideas. Andreas has previously taught workshops in machine learning and AI for creative technologists and developers at Facebook Reality Lab and at conferences like KIKK and Resonate. See also his new book in Danish: <https://www.skabtafenkunstigintelligens.dk> 

|  Time | Activity                                                                                                                    |
|-------+-----------------------------------------------------------------------------------------------------------------------------|
| 09:00 | Welcome: Intro to creative Machine Learning                                                                                 |
| 10:00 | Getting started with RunwayML: Understanding the interface, Exploring different types of models + inputs                    |
| 12:00 | Lunch                                                                                                                       |
| 13:00 | Advanced features: Training your own model, Exporting, Hosting models                                                       |
| 14:00 | Coffee Break + mingle: Talk to other people about what might be interesting to work on later                                |
| 14:15 | Work on an idea in groups                                                                                                   |
| 15:45 | Student  Presentations                                                                                                      |
| 16:00 | END of  Workshop, mingling  around  small  food                                                                             |
| 17:45 | Live connection to  the [TensorFlow Machine Learning Community Day](https://www.tensorflow.org/ml-community-day)            |
| 20:00 | End  of  the unofficial  program                                                                                            |
   
## Getting started with Runway ML   
### Expectations + debugging
👉 You can follow along and run the same models as I do, or just observe and take notes.

- If you experience errors running a model try to restart it and/or refresh the browser tab.
- Have a bit of patience when you start a new model, it can take up to a few minutes before it has loaded and is actually running.
- Sometimes your model might not load while I demonstrate it, or it might load a lot faster than mine.
- Let me know if I am going to fast or too slow and I will try to adjust the pace.

### A note on input images when trying out models in Runway 🖼 📷 🎞

The majority of models we will be working with use *image* as their input type. 
We will often demo them directly with the webcam, but you can also upload still images + videos and use those assets as inputs. 

Avoid using very big images (bigger than 1280x720 px) when just testing out models, since this will increase inference time and in some cases make the models crash. 

If a particular image does not work, try using another one. 
Stick to .jpg and .png formats for images and .mov and .mp4 for movies. 

Here is a small sample folder of images to use if you want to, but feel free to use your own images or images you find online: [https://drive.google.com/file/d/1WnPuf8kXMrRnLGfRhT20eVtj89L5j2fI/view?usp=sharing](https://drive.google.com/file/d/1WnPuf8kXMrRnLGfRhT20eVtj89L5j2fI/view?usp=sharing)

### 1) Image Analysis 

**Facial Landmarks:** [https://app.runwayml.com/models/runway/Facial-Landmarks](https://app.runwayml.com/models/runway/Facial-Landmarks)

Input type: Image 📷

Output Type: Array 📋 (List of x-and y-postions of facial landmarks)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/0ea9d690-ebb8-4eb7-94e9-3015862b8c71.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/0ea9d690-ebb8-4eb7-94e9-3015862b8c71.jpg)

**YOLOv4**: [https://app.runwayml.com/models/runway/YOLOv4](https://app.runwayml.com/models/runway/YOLOv4)

Input type: Image 📷 

Output Type: Array 📋 (Name of detected object, bounding box (x, y, w & h), confidence score)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c60d71a6-cdc0-45db-bee5-5ac23a73f908.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c60d71a6-cdc0-45db-bee5-5ac23a73f908.jpg)

### 2) Text generation models

**GPT-2:** [https://app.runwayml.com/models/runway/GPT-2](https://app.runwayml.com/models/runway/GPT-2)

Input type: Text (the more text you use for your prompt, the better results in general) ✍️

Output Type: Text ✍️

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/69053c32-a12d-4b9d-b5bf-f9f5f5eac133.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/69053c32-a12d-4b9d-b5bf-f9f5f5eac133.jpg)

👉 **Exercise: Write with GPT-2**
Run the GPT-2 model: [https://app.runwayml.com/models/runway/GPT-2](https://app.runwayml.com/models/runway/GPT-2)

Give GPT-2 a few lines of text about a specific subject as a prompt, and let's see what it comes up with! A good prompt clearly "steers" the text generation and makes it obvious what the text is about. The more prompt text, the better the output text normally is.

Examples of input prompts:

```Here is how to make a traditional apple pie in 10 easy steps: 

1) Preheat the oven```

or

```John Doe is a famous Danish football player who currently plays for Real Madrid. 
   He began playing football when he was just 5 years old```

#### Settings:
Adjust the *Max Characters* slider to the right, so you get a longer output than the default 64 characters. 

Load a bigger *checkpoint* (*Medium* or ***Large***) for better results, or use a small (*Extra Small* or *Small*) checkpoint for faster results and lower loading time. 

#### Post your results:
Post your best result in [this Google Document](https://docs.google.com/document/d/1Q-YQZ07Vkq7oALCu3BuCU0CCnbMoakWLR4YqlRnweXA/edit?usp=sharing).

### 3) Image generation with StyleGan (Latent Video Models)

Input type: Vector position ⌖

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/219c1c1e-9b86-4759-bf77-e20674bf234d.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/219c1c1e-9b86-4759-bf77-e20674bf234d.jpg)

👉 **Exercise: Faces vs Dogs - the impact of coherent training data**
Run the StyleGAN model [https://app.runwayml.com/models/runway/StyleGAN](https://app.runwayml.com/models/runway/StyleGAN) with the checkpoint "Flickr Faces HQ" selected and compare the outputs to running the same model with the "Dogs" checkpoint selected.

Tips:
If your model is running, but you don't see any images, make sure you click the "Vector" button at the top of the screen.

Drag the mouse or click the "regenerate" button to explore different outputs.

Post your results:
****Post the weirdest face🤪 and the weirdest dog 🐶 you can find in [this Google Document](https://docs.google.com/document/d/1Q-YQZ07Vkq7oALCu3BuCU0CCnbMoakWLR4YqlRnweXA/edit?usp=sharing).

Visual explanation of Vector Space by [Lia Coleman](https://twitter.com/lialialiacole?lang=en) and [Artificial images](https://artificial-images.com/): 

<iframe width="100%" height="315" src="https://www.youtube.com/embed/7cdfrUpYHrU?start=666" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

👉 **Exercise: Time to explore**
Try some of the models we have not tried yet and share your findings to inspire the rest of the workshop participants. 

Here are some of my favourites:

- **Colorization:** [https://app.runwayml.com/models/reiinakano/Colorization](https://app.runwayml.com/models/reiinakano/Colorization) 
- **Depth Maps:** [https://app.runwayml.com/models/akhaliq/Depth-Maps](https://app.runwayml.com/models/akhaliq/Depth-Maps)
- **U2-Net:** [https://app.runwayml.com/models/anastasis/U-2-Net](https://app.runwayml.com/models/anastasis/U-2-Net)
- **First-Order-Motion-Model:** [https://app.runwayml.com/models/runway/First-Order-Motion-Model](https://app.runwayml.com/models/runway/First-Order-Motion-Model)
- **Spade Landscapes:** [https://app.runwayml.com/models/genekogan/SPADE-Landscapes](https://app.runwayml.com/models/genekogan/SPADE-Landscapes)
- **ArtLine**: [https://app.runwayml.com/models/akhaliq/ArtLine](https://app.runwayml.com/models/akhaliq/ArtLine)
- **Fast Style Transfer:** [https://app.runwayml.com/models/genekogan/Fast-Style-Transfer](https://app.runwayml.com/models/genekogan/Fast-Style-Transfer)

Remember to ask for help if you get stuck or something is not working. But try to have patiences with the models, as they can take some minutes to load.

Post your results:
****Post interesting results in [this document](https://docs.google.com/document/d/1Q-YQZ07Vkq7oALCu3BuCU0CCnbMoakWLR4YqlRnweXA/edit?usp=sharing), and remember to write your name and the name of the model you used.

# Advanced features

## 4) Training models in Runway
We have explored three **pre-trained** models already and got an understanding of how they work. However, Runway has a powerful **training** mode that allows you to train your own versions of these models. 

For example, giving GPT-2 your own book(s) to train rather than the default webText, providing StyleGAN with your own dataset collection of images instead of just faces or labelling your own new objects  for YOLO to detect. 

👉 A good overview of the three different training options in Runway

[Model Training | Runway](https://runwayml.com/training/)

[https://www.youtube.com/watch?v=1shE4Mjie1I&ab_channel=RunwayML](https://www.youtube.com/watch?v=1shE4Mjie1I&ab_channel=RunwayML)

*Gene Kogan from Runway explaining how to train a StyleGAN model*

🔥 **Tips for gathering data to train StyleGAN**

- More pictures gives you better results. Try getting between 500 and 5.000 images (but ideally even more! Max is 25.000).
- StyleGAN generates 1x1 style images as output (for instance 1024x1024 px), so think about cropping your data in a 1x1 format before feeding them to Runway or via the **Dataset Preprocessing** feature in RunwayML.
- Aim for collecting hi-res images (ideally around 1024 px x 1024 px, but realistically perhaps 500x500 pixels).
- If a GAN is going to produce "realistic" looking images, you should try to train it with coherent data, similar looking objects, similar angles, light, crops, backgrounds etc. Otherwise you get nightmare cats (which is also cool, but perhaps not what you want?).

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-15_at_21.54.11.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-15_at_21.54.11.png)

🌐 **Links for collecting data**

- [Kaggle](https://www.kaggle.com/) - Dataset and ML community and database (eg. images of [Pokémons](https://www.kaggle.com/kvpratama/pokemon-images-dataset))
- [Google Data Set Search](https://datasetsearch.research.google.com/) - Search for datasets
- [Web Scraping](https://scrapism.lav.io/) - Sam Lavignes web scraping guide (python, requires code knowledge)
- [Image Downloader](https://chrome.google.com/webstore/detail/image-downloader/cnpniohnfphhjihaiiggeabnkjhpaldj) - Google Chrome Plugin to download all visible images on a website
- [Pindown Chrome Extension](https://chrome.google.com/webstore/detail/pindown/flieckppkcgagklbnnhnkkeladdghogp?hl=en) (costs a bit to use, but is perfect for instagram or Pinterest) - [Youtube Tutorial](https://www.youtube.com/watch?v=BwMk1Ik7aCM&ab_channel=ArtificialImages)
- [Splitting Video into individual image frames](https://youtu.be/ck11jOVYlIw) - Derrick Schultz video tutorial
- [Project Gutenberg](https://www.gutenberg.org/) - 60.000+ free eBooks (good for training GPT-2)

**Pre-processing data**

[Runway Tool Tips: Dataset Preprocessing](https://www.youtube.com/watch?v=dwlB5kG2CaQ&ab_channel=RunwayML)

## 5) Train an Object detection model with YOLO-v4

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37834404-93a2-45a2-8bd4-2945a487a4ad/Screenshot_2021-01-19_at_15.37.30.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/37834404-93a2-45a2-8bd4-2945a487a4ad/Screenshot_2021-01-19_at_15.37.30.png)

Walkthrough of annotating a dataset of cats🐱 and 🐶 downloaded from [Kaggle](https://www.kaggle.com/alvarole/asirra-cats-vs-dogs-object-detection-dataset).

🔥 *For an even more detailed walkthrough check out this [video](https://www.youtube.com/watch?v=XWyKkFj54aA&ab_channel=ArtificialImages)*  *by [Derrick Schultz](https://artificial-images.com/) explaining how to train a YOLO-v4 Object Detection Model in Runway* 
(I highly recommend his [videos](https://www.youtube.com/channel/UCaZuPdmZ380SFUMKHVsv_AA), courses and [Patreon](https://www.patreon.com/bustbright) content if you want to dig deeper into Machine Learning Art)

Example of trained YOLO model connected to P5JS + website

- [First Impressions](https://j3nsykes.github.io/FirstImpressions/)

<iframe src="https://player.vimeo.com/video/446832119?h=39a33168eb" width="100%" height="348" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
<p><a href="https://vimeo.com/446832119">firstImpressions</a> from <a href="https://vimeo.com/jensykes">Jen Sykes</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

## 6) Train a text generation model with GPT-2

Walkthrough of training GPT-2 using a corpus of sci-fi👽 stories from [Kaggle](https://www.kaggle.com/jannesklaas/scifi-stories-text-corpus)

[https://www.youtube.com/watch?v=-v5StaeOisM&t=5s&ab_channel=RunwayML](https://www.youtube.com/watch?v=-v5StaeOisM&t=5s&ab_channel=RunwayML)

*Gene Kogan from Runway explaining how to train a GPT-2 text model*

## 7) Hosted Models with Runway

💡 Hosted Models are a new feature to RunwayML. It is an alternative to connecting via HTTP or OSC (*see the P5JS examples above and Processing library below*). It provides a way of accessing your model via querying the information and waking up the model. Hosting a model provides you with a unique API  that you can use to interact with a model anytime, anywhere, without requiring Runway to be open! This is a more consistent method should you wish to make your work public in an exhibition or online via a website. 
[hosted model reference page](https://learn.runwayml.com/#/how-to/hosted-models)

✅ **Positives about Hosted Models:**
- Sometimes a model interaction will time out when running local network connections. 
****- Hosting a model is a fast, stable alternate method of communicating with your model 
- You are only charged $0.01 per request and not for the time the model actually runs. 
- You are not charged for the duration the model is awake. 
- You can always communicate remotely rather than locally and do not need to have any software running yourself for your models to be active.

⚠️  **Things to be aware of regarding Hosted Models:**
- You are charged $0.01 per request so if your webpage is public make sure you have functions to prevent repeated user requests in quick succession and hiding your API keys.
- Requires coding skills to set up.
- If you want to do near real-time interactions (for instance with a constant stream from a users webcam) perhaps Hosted Models are not ideal due to high costs and latency compared to a model running locally (or client-side in t[ensorflow.js](https://www.tensorflow.org/js)).


**Networking code examples**
GPT-2 basic (logs output text in the console): [https://editor.p5js.org/AndreasRef/sketches/SR6h8_CBR](https://editor.p5js.org/AndreasRef/sketches/SR6h8_CBR) 

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.23.21.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.23.21.png)

P5JS to StyleGAN with UI (buttons and sliders): [https://editor.p5js.org/AndreasRef/sketches/KcL6J6Mv3](https://editor.p5js.org/AndreasRef/sketches/KcL6J6Mv3) 

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-17_at_21.30.00.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-17_at_21.30.00.png)

P5JS to YOLOv4 (draws bounding boxes around detected objects to the P5 canvas): [https://editor.p5js.org/AndreasRef/sketches/HDzCCmYTv](https://editor.p5js.org/AndreasRef/sketches/HDzCCmYTv)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.25.14.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.25.14.png)

More options for connecting various other software to RunwayML can be found [here.](https://help.runwayml.com/hc/en-us/articles/4402110906259-Networking-Examples) It includes a comprehensive [Processing library](https://github.com/runwayml/processing-library) if you are more familiar with that coding environment.

For using Runway with Photoshop see [this tutorial](https://www.youtube.com/watch?v=Cq7NdUEbyYU).

**Further hosted model templates**

[Glitch: The friendly community where everyone builds the web](https://glitch.com/@daniel83693/runway-ml-templates)
This example uses Glitch to hide API keys by Daniel Shifmann

**Generative Boardgames**

[Generative Board Games](https://www.generativeboard.games/)

The website Generative BoardGames works by hosting two Runway Models (*StyleGAN* trained to generate game covers + *GPT-2* trained to generate game rules) and lets its visitors create new games directly in the browser. 

## 8) Work on an idea in groups

👉 Now you have time until 15:45 to explore an idea further.
You are free to do whatever you want, just as long as it includes one or more of the machine learning models available in RunwayML. It could be an artistic idea, an idea for a service, a part of a physical product, whatever you want!

Work in groups of 2 or 3 if possible, but no problem if you already have a group or want to work on something yourself. 

Depending on your interests, skills, the skill and and the available time you can try to do a small technical live-demo of the idea, where you host the model and build a small UI around it?

You can also just experiment with different inputs and outputs for different models to see what works and what does not work.

Another way of working on your idea might be to make a few slides in Keynote/Powerpoint presentation (or perhaps a small video) that explains and sells a bigger concept, where a model from RunwayML plays a key role.

Perhaps you are mainly interested in training a model (StyleGAN, GPT-2 or Yolo), in which case you can start to consider strategies and ressources for gathering data and see how far you can go?

## 9) Bonus material

### Sequel

Runway has a new experimental feature called **Sequel** which used Machine Learning to explore video editing methods such as masking/rotoscoping, colour correction and editing. 

[https://www.youtube.com/watch?v=loGc7DQL3YU&ab_channel=Runway](https://www.youtube.com/watch?v=loGc7DQL3YU&ab_channel=Runway)

Learn more here:

[Sequel](https://help.runwayml.com/hc/en-us/categories/1500001930562-Sequel)

## Connect Runway to other software (using the [desktop version of Runway](https://runwayml.com/download/))

### Connecting Runway to Processing

[https://www.youtube.com/watch?v=zGdOKaLOjck&t=3s](https://www.youtube.com/watch?v=zGdOKaLOjck&t=3s)

*Gene Kogan from Runway showing how to link RunwayML to Processing* 
Link to library: [https://github.com/runwayml/processing-library](https://github.com/runwayml/processing-library)

### Connecting Runway to P5.JS

Demonstrate how to connect Runway to a P5JS sketch running locally.
<video src='DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/zoom_Connecting_Runway_and_p5js.mp4' width=100%/>

The code mentioned is online at: [https://github.com/AndreasRef/p5js](https://github.com/AndreasRef/p5js)

### Network Examples

More options for connecting various other software to RunwayML can be found [here](https://learn.runwayml.com/#/networking/examples)

For using Runway with Photoshop see [this tutorial](https://www.youtube.com/watch?v=Cq7NdUEbyYU).

## Additional Runway video tutorials

[RunwayML](https://www.youtube.com/channel/UCUBqu_z5uP0AZhYtuyFZB3g/playlists)

[Model Training - YouTube](https://www.youtube.com/playlist?list=PLj598ZXODDO9fAdX7J5wt3pqYHUVCixMH)

[Intro to Machine Learning 🤖 with Gene Kogan - YouTube](https://www.youtube.com/playlist?list=PLj598ZXODDO_oWYAiO5c0Ac05IyrPUG8t)

## Other Runway Links

Official Runway learn section

[Learn how to use RunwayML](https://learn.runwayml.com/#/)

Runway Github

[Runway](https://github.com/runwayml)

[Running models for free with Docker on CPU](https://learn.runwayml.com/#/how-to/advanced-options?id=local-cpu) (or GPU if you are on Linux)

[Article: How Much Does RunwayML Cost?](https://support.runwayml.com/en/articles/3000086-how-much-does-runwayml-cost)

**Taught by Andreas Refsgaard**

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/VideoPainterGIF.gif](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/VideoPainterGIF.gif)

This page is a repost of https://www.notion.so/CREATE-ML-DAY-Runway-3a837d958a7d455a857577490a5c5762

[Website](http://andreasrefsgaard.dk/) / [Email](mailto:mail@andreasrefsgaard.dk) / [Twitter](https://twitter.com/AndreasRef) / [Instagram](https://www.instagram.com/andreasref/) / [GitHub](https://github.com/AndreasRef)

