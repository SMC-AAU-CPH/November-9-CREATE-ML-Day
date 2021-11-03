# Organizers
This workshop is organized by CREATE staff and students, and features Andreas Refsgaard.

Andreas Refsgaard is an artist and creative coder based in Copenhagen. He uses algorithms, coding and machine learning to explore the creative potentials of emerging digital technologies. He also offers workshops: https://andreasrefsgaard.dk/workshops/, in which, Andreas provides an introduction into how machine learning models can be productively integrated into existing workflows, integrated into websites and used for professional client projects. Through creative examples and hands-on exercises, he rolls out the many creative and technical possibilities machine learning brings to the field such as offering new and effective ways of prototyping and testing ideas. Andreas has previously taught workshops in machine learning and AI for creative technologists and developers at Facebook Reality Lab and at conferences like KIKK and Resonate. See also his new book in Danish: https://www.skabtafenkunstigintelligens.dk/ ![image](https://user-images.githubusercontent.com/1277203/140033209-0dd928c7-e5c4-4522-8d0c-75ecf322da0f.png).

Time	Activity
09:00	Welcome, Part I
12:15	Lunch
13:00	Part II
15:30	Coffee Break
15:45	Student Presentations
16:00	END of Workshop, mingling around small food
17:45   Live connection to the [TensorFlow Machine Learning Community Day](https://www.tensorflow.org/ml-community-day)
20:00   End of the official program

We provide a Danish template for the workshop below, the final language and sequence of activities will be determined by the participant profiles.

## DK Runway Workshop

### 0) Før vi starter

[RunwayML](https://runwayml.com/) - lav en (gratis) bruger og sørg for at du kan logge ind i Runway online. Alternativt kan du  download Runway i en desktop version her: [https://runwayml.com/download/](https://runwayml.com/download/)

### Dagens program **🗓**

- Forstå  RunwayML's interface
- Afprøv forskellige modeller
    - Image Analysis
    - Video Post Processing
    - Stylization
    - Text generation
    - Latent videos (GAN)
    - Animation
    - Experimental
    
    Træn dine egne modeller + indsaml data
    
    Host modeller online 
    
    Eksportering
    

### Forventninger + fejl 🐛

Du opfordres til at følge med i mit tempo og afprøve de modeller jeg afprøver, men du kan også bare læne dig tilbage og tage noter, hvis du lærer bedst sådan.

Hvis modeller giver fejl eller ikke vil køre efter et par minutter, kan du forsøge at genstarte dem (tryk på start/stop knappen) eller genloade siden i din browser.

Hav tålmodighed med modellerne, når du starter dem op. Flere af dem kan godt tage op til et par minutter, før de er loadet og kører.

Nogle gange vil din model muligvis ikke være færdig med at loade, mens jeg demonstrerer den, eller den kan vil måske loade meget hurtigere end min. I de fleste tilfælde har jeg linket til nogle alternative modeller, som du kan prøve at køre og eksperimentere med, så du ikke spilder tid på at vente på, at en model starter.

Fortæl mig i chatten, hvis jeg gennemgår ting for hurtigt eller for langsomt, og jeg vil forsøge at justere tempoet. Du er også velkommen til at beskrive specifikke problemer, du oplever, og jeg vil forsøge at hjælpe efter bedste evne.

### En bemærking om input-billeder 🖼 📷 🎞

Størstedelen af modellerne, vi arbejder med, bruger *image* som deres inputtype.
Jeg vil ofte demonstrere modellerne direkte med mit webcam, men du kan også uploade stillbilleder + videoer og bruge disse som dit input.

Undgå at bruge meget store billeder (større end 1280x720 px), når du  tester modeller, da dette vil øge loadtiden og i nogle tilfælde få modellerne til at gå crashe.

Hvis et bestemt billede ikke virker, kan du prøve at bruge et andet. Hold dig til *.jpg* og *.png* formater til billeder og .*mov* og *.mp4* til film.

Her er en lille folder med billeder du kan benytte, men det kan ofte være sjovere/mere relevant at finde og bruge dine egne billeder:

[https://drive.google.com/file/d/1WnPuf8kXMrRnLGfRhT20eVtj89L5j2fI/view?usp=sharing](https://drive.google.com/file/d/1WnPuf8kXMrRnLGfRhT20eVtj89L5j2fI/view?usp=sharing)

### 1) Image Analysis Models

**Pose Estimation:** [https://app.runwayml.com/models/runway/PoseNet](https://app.runwayml.com/models/runway/PoseNet)

Input type: Image 📷

Output Type: Array 📋 (List of x-and y-postions of pose landmarks + confidence)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/e9f5ab7a-6ada-4fc5-92dd-9457cd44f2e8.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/e9f5ab7a-6ada-4fc5-92dd-9457cd44f2e8.jpg)

**Facial Landmarks:** [https://app.runwayml.com/models/runway/Facial-Landmarks](https://app.runwayml.com/models/runway/Facial-Landmarks)

Input type: Image 📷

Output Type: Array 📋 (List of x-and y-postions of facial landmarks)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/0ea9d690-ebb8-4eb7-94e9-3015862b8c71.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/0ea9d690-ebb8-4eb7-94e9-3015862b8c71.jpg)

**YOLOv4**: [https://app.runwayml.com/models/runway/YOLOv4](https://app.runwayml.com/models/runway/YOLOv4)

Input type: Image 📷 

Output Type: Array 📋 (Name of detected object, bounding box (x, y, w & h), confidence score)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c60d71a6-cdc0-45db-bee5-5ac23a73f908.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c60d71a6-cdc0-45db-bee5-5ac23a73f908.jpg)

### 2) Stylization models

**Fast Style Transfer:** [https://app.runwayml.com/models/genekogan/Fast-Style-Transfer](https://app.runwayml.com/models/genekogan/Fast-Style-Transfer)

Input type: Content Image 🖼 (select style via checkpoint)

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/84f96d51-45a0-4f97-8354-087081e9f22a.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/84f96d51-45a0-4f97-8354-087081e9f22a.jpg)

**AdaIN Style Transfer:** [https://app.runwayml.com/models/reiinakano/AdaIN-Style-Transfer](https://app.runwayml.com/models/reiinakano/AdaIN-Style-Transfer)

Input type: Content image 📷 + Style image 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/11ee3da9-a4d0-415b-9f71-8cbf4a48267b.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/11ee3da9-a4d0-415b-9f71-8cbf4a48267b.jpg)

**Anime Filter:** [https://app.runwayml.com/models/runway/Anime-Filter](https://app.runwayml.com/models/runway/Anime-Filter)

Input type: Image 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/106fac3f-1c98-49cb-976a-47d4b8ccd75c.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/106fac3f-1c98-49cb-976a-47d4b8ccd75c.jpg)

### 3) Text generation models

**GPT-2:** [https://app.runwayml.com/models/runway/GPT-2](https://app.runwayml.com/models/runway/GPT-2)

Input type: Text (på engelsk, og jo mere tekst du selv skriver desto bedre!) ✍️

Output Type: Text ✍️

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/69053c32-a12d-4b9d-b5bf-f9f5f5eac133.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/69053c32-a12d-4b9d-b5bf-f9f5f5eac133.jpg)

**Øvelse: Skriv med GPT-2**
Kør GPT-2 modellen: [https://app.runwayml.com/models/runway/GPT-2](https://app.runwayml.com/models/runway/GPT-2)

****Giv GPT-2 nogle linjers tekst om et emne, og lad os se hvordan den skriver videre på din tekst! Et godt "prompt" indeholder tekst og struktur nok til tydeligt at styre GPT-2, så det er åbenlyst for den, hvilken slags tekst der er tale om. Tre ord eller en halv sætning er typisk ikke nok til at give meningsfulde outputs, så skriv mindst et par sætninger. Skriv på engelsk, den har ikke lært ordentligt dansk endnu.

Examples of input prompts:
*Here is how to make a traditional apple pie in 10 easy steps: 
1) Preheat the oven
2) Find a bowl
3)

eller

Andreas Refsgaard is a famous Danish football player who currently plays for Real Madrid. He began playing football when he was just 5 years old*

****Settings:
****Tilpas *Max Characters* slidereren i højre side, så du får mere output end kun 64 karakterer. 

****Load et større *checkpoint* (*Medium* eller *Large*) for de bedste resultater resultater. 

****Del dine resultater:
****Del dine bedste resultater i chatten på Zoom

### 4) Latent Video Models (GANs)

Input type: Vector position ⌖

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/219c1c1e-9b86-4759-bf77-e20674bf234d.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/219c1c1e-9b86-4759-bf77-e20674bf234d.jpg)

**Øvelser: Faces vs Dogs - betydningen af "ensartet træningsdata"**
Kør ****StyleGAN modellen [https://app.runwayml.com/models/runway/StyleGAN](https://app.runwayml.com/models/runway/StyleGAN) med checkpointet "Flickr Faces HQ" valgt. Sammenlign billederne med den samme model med  "Dogs" checkpointet valgt.

Tips:

Hvis din model kører, men du ikke ser nogen billeder, skal du klikke på knappen "Vector" øverst på skærmen.

Træn med musen, eller klik på knappen "regenerer" for at udforske forskellige outputs.

Vis dine resultater:
****Del the sjoveste ansigt🤪  og den mærkeligste hund du kan finde i [dette dokument](https://docs.google.com/document/d/1UKdDCbGx-7H4QxYEvf0DWwqUy73zYku-2JASe4Fm1Wg/edit).

### 5) Experimental models (hvis vi har tid 🕰)

**ArtLine**: [https://app.runwayml.com/models/akhaliq/ArtLine](https://app.runwayml.com/models/akhaliq/ArtLine)
Input type: Image 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/208e15b8-c68c-4ed0-b7a7-677f55b59165.jpeg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/208e15b8-c68c-4ed0-b7a7-677f55b59165.jpeg)

**Spade Landscapes:** [https://app.runwayml.com/models/genekogan/SPADE-Landscapes](https://app.runwayml.com/models/genekogan/SPADE-Landscapes)

Input type: Segmentation Image (with specific colors for each category) 🎨

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/eb491254-74b9-48b9-9aa3-9c937a9e3322.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/eb491254-74b9-48b9-9aa3-9c937a9e3322.jpg)

**Style Space Face (SLOW!):** [https://app.runwayml.com/models/justinpinkney/Style-space-face-editing](https://app.runwayml.com/models/justinpinkney/Style-space-face-editing)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/f84b9f80-e566-4016-ba5f-e0a45c25f1c9.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/f84b9f80-e566-4016-ba5f-e0a45c25f1c9.jpg)

Input type: Image containing face (with/without changes) 🖼

Output Type: Image 🖼

### 6) Video Post Processing Models (hvis vi har tid 🕰)

**Colorization:** [https://app.runwayml.com/models/reiinakano/Colorization](https://app.runwayml.com/models/reiinakano/Colorization)

Input type: Image (black and white) 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/4132c5f1-07ee-43f6-964c-cec114024b62.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/4132c5f1-07ee-43f6-964c-cec114024b62.jpg)

**Depth Maps:** [https://app.runwayml.com/models/akhaliq/Depth-Maps](https://app.runwayml.com/models/akhaliq/Depth-Maps)

Input type: Image 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/6eff2081-2f44-429c-9cdd-68c81d9bbb57.jpeg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/6eff2081-2f44-429c-9cdd-68c81d9bbb57.jpeg)

**U2-Net:** [https://app.runwayml.com/models/anastasis/U-2-Net](https://app.runwayml.com/models/anastasis/U-2-Net)

Input type: Image 🖼

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/1eb8e7d3-4326-40d6-aed4-fadb9dd328e6.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/1eb8e7d3-4326-40d6-aed4-fadb9dd328e6.png)

**Person Segmentation:** [https://app.runwayml.com/models/runway/Person-Segmentation](https://app.runwayml.com/models/runway/Person-Segmentation) 

Input type: Image 🖼

Output Type: Image 🖼

![859d8ec3-3cbc-4ffa-9654-e824459ed741.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/859d8ec3-3cbc-4ffa-9654-e824459ed741.png)

### 7) Animation models (hvis vi har tid 🕰)

**Fast Bi-layer Neural Synthesis:** [https://app.runwayml.com/models/akhaliq/bilayer-model](https://app.runwayml.com/models/akhaliq/bilayer-model)

Input type: Source Image/Video (containing face)👤+ Target Image (containing face) 👤

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c8655aea-52fd-44b8-b467-ab66b4def566-min.gif](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/c8655aea-52fd-44b8-b467-ab66b4def566-min.gif)

**First-Order-Motion-Model:** [https://app.runwayml.com/models/runway/First-Order-Motion-Model](https://app.runwayml.com/models/runway/First-Order-Motion-Model)

Input type: Driving Image/Video (containing face)👤+ Source Image (containing face) 👤

Output Type: Image 🖼

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/9a9b49ea-1345-4529-b540-31b0cada0afc.gif](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/9a9b49ea-1345-4529-b540-31b0cada0afc.gif)

**Øvelse: Time to explore (hvis vi har tid 🕰)**

Afprøv nogle af de modeller, du endnu ikke har prøvet, og del sjove outputs med resten af deltagerne. 

Benyt chatten til at stille spørgsmål hvis du sidder fast eller noget ikke virker. Men husk at have tålmodighed med modellerne, de kan godt tage adskillige minutter før de er loadet.

Del dine resultater:
****Del de sjoveste outputs i [dette dokument](https://docs.google.com/document/d/1UKdDCbGx-7H4QxYEvf0DWwqUy73zYku-2JASe4Fm1Wg/edit).

## 8) Træn selv modeller i Runway

[Model Training | Runway](https://runwayml.com/training/)

[https://www.youtube.com/watch?v=1shE4Mjie1I&ab_channel=RunwayML](https://www.youtube.com/watch?v=1shE4Mjie1I&ab_channel=RunwayML)

*Gene Kogan from Runway explaining how to train a StyleGAN model*

**Tips til at træne StyleGAN**

- Jo flere billeder, desto bedre resultater. Prøv at få fat på mellem 500 og 5.000 billeder (men ideelt set endnu mere! Jeg tror max er 25.000).
- StyleGAN genererer 1x1 -stilbilleder som output (f.eks. 1024x1024 px), så tænk på at beskære dine data i et 1x1 -format, før du sender dem til Runway eller via funktionen Dataset Preprocessing i RunwayML.
- Forsøg at indsamle billeder i høj opløsning (ideelt omkring 1024 px x 1024 px, men realistisk set måske 500 x 500 pixels).
- Hvis en GAN-model skal producere "realistiske" billeder, skal du prøve at træne det med ensartede billeder af lignende objekter, lignende vinkler, ensartet lys, ensartede beskæringer, baggrunde osv. Ellers får du mareridtskatte (hvilket også er sejt, men måske ikke hvad du vil?).

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-15_at_21.54.11.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-15_at_21.54.11.png)

**Links til at hjælpe med at indsamle data**

- [Kaggle](https://www.kaggle.com/) - Dataset and ML community and database (eg. images of [Pokémons](https://www.kaggle.com/kvpratama/pokemon-images-dataset))
- [Google Data Set Search](https://datasetsearch.research.google.com/) - Search for datasets
- [Web Scraping](https://scrapism.lav.io/) - Sam Lavignes web scraping guide (python, requires code knowledge)
- [Image Downloader](https://chrome.google.com/webstore/detail/image-downloader/cnpniohnfphhjihaiiggeabnkjhpaldj) - Google Chrome Plugin to download all visible images on a website
- [Pindown Chrome Extension](https://chrome.google.com/webstore/detail/pindown/flieckppkcgagklbnnhnkkeladdghogp?hl=en) (costs a bit to use, but is perfect for instagram or Pinterest) - [Youtube Tutorial](https://www.youtube.com/watch?v=BwMk1Ik7aCM&ab_channel=ArtificialImages)
- [Splitting Video into individual image frames](https://youtu.be/ck11jOVYlIw) - Derrick Schultz video tutorial
- [Project Gutenberg](https://www.gutenberg.org/) - 60.000+ free eBooks (good for training GPT-2)

**Pre-processing data**

[Runway Tool Tips: Dataset Preprocessing](https://www.youtube.com/watch?v=dwlB5kG2CaQ&ab_channel=RunwayML)

## 9) Træn andre typer af modeller i Runway

### Træn en Object detection model med YOLO-v4

[https://www.youtube.com/watch?v=XWyKkFj54aA](https://www.youtube.com/watch?v=XWyKkFj54aA)

[Derrick Schultz](https://artificial-images.com/) forklarer hvordan man træner en *YOLO-v4 Object Detection Model i Runway* 
(Jeg anbefaler i øvrigt hans [videos](https://www.youtube.com/channel/UCaZuPdmZ380SFUMKHVsv_AA),  og indhold på [Patreon](https://www.patreon.com/bustbright) hvis du er interesseret i Machine Learning Art)

### Træn en model der generer tekst med GPT-2

Walkthrough of training GPT-2 using a corpus of 

[https://www.youtube.com/watch?v=-v5StaeOisM&t=5s&ab_channel=RunwayML](https://www.youtube.com/watch?v=-v5StaeOisM&t=5s&ab_channel=RunwayML)

*Gene Kogan fra Runway forklarer, hvordan man træner en GPT-2 tekst model med sci-fi👽 tekster fra Kaggle*

# Bonusmateriale (på engelsk)

## 10) Hosted Models with Runway

Hosted Models are a new feature to RunwayML. It is an alternative to connecting via HTTP or OSC (see the P5JS and Processing examples below). It provides an 'always on' approach to accessing your model and you then query the information when by waking up the model. 

[hosted model reference page](https://learn.runwayml.com/#/how-to/hosted-models) 

**Positives about Hosted Models:**
- It is a fast, stable method of communicating with your model 
- You are only charged $0.01 per request and not for the time the model actually runs. 
- You are not charged for the duration the model is awake. 
- You can always communicate remotely rather than locally and do not need to have any software running yourself for your models to be active. 

 **Things to be aware of regarding Hosted Models:**
- You are charged $0.01 per request so if your webpage is public make sure you have functions to prevent repeated user requests in quick succession and hiding your API keys.
- Requires coding skills to set up.
- If you want to do near real-time interactions (for instance with a constant stream from a users webcam) perhaps Hosted Models are not ideal due to high costs and latency compared to a model running locally (or client-side in t[ensorflow.js](https://www.tensorflow.org/js)).

**Networking code examples**
GPT-2 basic (logs output text in the console): [https://editor.p5js.org/AndreasRef/sketches/SR6h8_CBR](https://editor.p5js.org/AndreasRef/sketches/SR6h8_CBR) 

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.23.21.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.23.21.png)

StyleGAN with UI (buttons and sliders): [https://editor.p5js.org/AndreasRef/sketches/KcL6J6Mv3](https://editor.p5js.org/AndreasRef/sketches/KcL6J6Mv3) 

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-17_at_21.30.00.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2020-11-17_at_21.30.00.png)

YOLOv4 with p5js drawings (draw bounding boxes around detected objects): [https://editor.p5js.org/AndreasRef/sketches/HDzCCmYTv](https://editor.p5js.org/AndreasRef/sketches/HDzCCmYTv)

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.25.14.png](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_13.25.14.png)

**More templates for RunwayML hosted models using Glitch to hide API keys by Daniel Shiffmann**

[Glitch: The friendly community where everyone builds the web](https://glitch.com/@daniel83693/runway-ml-templates)

**Generative Boardgames**

[Generative Board Games](https://www.generativeboard.games/)

The website Generative BoardGames works by hosting two Runway Models (*StyleGAN* trained to generate game covers + *GPT-2* trained to generate game rules) and lets its visitors create new games directly in the browser. 

[Making Generative Board Games](https://medium.com/better-programming/making-generative-board-games-1778d6267d8b)

Florian Porada from Generative Boardgames talks through the design process of making Generative Boardgames as well as the technical stack behind it.

[Creating a custom GPT-2 Slack Bot with RunwayML's hosted models.](https://medium.com/runwayml/creating-a-custom-gpt-2-slack-bot-with-runwaymls-hosted-models-c639fe135379)

Tutorial connecting to Glitch and Slack AP to make a chatbot by Cristobal Valenzuela from Runway

**Exercise: Hosted Models Concept Brainstorm**

Try to come up with an idea for a website/service/app/experience that uses one or more hosted models from RunwayML
Give the project a title, write which model(s) you imagine using, and a short description of your idea. They can be useful, funny, weird, artistic, whatever you like!
****
Post your ideas:
****Post your idea in in this Google Doc: 
[https://docs.google.com/document/d/1psaGcarfL6nWNoBQMI2RWp7AJv1k-6ptzMNuJHOMZdI/edit](https://docs.google.com/document/d/1V4TnV4inzBW3cpKIksYjYCGoqpMLYXMLAQl99Vm6URA/edit?usp=sharing) 

## 11) Exporting assets

Walkthrough of exporting videos from GAN models + experimental models

Mention exporting CSV data from image analysis models (via Desktop version)

## 12) Connect Runway to other software

### Connecting Runway to Processing

[https://www.youtube.com/watch?v=zGdOKaLOjck&t=3s](https://www.youtube.com/watch?v=zGdOKaLOjck&t=3s)

*Gene Kogan from Runway showing how to link RunwayML to Processing* 
Link to library: [https://github.com/runwayml/processing-library](https://github.com/runwayml/processing-library)

### Connecting Runway to P5.JS

Demonstrate how to connect Runway to a P5JS sketch running locally.

[DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/zoom_Connecting_Runway_and_p5js.mp4](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/zoom_Connecting_Runway_and_p5js.mp4)

The code mentioned is online at: [https://github.com/AndreasRef/p5js](https://github.com/AndreasRef/p5js)

### Network Examples

More options for connecting various other software to RunwayML can be found [here](https://learn.runwayml.com/#/networking/examples)

For using Runway with Photoshop see [this tutorial](https://www.youtube.com/watch?v=Cq7NdUEbyYU).

## 13) Green Screen

Walkthrough of the new Green Screen tool

![DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_16.23.51.jpg](DK%20Runway%20Workshop%202%20timer%20af18eb2c032b4f5bbf43eac0be4c2007/Screenshot_2021-01-19_at_16.23.51.jpg)

[https://www.youtube.com/watch?v=-2UBoklCtjk&ab_channel=Runway](https://www.youtube.com/watch?v=-2UBoklCtjk&ab_channel=Runway)

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

[Website](http://andreasrefsgaard.dk/) / [Email](mailto:mail@andreasrefsgaard.dk) / [Twitter](https://twitter.com/AndreasRef) / [Instagram](https://www.instagram.com/andreasref/) / [GitHub](https://github.com/AndreasRef)

### Having issues running Runway in the browser😬?

Make sure you are running Runway in [Google Chrome](https://www.google.com/chrome/)

[Allow camera and microphone in Google Chrome](https://support.google.com/chrome/answer/2693767?co=GENIE.Platform%3DDesktop&hl=en&oco=0)

Mac: [Allow camera on MacOSX in System Preferences](https://support.apple.com/guide/mac-help/control-access-to-your-camera-on-mac-mchlf6d108da/mac)

Windows: Webcam access on Windows 10: Select Start > Settings > Privacy > Camera. Set "Let apps use my camera" to "On". Make sure Chrome has access to use the camera. Make sure you are not using your camera in any other application.

Turn off your webcam in all other applications (+ Zoom) if you are on Windows.

Webcam not working? Try uninstalling any software that messes with your webcam settings.
