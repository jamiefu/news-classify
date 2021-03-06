========
DistilBERT
========

The DistilBERT model applies `huggingface's <https://huggingface.co/transformers/model_doc/gpt2.html>`_ implementation of 
`Victor Sanh, Lysandre Debut, Julien Chaumond and Thomas Wolf: “DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter” <https://arxiv.org/pdf/1910.01108.pdf>`_, 
a large transformer-based language model which embeds an entire document into a vector, 
usually to perform various natural language processing tasks. The model is trained using 
[HYPERPARAMETERS], and is saved on our server.

Once a new article is fed into the DistilBERT model, the article gets embedded through the saved model. The output is then run through a deep neural network to produce the predicted tags for the article. Due to the limits of time, our package does not support gettags at the moment.

32.8 KB of model files will be downloaded (not including huggingface's pretrained model), M MB of RAM will be used on average to run the model and the classification takes P ms.

getfeatures
-----------------

``class mitnewsclassify.distilbert.getfeatures(txt)``

Gets the output from the saved GPT2 model before it gets fed into the neural network to obtain a classification for a given article text.

**Parameters**
    * txt (``string``) - The article text

**Returns**
    * features (``Tensor[float32]``) - The 768 values

**Example**

.. code-block:: python

    >>> from mitnewsclassify import distilbert

    >>> distilbert.getfeatures("A destructive storm is rising from warm waters. Again. America and the world are getting more frequent and bigger multibillion dollar tropical catastrophes like Hurricane Laura, which is menacing the U.S. Gulf Coast, because of a combination of increased coastal development, natural climate cycles, reductions in air pollution and man-made climate change, experts say. The list of recent whoppers keeps growing: Harvey, Irma, Maria, Florence, Michael, Dorian. And hurricane experts have no doubt that Laura will be right there with them. It’s a mess at least partially of our own making, said Susan Cutter, director of the Hazards and Vulnerability Institute at the University of South Carolina. “We are seeing an increase of intensity of these phenomena because we as a society are fundamentally changing the Earth and at the same time we are moving to locations that are more hazardous,” Cutter said Wednesday. In the last three years, the United States has had seven hurricane disasters that each caused at least $1 billion in damage, totaling $335 billion. In all of the 1980s, there were six, and their damage totaled $38.2 billion, according to the National Oceanic and Atmospheric Administration. All those figures are adjusted for the cost of living. The Atlantic is increasingly spawning more major hurricanes, according to an Associated Press analysis of NOAA hurricane data since 1950. That designation refers to storms with at least 111-mile-per-hour (179-kilometer-per-hour) winds that are the ones that do the most damage. The Atlantic now averages three major hurricanes a year, based on a 30-year running average. In the 1980s and 1990s, it was two. The Atlantic’s Accumulated Cyclone Energy — a measurement that takes into account the number of storms, their strength and how long they last — is now 120 on a 30-year running average. Thirty years ago, it was in the 70s or 80s on average. Some people argue the increase is due to unchecked coastal development, while others will point to man-made climate change from the burning of coal, oil and gas. In fact, both are responsible, said former Federal Emergency Management Agency chief Craig Fugate. “There’s a lot of factors going on,” he said. When it comes to hurricane risk, a major factor is “the amount of stuff in the way of natural peril and the vulnerability of the stuff in the way,” said Mark Bove, a meteorologist who works for the insurance firm Munich Re U.S. One factor that increases the possibility that there will be “stuff in the way” of a major storm is that federal disaster policy and flood insurance subsidize and encourage people to rebuild in risky areas, Fugate said. After storms, communities “always say they are going to rise from the ashes,” and, too often, they build the same way in the same place for the same vulnerability and the same outcome, Fugate said. In addition, some places, like Houston, don’t limit development in areas that could serve as flood control zones if left empty and allow development that’s not disaster resilient, said Kathleen Tierney, former director of the Natural Hazards Center at Colorado University. Now add in the meteorology. Scientists agree that waters are warming, and that serves as hurricane fuel, said NOAA climate scientist Jim Kossin. A study by Kossin found that, once a storm formed, the chances of its attaining major storm status globally increased by 8% a decade since 1979. In the Atlantic, chances went up by 49% a decade. But scientists disagree on why waters are warming. They know climate change is a factor — but they say it’s not the biggest driver and disagree on what else may be behind it. Some argue it’s because of a 25- to 30-year natural global cycle that acts like a giant conveyor belt, carrying different levels of salt and temperature around the globe, including into the part of the tropical Atlantic off Africa where the worst hurricanes form, Colorado State University hurricane researcher Phil Klotzbach said. When the water in the northern Atlantic is extra warm, the water in those tropical hurricane breeding grounds is unusually hot, and the hurricane season is abnormally active, Klotzbach said. Such a busy period started in 1995 and might end soon as northern Atlantic waters shift to a cooler regime, he said. Klotzbach acknowledged that one problem with this theory is that the waters in the northern Atlantic have been unusually cool this summer, and still there have been lots of storms. It may have been a blip, he said. But MIT meteorology professor Kerry Emanuel says it’s because another counterintuitive factor is at play: There are more storms because of cleaner air. European air pollution cooled the area over Africa in the 1960s and 1970s and put more dust into the air — both of which tamped down on any hurricanes, he said. When the pollution eased, Africa got warmer, more storms developed, and that’s why it’s such a busy period, Emanuel said. While climate change is not the most important factor in warming waters, it contributes to creating more damaging storms in other ways, by causing a rising sea level that worsens storm surges and making storms move more slowly and produce more rain, scientists say. All of this means that we should get used to more catastrophic storms, according to Munich Re’s Bove. In addition, he said: “Climate change will be a bigger driver of losses in the future.”")
    tensor([[ 1.3516e-02, -6.6536e-02, -1.2586e-01,  7.8865e-02,  1.5436e-01,
            ...
            4.4400e-02,  1.0047e-01, -8.2776e-02]])
