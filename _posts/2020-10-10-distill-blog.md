---
layout: distill
title: Communicating with Interactive Articles
description: Examining the design of interactive articles by synthesizing theory from disciplines such as education, journalism, and visualization.
date: 2020-10-10
authors:
  - name: Fred Hohman
    url: "https://fredhohman.com"
    affiliations:
      name: Georgia Tech
      url: "https://www.gatech.edu/"
  - name: Matthew Conlen
    url: "https://mathisonian.com/"
    affiliations:
      name: University of Washington
      url: http://www.washington.edu/
  - name: Jeffrey Heer
    url: "https://homes.cs.washington.edu/~jheer/"
    affiliations:
      name: University of Washington
      url: http://www.washington.edu/
  - name: Duen Horng (Polo) Chau
    url: https://poloclub.github.io/polochau/
    affiliations:
      name: Georgia Tech
      url: "https://www.gatech.edu/"
bibliography: 2020-10-10-bibliography.bib
# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
includestyles: interactivestyles.css
---
<body>
  
  <d-article>
    <div id="mosaic" class="subgrid"></div>
    <d-contents id="toc"></d-contents>
    <div>
      <p id="introduction">
        Computing has changed how people communicate. The transmission of news, messages, and ideas is instant. Anyone's voice can be heard. In fact, access to digital communication technologies such as the Internet is so fundamental to daily life that their disruption by government is condemned by the United Nations Human Rights Council <d-cite key="un2017special"></d-cite>. But while the technology to distribute our ideas has grown in leaps and bounds, the interfaces have remained largely the same.
      </p>
      <p>
        Parallel to the development of the internet, researchers like Alan Kay and Douglas Engelbart worked to build technology that would empower individuals and enhance cognition. Kay imagined the Dynabook <d-cite key="kay2011personal"></d-cite> in the hands of children across the world. Engelbart, while best remembered for his "mother of all demos," was more interested in the ability of computation to augment human intellect <d-cite key="engelbart1962augmenting"></d-cite>. Neal Stephenson wrote speculative fiction that imagined interactive paper that could display videos and interfaces, and books that could teach and respond to their readers <d-cite key="stephenson1998diamond"></d-cite>.
      </p>
    </div>
    <p class="l-body-side">
      More recent designs (though still historical by personal computing standards) point to a future where computers are connected and assist people in decision-making and communicating using rich graphics and interactive user interfaces <d-cite key="apple1987knowledge"></d-cite>. While some technologies have seen mainstream adoption, such as Hypertext <d-cite key="nelson1967getting"></d-cite>, unfortunately, many others have not. The most popular publishing platforms, for example WordPress and Medium, choose to prioritize social features and ease-of-use while limiting the ability for authors to communicate using the dynamic features of the web.
    </p>
    <p>
      In the spirit of previous computer-assisted cognition technologies, a new type of computational communication medium has emerged that leverages active reading techniques to make ideas more accessible to a broad range of people. These interactive articles build on a long history, from Plato <d-cite key="ui1987plato"></d-cite> to PHeT <d-cite key="uc2002phet"></d-cite> to explorable explanations <d-cite key="victor2011explorable"></d-cite>. They have been shown to be more engaging, can help improve recall and learning, and attract broad readership and acclaim,<d-footnote>For example, some of <i>The New York Times</i> <d-cite key="katz2013all, branch2014snow"></d-cite> and <i>The Washington Post's</i> <d-cite key="stevens2020why"></d-cite> most read articles are interactive stories.</d-footnote> yet we do not know that much about them.
    </p>
    <p>
      In this work, for the the first time, we connect the dots between interactive articles such as those featured in this journal and publications like <i>The New York Times</i> and the techniques, theories, and empirical evaluations put forth by academic researchers across the fields of education, human-computer interaction, information visualization, and digital journalism. We show how digital designers are operationalizing these ideas to create interactive articles that help boost learning and engagement for their readers compared to static alternatives.
    </p>
    <div id="applications-tab" class="subgrid"></div>
    <div class="hidden-citations"><d-cite key="wattenberg2016attacking, petricek2017coeffects, dedomenico2019complexity, roston2015whats, aisch2015you, blood2017uber, comeau2018lets, vivo2015book, makler2017econgraphs, case2016build, atlas2018bycoffe, bostock2014better"></d-cite></div>
    <p>
      Today there is a growing excitement around the use of interactive articles for communication since they offer unique capabilities to help people learn and engage with complex ideas that traditional media lacks. After describing the affordances of interactive articles, we provide critical reflections from our own experience with open-source, interactive publishing at scale. We conclude with discussing practical challenges and open research directions for authoring, designing, and publishing interactive articles.
    </p>
    <p>
      This style of communication—and the platforms which support it—are still in their infancy. When choosing where to publish this work, we wanted the medium to reflect the message. Journals like <i>Distill</i> are not only pushing the boundaries of machine learning research but also offer a space to put forth new interfaces for dissemination. This work ties together the theory and practice of authoring and publishing interactive articles. It demonstrates the power that the medium has for providing new representations and interactions to make systems and ideas more accessible to broad audiences.
    </p>
    <h2 id="interactive-articles">Interactive Articles: Theory & Practice</h2>
    <p>
      Interactive articles draw from and connect many types of media, from static text and images to movies and animations. But in contrast to these existing forms, they also leverage interaction techniques such as details-on demand, belief elicitation, play, and models and simulations to enhance communication.
    </p>
    <p>
      While the space of possible designs is far too broad to be solved with one-size-fits-all guidelines, by connecting the techniques used in these articles back to underlying theories presented across disparate fields of research we provide a missing foundation for designers to use when considering the broad space of interactions that could be added to a born-digital article.
    </p>
    <p>
      We draw from a corpus of over sixty interactive articles to highlight the breadth of techniques available and analyze how their authors took advantage of a digital medium to improve the reading experience along one or more dimensions, for example, by reducing the overall cognitive load, instilling positive affect, or improving information recall.
    </p>
    <div id="example-table" class="subgrid"></div>
    <p>
      Because diverse communities create interactive content, this medium goes by many different names and has not yet settled on a standardized format nor definition.<d-footnote>However, one is taking shape<d-cite key="wiki2019explorable"></d-cite>.</d-footnote> Researchers have proposed artifacts such as explorable multiverse analyses <d-cite key="dragicevic2019increasing"></d-cite>, explainables <d-cite key="visxai"></d-cite>, and exploranations <d-cite key="ynnerman2018exploranation"></d-cite> to more effectively disseminate their work, communicate their results to the public, and remove research debt <d-cite key="olah2017research"></d-cite>. In newsrooms, data journalists, developers, and designers work together to make complex news and investigative reporting clear and engaging using interactive stories <d-cite key="lee2015more"></d-cite>. Educators use interactive textbooks as an alternative learning format to give students hands-on experience with learning material <d-cite key="sarama2009concrete"></d-cite>.
    </p>
    <p>
      Besides these groups, others such as academics, game developers, web developers, and designers blend editorial, design, and programming skills to create and publish explorable explanations <d-cite key="victor2011explorable"></d-cite>, interactive fiction <d-cite key="aarseth1997cybertext"></d-cite>, interactive non-fiction <d-cite key="sizemore2011interactive"></d-cite>, active essays <d-cite key="yamamiya2009active"></d-cite>, and interactive games <d-cite key="bogost2012newsgames"></d-cite>. While these all slightly differ in their technical approach and target audience, they all largely leverage the interactivity of the modern web.
    </p>
    <p>
      We focus on five unique affordances of interactive articles, listed below. In-line videos and example interactive graphics are presented alongside this discussion to demonstrate specific techniques.
    </p>
    <d-figure id="affordances" class="subgrid"></d-figure>
    <!-- <h4>Affordances</h4>
    <div id="affordances">
      <ul>
        <li class="blue-green">Connecting People and Data</li>
        <li class="red-orange">Making Systems Playful</li>
        <li class="soft-blue">Prompting Self-Reflection</li>
        <li class="argon">Personalization</li>
        <li class="sun">Reducing Cognitive Load</li>
      </ul>
    </div> -->
    <!-- <div id="message">
      We focus on five unique affordances of interactive articles, listed below. In-line videos and example interactive graphics are presented alongside this discussion to demonstrate specific techniques.
    </div> -->
    <h3 id="connecting-people-and-data" class="blue-green affordance">Connecting People and Data</h3>
    <p>
      As visual designers are well aware, and as journalism researchers have confirmed empirically <d-cite key="greussing2019simply"></d-cite>, an audience which finds content to be aesthetically pleasing is more likely to have a positive attitude towards it. This in turn means people will spend more time engaging with content and ultimately lead to improved learning outcomes. While engagement itself may not be an end goal of most research communications, the ability to influence both audience attitude and the amount of time that is spent is a useful lever to improve learning: we know from education research that both time spent <d-cite key="fredrick1980learning"></d-cite> and emotion <d-cite key="um2012emotional"></d-cite> are predictive of learning outcomes.
    </p>
    <p>
      Animations can also be used to improve engagement <d-cite key="amini2018hooked"></d-cite>. While there is debate amongst researchers if animations in general are able to more effectively convey the same information compared to a well designed static graphic <d-cite key="tversky2002animation"></d-cite>, animation has been shown to be effective specifically for communicating state transitions <d-cite key="heer2007animated"></d-cite>, uncertainty <d-cite key="hullman2015hypothetical"></d-cite>, causality <d-cite key="michotte1946perception"></d-cite>, and constructing narratives <d-cite key="thomas1995illusion"></d-cite>. A classic example of this is Muybridge's motion study <d-cite key="muybridge1882horse"></d-cite> that can be seen in <a class="figure-number-text" href="#horse">3</a>: while the series of still images may be more effective for answering specific questions like, "Does a horse lift all four of its feet off the ground when it runs?" watching the animation in slow motion gives the viewer a much more visceral sense of how it runs. A more modern example can be found in OpenAI's reporting on their hide-and-seek agents <d-cite key="baker2019emergent"></d-cite>. The animations here instantly give the viewer a sense of how the agents are operating in their environment.
    </p>
    <d-figure id="horse" class="subgrid"></d-figure>
    <p>
      Passively, animation can be used to add drama to a graphic displaying important information, but which readers may otherwise find dry. Scientific data which is inherently time varying may be shown using an animation to connect viewers more closely with the original data, as compared to seeing an abstracted static view. For example, Ed Hawkins designed "Climate Spirals," which shows the average global temperature change over time <d-cite key="hawkins2016climate"></d-cite>. This presentation of the data resonated with a large public audience, so much so that it was displayed at the opening ceremony at the 2016 Rio Olympics. In fact, many other climate change visualizations of this same dataset use animation to build suspense and highlight the recent spike in global temperatures <d-cite key="roston2015whats, randall2018earths, nasa2020global, popovich2017its"></d-cite>.
    </p>
    <p>
      <d-figure class="video-d-figure" id="badger2018extensive"></d-figure>
      By adding variation over time, authors have access to a new dimension to encode information and an even wider design space to work in. Consider the animated graphic in <i>The New York Times</i> story "Extensive Data Shows Punishing Reach of Racism for Black Boys," which shows economic outcomes for 10,000 men who grew up in rich families <d-cite key="badger2018extensive"></d-cite>. While there are many ways in which the same data could have been communicated more succinctly using a static visualization <d-cite key="cox2018disagreements"></d-cite>, by utilizing animation, it became possible for the authors to design a unit visualization in which each data point shown represented an individual, reminding readers that the data in this story was about real peoples' lives.
    </p>
    <p>
      Unit visualizations have also been used to evoke empathy in readers in other works covering grim topics such as gun deaths <d-cite key="casselman2016gun"></d-cite> and soldier deaths in war <d-cite key="halloran2015fallen"></d-cite>. Using person-shaped glyphs (as opposed to abstract symbols like circles or squares) has been shown not to produce additional empathic responses <d-cite key="boy2017showing"></d-cite>, but including actual photographs of people helps readers gain interest in, remember <d-cite key="borkin2015beyond, borkin2013makes"></d-cite>, and communicate complex phenomena <d-cite key="slobin2014what"></d-cite> using visualizations. Correll argues that much of the power of visualization comes from abstraction, but quantization stymies empathy <d-cite key="correll2019ethical"></d-cite>. He instead suggests anthropomorphizing data, borrowing journalistic and rhetoric techniques to create novel designs or interventions to foster empathy in readers when viewing visualizations <d-cite key="correll2019ethical, ivanov2019walk"></d-cite>.
    </p>
    <p>
      Regarding the format of interactive articles, an ongoing debate within the data journalism community has been whether articles which utilize scroll-based graphics (scrollytelling) are more effective than those which use step-based graphics (slideshows). McKenna et al. <d-cite key="mckenna2017visual"></d-cite> found that their study participants largely preferred content to be displayed with a step- or scroll-based navigation as opposed to traditional static articles, but did not find a significant difference in engagement between the two layouts. In related work, Zhi et al. found that performance on comprehension tasks was better in slideshow layouts than in vertical scroll-based layouts <d-cite key="zhi2019linking"></d-cite>. Both studies focused on people using desktop (rather than mobile) devices. More work is needed to evaluate the effectiveness of various layouts on mobile devices, however the interviews conducted by MckEnna et al. suggest that additional features, such as supporting navigation through swipe gestures, may be necessary to facilitate the mobile reading experience.
    </p>
    <div>
      <p>
        <d-figure class="video-d-figure" id="webworks2009cutthroat"></d-figure>
        The use of games to convey information has been explored in the domains of journalism <d-cite key="bogost2012newsgames"></d-cite> and education <d-cite key="squire2011video"></d-cite>. Designers of newsgames use them to help readers build empathy with their subject, for example in <i>The Financial Times's</i> "Uber Game" <d-cite key="blood2017uber"></d-cite>, and explain complex systems consisting of multiple parts, for example in <i>Wired's</i> "Cutthroat Capitalism: The Game" <d-cite key="webworks2009cutthroat"></d-cite>. In educational settings the use of games has been shown to motivate students while maintaining or improving learning outcomes <d-cite key="virvou2005combining"></d-cite>.
      </p>
      <p>
        As text moves away from author-guided narratives towards more reader-driven ones <d-cite key="segel2010narrative"></d-cite>, the reading experience becomes closer to that of playing a game. For example, the critically acclaimed explorable explanation "Parable of the Polygons" puts play at the center of the story, letting a reader manually run an algorithm that is later simulated in the article to demonstrate how a population of people with slight personal biases against diversity leads to social segregation <d-cite key="hart2016parable"></d-cite>.
      </p>
    </div>
    <h3 id="making-systems-playful" class="affordance red-orange">Making Systems Playful</h3>
    <p>
      Interactive articles utilize an underlying computational infrastructure, allowing authors editorial control over the computational processes happening on a page. This access to computation allows interactive articles to engage readers in an experience they could not have with traditional media. For example, in "Drawing Dynamic Visualizations", Victor demonstrates how an interactive visualization can allow readers to build an intuition about the behavior of a system, leading to a fundamentally different understanding of an underlying system compared to looking at a set of static equations <d-cite key="victor2013drawing"></d-cite>. These articles leverage active learning and reading, combined with critical thinking <d-cite key="adler2014read"></d-cite> to help diverse sets of people learn and explore using sandboxed models and simulations <d-cite key="victor2011explorable"></d-cite>.
    </p>
    <p>
      Complex systems often requires extensive setup to allow for properly study: conducting scientific experiments, training machine learning models, modeling social phenomenon, digesting advanced mathematics, and researching recent political events, all require the configuration of sophisticated software packages before a user can interact with a system at all, even just to tweak a single parameter. This barrier to entry can deter people from engaging with complex topics, or explicitly prevent people who do not have the necessary resources, for example, computer hardware for intense machine learning tasks. Interactive articles drastically lower these barriers.
    </p>
    <p>
      Science that utilizes physical and computational experiments requires systematically controlling and changing parameters to observe their effect on the modeled system. In research, dissemination is typically done through static documents, where various figures show and compare the effect of varying particular parameters. However, efforts have been made to leverage interactivity in academic publishing, summarized in <d-cite key="dragicevic2019increasing"></d-cite>. Reimagining the research paper with interactive graphics <d-cite key="victor2011scientific"></d-cite>, as exploranations <d-cite key="ynnerman2018exploranation"></d-cite>, or as explorable multiverse analyses <d-cite key="dragicevic2019increasing"></d-cite>, gives readers control over the reporting of the research findings and shows great promise in helping readers both digest new ideas and learn about existing fields that are built upon piles of research debt <d-cite key="olah2017research"></d-cite>.
    </p>
    <p>
      Beyond reporting statistics, interactive articles are extremely powerful when the studied systems can be modeled or simulated in real-time with interactive parameters without setup, e.g., in-browser sandboxes. Consider the example in <a class="figure-number-text" href="#simulation-vis">4</a> of a Boids simulation that models how birds flock together. Complex systems such as these have many different parameters that change the resulting simulation. These sandbox simulations allow readers to play with parameters to see their effect without worrying about technical overhead or other experimental consequences.
    </p>
    <d-figure id="simulation-vis" class="subgrid"></d-figure>
    <p>
      This is a standout design pattern within interactive articles, and many examples exist ranging in complexity. "How You Will Die" visually simulates the average life expectancy of different groups of people, where a reader can choose the gender, race, and age of a person <d-cite key="yau2016how"></d-cite>. "On Particle Physics" allows readers to experiment with accelerating different particles through electric and magnetic fields to build intuition behind electromagnetism foundations such as the Lorentz force and Maxwell's equations—the experiments backing these simulations cannot be done without multi-million dollar machinery <d-cite key="bianchi2019on"></d-cite>. "Should Prison Sentences Be Based On Crimes That Haven't Been Committed Yet?" shows the outcome of calculating risk assessments for recidivism where readers adjust the thresholds for determining who gets parole <d-cite key="barry2015should"></d-cite>.
    </p>
    <p>
      <d-figure class="video-d-figure" id="barron2018designing"></d-figure>
      The dissemination of modern machine learning techniques has been bolstered by interactive models and simulations. Three articles, "How to Use t-SNE Effectively" <d-cite key="wattenberg2016use"></d-cite>, "The Beginner's Guide to Dimensionality Reduction" <d-cite key="conlen2018dr"></d-cite>, and "Understanding UMAP" <d-cite key="coenen2019understanding"></d-cite> show the effect that hyperparameters and different dimensionality reduction techniques have on creating low dimensional embeddings of high-dimensional data. A popular approach is to demonstrate how machine learning models work with in-browser models <d-cite key="smilkov2019tensorflow"></d-cite>, for example, letting readers use their own video camera as input to an image classification model <d-cite key="barron2018designing"></d-cite> or handwriting as input to a stroke prediction model <d-cite key="carter2016experiments"></d-cite>. Other examples are aimed at technical readers who wish to learn about specific concepts within deep learning. Here, interfaces allow readers to choose model hyperparameters, datasets, and training procedures that, once selected, visualize the training process and model internals to inspect the effect of varying the model configuration <d-cite key="smilkov2017direct,kahng2018ganlab"></d-cite>.
    </p>
    <p>
      Interactive articles commonly communicate a single idea or concept using multiple representations. The same information represented in different forms can have different impact. For example, in mathematics often a single object has both an algebraic and a geometric representation. A clear example of this is the definition of a circle <d-cite key="carter2017using"></d-cite>. Both are useful, inform one another, and lead to different ways of thinking. Examples of interactive articles that demonstrate this include various media publications' political election coverage that break down the same outcome in multiple ways, for example, by voter demographics, geographical location, and historical perspective <d-cite key="fivethirtyeight2016who,katz2016will,wapo2016live"></d-cite>.
    </p>
    <p>
      The Multimedia Principle states that people learn better from words and pictures rather than words or pictures alone <d-cite key="mayer2002multimedia"></d-cite>, as people can process information through both a visual channel and auditory channel simultaneously. Popular video creators such as 3Blue1Brown <d-cite key="3blue1brown"></d-cite> and Primer <d-cite key="primer"></d-cite> exemplify these principles by using rich animation and simultaneous narration to break down complex topics. These videos additionally take advantage of the Redundancy Principle by including complementary information in the narration and in the graphics rather than repeating the same information in both channels <d-cite key="mayer2008revising"></d-cite>.
    </p>
    <div>
      <p>
        <d-figure class="video-d-figure" id="sanderson2018visualizing"></d-figure>
        While these videos are praised for their approachability and rich exposition, they are not interactive. One radical extension from traditional video content is also incorporating user input into the video while narration plays. A series of these interactive videos on "Visualizing Quaternions" lets a reader listen to narration of a live animation on screen, but at any time the viewer can take control of the video and manipulate the animation and graphics while simultaneously listening to the narration <d-cite key="sanderson2018visualizing"></d-cite>.
      </p>
      <p>
        Utilizing multiple representations allows a reader to see different abstractions of a single idea. Once these are familiar and known, an author can build interfaces from multiple representations and let readers interact with them simultaneously, ultimately leading to interactive experiences that demonstrate the power of computational communication mediums. Next, we discuss such experiences where interactive articles have transformed communication and learning by making live models and simulations of complex systems and phenomena accessible.
      </p>
    </div>
    <h3 id="prompting-self-reflection" class="affordance soft-blue">Prompting Self-Reflection</h3>
    <p>
      Asking a student to reflect on material that they are studying and explain it back to themselves—a learning technique called self-explanation—is known to have a positive impact on learning outcomes <d-cite key="chi1989self"></d-cite>. By generating explanations and refining them as new information is obtained, it is hypothesized that a student will be more engaged with the processes which they are studying <d-cite key="chi2000self"></d-cite>. When writing for an interactive environment, components can be included which prompt readers to make a prediction or reflection about the material and cause them to engage in self-explanation <d-cite key="kim2017explaining"></d-cite>.
    </p>
    <p>
      While these prompts may take the form of text entry or other standard input widgets, one of the most prominent examples of this technique used in practice comes from <i>The New York Times</i> "You Draw It" visualizations <d-cite key="aisch2015you, katz2017you, buchanan2017you"></d-cite>. In these visualizations, readers are prompted to complete a trendline on a chart, causing them to generate an explanation based on their current beliefs for why they think the trend may move in a certain direction. Only after readers make their prediction are they shown the actual data. Kim et al. showed that using visualizations as a prompt is an effective way to encourage readers to engage in self explanation and improve their recall of the information <d-cite key="kim2017explaining, nguyen2019they"></d-cite>. <a class="figure-number-text" href="#you-draw-it">5</a> shows one these visualizations for CO₂ emissions from burning fossil fuels. After clicking and dragging to guess the trend, your guess will be compared against the actual data.
    </p>
    <d-figure id="you-draw-it" class="subgrid"></d-figure>
    <div>
      <p>
        <d-figure class="video-d-figure" id="goldenberg2019you"></d-figure>
        In the case of "You Draw It," readers were also shown the predictions that others made, adding a social comparison element to the experience. This additional social information was not shown to necessarily be effective for improving recall <d-cite key="kim2017data"></d-cite>. However, one might hypothesize that this social aspect may have other benefits such as improving reader engagement, due to the popularity of recent visual stories using this technique, for example in <i>The Pudding's</i> "Gyllenhaal Experiment" <d-cite key="goldenberg2019you"></d-cite> and <i>Quartz's</i> "How do you draw a circle?" <d-cite key="ha2017you"></d-cite>.
      </p>
      <p>
        Prompting readers to remember previously presented material, for example through the use of quizzes, can be an effective way to improve their ability to recall it in the future <d-cite key="gates1922recitation"></d-cite>. This result from cognitive psychology, known as the testing effect <d-cite key="roediger2006power"></d-cite>, can be utilized by authors writing for an interactive medium <d-cite key="khanacademy"></d-cite>. While testing may call to mind stressful educational experiences for many, quizzes included in web articles can be low stakes: there is no need to record the results or grade readers. The effect is enhanced if feedback is given to the quiz-takers, for example by providing the correct answer after the user has recorded their response <d-cite key="bangert1991instructional"></d-cite>.
      </p>
      <p>
        <d-figure class="video-d-figure" id="case2014how"></d-figure>
        The benefits of the testing effect can be further enhanced if the testing is repeated over a period of time <d-cite key="karpicke2008critical"></d-cite>, assuming readers are willing to participate in the process. The idea of spaced repetition has been a popular foundation for memory building applications, for example in the Anki flash card system. More recently, authors have experimented with building spaced repetition directly into their web-based writing <d-cite key="case2014how, matuschak2019quantum"></d-cite>, giving motivated readers the opportunity to easily opt-in to a repeated testing program over the relevant material.
      </p>
    </div>
    <h3 id="personalizing-reading" class="affordance argon">Personalizing Reading</h3>
    <p>
      Content personalization—automatically modifying text and multimedia based on a reader's individual features or input (e.g., demographics or location)—is a technique that has been shown to increase engagement and learning within readers <d-cite key="cordova1996intrinsic"></d-cite> and support behavioral change <d-cite key="di2006authoring"></d-cite>. The PersaLog system gives developers tools to build personalized content and presents guidelines for personalization based on user research from practicing journalists <d-cite key="adar2017persalog"></d-cite>. Other work has shown that "personalized spatial analogies," presenting distance measurements in regions where readers are geographically familiar with, help people more concretely understand new distance measurements within news stories <d-cite key="kim2016generating"></d-cite>.
    </p>
    <p>
      <d-figure class="video-d-figure" id="popovich2018how"></d-figure>
      Personalization alone has also been used as the standout feature of multiple interactive articles. Both "How Much Hotter Is Your Hometown Than When You Were Born?" <d-cite key="popovich2018how"></d-cite> and "Human Terrain" <d-cite key="daniels2018human"></d-cite> use a reader's location to drive stories relating to climate change and population densities respectively. Other examples ask for explicit reader input, such as a story that visualizes a reader's net worth to challenge a reader's assumptions if they are wealthy or not (relative to the greater population) <d-cite key="quealy2019are"></d-cite>, or predicting a reader's political party affiliation <d-cite key="chinoy2010quiz"></d-cite>. Another example is the interactive scatterplot featured in "Find Out If Your Job Will Be Automated" <d-cite key="whitehouse2017find"></d-cite>. In this visualization, professions are plotted to determine their likelihood of being automated against their average annual wage. The article encourages readers to use the search bar to type in their own profession to highlight it against the others.
    </p>
    <p>
      An interactive medium has the potential to offer readers an experience other than static, linear text. Non-linear stories, where a reader can choose their own path through the content, have the potential to provide a more personalized experience and focus on areas of user interest <d-cite key="sizemore2011interactive"></d-cite>. For example, the <i>BBC</i> has used this technique in both online articles <d-cite key="lowther2017booze"></d-cite> and in a recent episode of "Click" <d-cite key="beckett2019click"></d-cite>, a technology focused news television program. Non-linear stories present challenges for authors, as they must consider the myriad possible paths through the content, and consider the different possible experiences that the audience would have when pursuing different branches.
    </p>
    <p>
      <d-figure class="video-d-figure" id="matuschak2019quantum"></d-figure>
      Another technique interactive articles often use is segmenting content into small pieces to be read in-between or alongside other graphics. While we have already discussed cognitive load theory, the Segmenting Theory, the idea that complex lessons are broken into smaller, bit-sized parts <d-cite key="clark2016learning"></d-cite>, also supports personalization within interactive articles. Providing a reader the ability to play, pause, and scrub content allows the reader to move at their own speed, comprehending the information at a speed that works best for them. Segmenting also engages a reader's essential processing without overloading their cognitive system <d-cite key="clark2016learning"></d-cite>.
    </p>
    <p>
      Multiple studies have been conducted showing that learners perform better when information is segmented, whether it be only within an animation <d-cite key="mayer2003multimedia"></d-cite> or within an interface with textual descriptions <d-cite key="mayer2002pictorial"></d-cite>. One excellent example of using segmentation and animation to personalize content delivery is "A Visual Introduction to Machine Learning," which introduces fundamental concepts within machine learning in bite-sized pieces, while transforming a single dataset into a trained machine learning model <d-cite key="yee2015visual"></d-cite>. Extending this idea, in "Quantum Country," an interactive textbook covering quantum computing, the authors implemented a user account system, allowing readers to save their position in the text and consume the content at their own pace <d-cite key="matuschak2019quantum"></d-cite>. This book further utilizes the interactive medium by utilizing spaced repetition that helps improve recall.
    </p>
    <h3 id="reducing-cognitive-load" class="affordance sun">Reducing Cognitive Load</h3>
    <p>
      Authors must calibrate the detail at which to discuss ideas and content to their readers expertise and interest to not overload them. When topics become multifaceted and complex, a balance must be struck between a high-level overview of a topic and its lower-level details. One interaction technique used to prevent a cognitive overload within a reader is "details-on-demand."
    </p>
    <p>
      Details-on-demand has become an ubiquitous design pattern. For example, modern operating systems offer to fetch dictionary definitions when a word is highlighted. When applied to visualization, this technique allows users to select parts of a dataset to be shown in more detail while maintaining a broad overview. This is particularly useful when a change of view is not required, so that users can inspect elements of interest on a point-by-point basis in the context of the whole <d-cite key="craft2005beyond"></d-cite>. Below we highlight areas where details-on-demand has been successfully applied to reduce the amount of information present within an interface at once.
    </p>
    <h4>Data Visualization</h4>
    <p>
      Details-on-demand is core to information visualization, and concludes the seminal Visual Information-Seeking Mantra: <i>"Overview first, zoom and filter, then details-on-demand"</i> <d-cite key="shneiderman1996eyes"></d-cite>. Successful visualizations not only provide the base representations and techniques for these three steps, but also bridge the gaps between them <d-cite key="keim2002information"></d-cite>. In practice, the solidified standard for details-on-demand in data visualization manifests as a tooltip, typically summoned on a cursor mouseover, that presents extra information in an overlay. Given that datasets often contain multiple attributes, tooltips can show the other attributes that are not currently encoded visually <d-cite key="ashkenas2014how"></d-cite>, for example, the map in <a class="figure-number-text" href="#details-vis">6</a> that shows where different types of birdsongs where recorded and what they sound like.
    </p>
    <d-figure id="details-vis" class="subgrid"></d-figure>
    <h4>Illustration</h4>
    <p>
      Details-on-demand is also used in illustrations, interactive textbooks, and museum exhibits, where highlighted segments of a figure can be selected to display additional information about the particular segment. For example, in "How does the eye work?" readers can select segments of an anatomical diagram of the human eye to learn more about specific regions, e.g., rods and cones <d-cite key="ala2018how"></d-cite>. Another example is "Earth Primer," an interactive textbook on tablets that allows readers to inspect the Earth's interior, surface, and biomes <d-cite key="gingold2015earth"></d-cite>. Each illustration contains segments the reader can tap to learn and explore in depth. <a class="figure-number-text" href="#details-illustration">7</a> demonstrates this by pointing out specific regions in machine-generated imagery <d-cite key="karras2018progressive,karras2019style"></d-cite> to help people spot fake images.
    </p>
    <d-figure id="details-illustration" class="subgrid"></d-figure>
    <h4>Mathematical Notation</h4>
    <p>
      Formal mathematics, a historically static medium, can benefit from details-on-demand, for example, to elucidate a reader with intuition about a particular algebraic term, present a geometric interpretation of an equation, or to help a reader retain high-level context while digesting technical details.<d-footnote>See this <a href="https://github.com/fredhohman/awesome-mathematical-notation-design">list of examples</a> that experiment with applying new design techniques to various mathematical notation.</d-footnote> For example, in "Why Momentum Really Works," equation layout is done using Gestalt principles plus annotation to help a reader easily identify specific terms<d-cite key="goh2017why"></d-cite>. In "Colorized Math Equations," the Fourier transform equation is presented in both mathematical notation and plain text, but the two are linked through a mouseover that highlights which term in the equation corresponds to which word in the text <d-cite key="azad2017colorized"></d-cite>. Another example that visualizes mathematics and computation is the "Image Kernels" tutorial where a reader can mouseover a real image and observe the effect and exact computation for applying a filter over the image <d-cite key="powell2015image"></d-cite>.
      <!-- This operation, called a convolution, is at the core of convolutional neural network architectures that have recently driven machine learning progress. -->
      Instead of writing down long arithmetic sums, the interface allows readers to quickly see the summation operation's terms and output. In <a class="figure-number-text" href="#details-math">8</a>, one of Maxwell's equations is shown. Click the two buttons to reveal, or remind yourself, what each notation mark and variable represent.
    </p>
    <d-figure id="details-math" class="subgrid"></d-figure>
    <h4>Text</h4>
    <p>
      While not as pervasive, text documents and other long-form textual mediums have also experimented with letting readers choose a variable level of detail to read. This idea was explored as early as the 1960s in StretchText, a hypertext feature that allows a reader to reveal a more descriptive or exhaustive explanation of something by expanding or contracting the content in place <d-cite key="nelson1967stretchtext"></d-cite>. The idea has resurfaced in more recent examples, including "On Variable Level-of-detail Documents" <d-cite key="beecroft2016on"></d-cite>, a PhD thesis turned interactive article <d-cite key="petricek2017coeffects"></d-cite>, and the call for proposals of <i>The Parametric Press</i> <d-cite key="cfp2018parametric"></d-cite>. One challenge that has limited this technique's adoption is the burden it places on authors to write multiple versions of their content. For example, drag the slider in <a class="figure-number-text" href="#details-text">9</a> to read descriptions of the Universal Approximation Theorem in increasing levels of detail. For other examples of details-on-demand for text, such as application in code documentation, see this small collection of examples <d-cite key="basques2018ui"></d-cite>.
    </p>
    <d-figure id="details-text" class="subgrid"></d-figure>
    <h4>Previewing Content</h4>
    <p>
      Details-on-demand can also be used as a method for previewing content without committing to another interaction or change of view. For example, when hovering over a hyperlink on Wikipedia, a preview card is shown that can contain an image and brief description; this gives readers a quick preview of the topic without clicking through and loading a new page <d-cite key="wikipedia2018preview"></d-cite>. This idea is also not new: work from human-computer interaction explored fluid links <d-cite key="zellweger1998fluid, zellweger2002reading"></d-cite> within hypertext that present information about a particular topic in a location that does not obscure the source material. Both older and modern preview techniques use perceptually-based animation and simple tooltips to ensure their interactions are natural and lightweight feeling to readers <d-cite key="zellweger1998fluid"></d-cite>.
    </p>
    <h2 id="challenges">Challenges for Authoring Interactives</h2>
    <p>
      <i>If interactive articles provide clear benefits over other mediums for communicating complex ideas, then why aren't they more prevalent? </i>
    </p>
    <p>
      Unfortunately, creating interactive articles today is difficult. Domain-specific diagrams, the main attraction of many interactive articles, must be individually designed and implemented, often from scratch. Interactions need to be intuitive and performant to achieve a nice reading experience. Needless to say, the text must also be well-written, and, ideally, seamlessly integrated with the graphics.
    </p>
    <p>
      The act of creating a successful interactive article is closer to building a website than writing a blog post, often taking significantly more time and effort than a static article, or even an academic publication.<d-footnote>As a proxy, see the number of commits on an <a href="https://github.com/distillpub/post--building-blocks">example <i>Distill</i> article</a>.</d-footnote> Most interactive articles are created using general purpose web-development frameworks which, while expressive, can be difficult to work with for authors who are not also web developers. Even for expert web developers, current tools offer lower levels of abstraction than may be desired to prototype and iterate on designs.
    </p>
    <p>
      While there are some tools that help with alleviating this problem <d-cite key="conlen2018idyll, apparatus, observable, case2017loopy, klokmose2015webstrates"></d-cite>, they are relatively immature and mainly help with reducing the necessary programming tedium. Tools like Idyll <d-cite key="conlen2018idyll"></d-cite> can help authors start writing quickly and even enable rapid iteration through various designs (for example, letting an author quickly compare between sequencing content using a "scroller" or "stepper" based layout). However, Idyll does not offer any design guidance, help authors think through where interactivity would be most effectively applied, nor highlight how their content could be improved to increase its readability and memorability. For example, Idyll encodes no knowledge of the positive impact of self-explanation, instead it requires authors to be familiar with this research and how to operationalize it.
    </p>
    <p>
      To design an interactive article successfully requires a diverse set of editorial, design, and programming skills. While some individuals are able to author these articles on their own, many interactive articles are created by a collective team consisting of multiple members with specialized skills, for example, data analysts, scripters, editors, journalists, graphic designers, and typesetters, as outlined in <d-cite key="lee2015more"></d-cite>. The current generation of authoring tools do not acknowledge this collaboration. For example, to edit only the text of <i>this article</i> requires one to clone its source code using git, install project-specific dependencies using a terminal, and be comfortable editing HTML files. All of this complexity is incidental to task of editing text.
    </p>
    <p>
      Publishing to the web brings its own challenges: while interactive articles are available to anyone with a browser, they are burdened by rapidly changing web technologies that could break interactive content after just a few years. For this reason, easy and accessible interactive article archival is important for authors to know their work can be confidently preserved indefinitely to support continued readership.<d-footnote>This challenge has been <a href="https://twitter.com/redblobgames/status/1168520452634865665">pointed out</a> by the community.</d-footnote> Authoring interactive articles also requires designing for a diverse set of devices, for example, ensuring bespoke content can be adapted for desktop and mobile screen sizes with varying connection speeds, since accessing interactive content demands more bandwidth.
    </p>
    <p>
      There are other non-technical limitations for publishing interactive articles. For example, in non-journalism domains, there is a mis-aligned incentive structure for authoring and publishing interactive content: why should a researcher spend time on an "extra" interactive exposition of their work when they could instead publish more papers, a metric by which their career depends on? While different groups of people seek to maximize their work's impact, legitimizing interactive artifacts requires buy-in from a collective of communities.
    </p>
    <p>
      Making interactive articles accessible to people with disabilities is an open challenge. The dynamic medium exacerbates this problem compared to traditional static writing, especially when articles combine multiple formats like audio, video, and text. Therefore, ensuring interactive articles are accessible to everyone will require alternative modes of presenting content (e.g. text-to-speech, video captioning, data physicalization, data sonification) and careful interaction design.
    </p>
    <p>
      It is also important to remember that not everything needs to be interactive. Authors should consider the audience and context of their work when deciding if use of interactivity would be valuable. In the worst case, interactivity may be distracting to readers or the functionality may go unused, the author having wasted their time implementing it. However, even in a domain where the potential communication improvement is incremental,<d-footnote>In reality, multimedia studies show large effect sizes for improvement of transfer learning in many cases, see Chapter 12 of<d-cite key="mayer2002multimedia"></d-cite>.</d-footnote> at scale (e.g., delivering via the web), interactive articles can still <a href="https://twitter.com/michael_nielsen/status/1031256363458916352?lang=en">have impact</a> <d-cite key="nielsen2015neural"></d-cite>.
    </p>
    <h2 id="critical-reflections">Critical Reflections</h2>
    <p>
      We write this article not as media theorists, but as practitioners, researchers, and tool builders. While it has never been easier for writers to share their ideas online, current publishing tools largely support only static authoring and do not take full advantage of the fact that the web is a dynamic medium. We want that to change, and we are not alone. Others from the explorable explanations community have identified design patterns that help share complex ideas through play <d-cite key="case2017how, case2018explorable, segel2010narrative, stolper2016emerging, mckenna2017visual"></d-cite>.
    </p>
    <p>
      To explore these ideas further, two of this work's authors created <i>The Parametric Press:</i> an annually published digital magazine that showcases the expository power that interactive dynamic media can have when effectively combined <d-cite key="parametric"></d-cite>. In late 2018, we invited writers to respond to a call for proposals for our first issue focusing on exploring scientific and technological phenomena that stand to shape society at large. We sought to cover topics that would benefit from using the interactive or otherwise dynamic capabilities of the web. Given the challenges of authoring interactive articles, we did not ask authors to submit fully developed pieces. Instead, we accepted idea submissions, and collaborated with the authors over the course of four months to develop the issue, offering technical, design, and editorial assistance collectively to the authors that lacked experience in one of these areas. For example, we helped a writer implement visualizations, a student frame a cohesive narrative, and a scientist recap history and disseminate to the public. Multiple views from one article are shown in <a class="figure-number-text" href="#parametric">10</a>.
    </p>
    <d-figure id="parametric" class="subgrid"></d-figure>
    <div class="hidden-citations"><d-cite key="feng2019myth"></d-cite></div>
    <p>
      We see <i>The Parametric Press</i> as a crucial connection between the often distinct worlds of research and practice. The project serves as a platform through which to operationalize the theories put forth by education, journalism, and HCI researchers. Tools like Idyll which are designed in a research setting need to be validated and tested to ensure that they are of practical use; <i>The Parametric Press</i> facilitates this by allowing us to study its use in a real-world setting, by authors who are personally motivated to complete their task of constructing a high-quality interactive article, and only have secondary concerns and care about the tooling being used, if at all.
    </p>
    <p>
      Through <i>The Parametric Press</i>, we saw the many challenges of authoring, designing, and publishing first hand, dually as researchers and practitioners. <a class="table-number-text" href="#research-x-practice-table">1</a> summarizes interactive communication opportunities from both research and practice.
    </p>
    <d-figure id="research-x-practice" class="subgrid"></d-figure>
    <p>
      As researchers we can treat the project as a series of case studies, where we were observers of the motivation and workflows which were used to craft the stories, from their initial conception to their publication. Motivation to contribute to the project varied by author. Where some authors had personal investment in an issue or dataset they wanted to highlight and raise awareness to broadly, others were drawn towards the medium, recognizing its potential but not having the expertise or support to communicate interactively. We also observed how research software packages like Apparatus <d-cite key="apparatus"></d-cite>, Idyll <d-cite key="conlen2018idyll"></d-cite>, and D3 <d-cite key="bostock2011d3"></d-cite> fit into the production of interactive articles, and how authors must combine these disparate tools to create an engaging experience for readers. In one article, "On Particle Physics," an author combined two tools in a way that allowed him to create and embed dynamic graphics directly into his article without writing any code beyond basic markup. One of the creators of Apparatus had not considered this type of integration before, and upon seeing the finished article <a href="https://twitter.com/qualmist/status/1128157840672051200?s=20">commented</a>, <i>"That's fantastic! Reading that article, I had no idea that Apparatus was used. This is a very exciting proof-of-concept for unconventional explorable-explanation workflows."</i>
    </p>
    <p>
      We were able to provide editorial guidance to the authors drawing on our knowledge of empirical studies done in the multimedia learning and information visualization communities to recommend graphical structures and page layouts, helping each article's message be communicated most effectively. One of the most exciting outcomes of the project is that we saw authors develop interactive communication skills like any other skill: through continued practice, feedback, and iteration. We also observed the challenges that are inherent in publishing dynamic content on the web and identified the need for improved tooling in this area, specifically around the archiving of interactive articles. Will an article's code still run a year from now? Ten years from now? To address interactive content archival, we set up a system to publish a digital archive of all of our articles at the time that they are first published to the site. At the top of each article on <i>The Parametric Press</i> is an archive link that allows readers to download a WARC (Web ARChive) file that can "played back" without requiring any web infrastructure. While our first iteration of the project relied on ad-hoc solutions to these problems, we hope to show how digital works such as ours can be published confidently knowing that they will be preserved indefinitely.
    </p>
    <p>
      As practitioners we pushed the boundaries of the current generation of tools designed to support the creation of interactive articles on the web. We found bugs and limitations in Idyll, a tool which was originally designed to support the creation of one-off articles that we used as a content management system to power an entire magazine issue. We were forced to write patches and plugins to work around the limitations and achieve our desired publication.<d-footnote>Many of these patches have since been merged to Idyll itself. This is the power of modular open-source tooling in action.</d-footnote> We were also forced to craft designs under a more realistic set of constraints than academics usually deal with: when creating a visualization it is not enough to choose the most effective visual encodings, the graphics also had to be aesthetically appealing, adhere to a house style, have minimal impact on page load time and runtime performance, be legible on both mobile and desktop devices, and not be overly burdensome to implement. Any extra hour spent implementing one graphic was an hour that was not spent improving some other part of the issue, such as the clarity of the text, or the overall site design.
    </p>
    <p>
      There are relatively few outlets that have the skills, technology, and desire to publish interactive articles. From its inception, one of the objectives of <i>The Parametric Press</i> is to showcase the new forms of media and publishing that are possible with tools available today, and inspire others to create their own dynamic writings. For example, Omar Shehata, the authors of <i>The Parametric Press</i> article <a href="https://parametric.press/issue-01/unraveling-the-jpeg/">"Unraveling the JPEG,"</a> told us he had wanted to write this interactive article for years yet never had the opportunity, support, or incentive to create it. His article drew wide interest and critical acclaim.
    </p>
    <p>
      We also wanted to take the opportunity as an independent publication to serve as a concrete example for others to follow, to represent a set of best practices for publishing interactive content. To that end, we made available all of the software that runs the site, including reusable components, custom data visualizations, and the publishing engine itself.
    </p>
    <h2 id="looking-forward">Looking Forward</h2>
    <p>
      A diverse community has emerged to meet these challenges, exploring and experimenting with what interactive articles could be. The <a href="https://explorabl.es/">Explorable Explanations community</a> is a "disorganized ‘movement’ of artists, coders & educators who want to reunite play and learning." Their online hub contains 170+ interactive articles on topics ranging from art, natural sciences, social sciences, journalism, and civics. The curious can also find tools, tutorials, and meta-discussion around learning, play, and representations. Explorables also hosted a mixed in-person and <a href="https://explorabl.es/jam/">online Jam</a>: a community-based sprint focused on creating new explorable explanations. <a class="figure-number-text" href="#jam">11</a> highlights a subset of the interactive articles created during the Jam.
    </p>
    <d-figure id="jam" class="subgrid"></d-figure>
    <p>
      Many interactive articles are self-published due to a lack of platforms that support interactive publishing. Creating more outlets that allow authors to publish interactive content will help promote their development and legitimization. The few existing examples, including newer journals such as <i>Distill</i>, academic workshops like VISxAI <d-cite key="visxai"></d-cite>, open-source publications like <i>The Parametric Press</i> <d-cite key="conlen2019launching"></d-cite>, and live programming notebooks like Observable <d-cite key="observable"></d-cite> help, but currently target a narrow group of authors, namely those who have programming skills. Such platforms should also provide clear paths to submission, quality and editorial standards, and authoring guidelines. For example, news outlets have clear instructions for pitching written pieces, yet this is under-developed for interactive articles. Lastly, there is little funding available to support the development of interactive articles and the tools that support them. Researchers do not receive grants to communicate their work, and practitioners outside of the largest news outlets are not able to afford the time and implementation investment. Providing more funding for enabling interactive articles incentivizes their creation and can contribute to a culture where readers expect digital communications to better utilize the dynamic medium.
    </p>
    <p>
      We have already discussed the breadth of skills required to author an interactive article. Can we help lower the barrier to entry? While there have been great, practical strides in this direction <d-cite key="conlen2018idyll, apparatus, observable, case2017loopy, klokmose2015webstrates"></d-cite>, there is still opportunity for creating tools to design, develop, and evaluate interactive articles in the wild. Specific features should include supporting mobile-friendly adaptations of interactive graphics (for example <d-cite key="hoffswell2020techniques, brehmer2019comparative, brehmer2018visualizing"></d-cite>), creating content for different platforms besides just the web, and tools that allow people to create interactive content without code.
    </p>
    <p>
      The usefulness of interactive articles is predicated on the assumption that these interactive articles actually facilitate communication and learning. There is limited empirical evaluation of the effectiveness of interactive articles. The problem is exacerbated by the fact that large publishers are unwilling to share internal metrics, and laboratory studies may not generalize to real world reading trends. <i>The New York Times</i> provided one of the few available data points, stating that only a fraction of readers interact with non-static content, and suggested that designers should move away from interactivity <d-cite key="tse2016why"></d-cite>. However, other research found that many readers, even those on mobile devices, are interested in utilizing interactivity when it is a core part of the article's message <d-cite key="conlen2019capture"></d-cite>. This statement from <i>The New York Times</i> has solidified as a rule-of-thumb for designers and many choose not to utilize interactivity because of it, despite follow-up discussion that contextualizes the original point and highlights scenarios where interactivity can be beneficial <d-cite key="aisch2017defense"></d-cite>. This means designers are potentially choosing a suboptimal presentation of their story due to this anecdote. More research is needed in order to identify the cases in which interactivity is worth the cost of creation.
    </p>
    <p>
      We believe in the power and untapped potential of interactive articles for sparking reader's desire to learn and making complex ideas accessible and understandable to all.
    </p>
  </d-article>
  <d-appendix>
    <h3>Acknowledgments</h3>
    <p>
      <!-- We are thankful to <span class="tk">{people}</span> for their helpful feedback on this work, as well as the reviewers. -->
      We are grateful to Arvind Satyanarayan for his early encouragement for pursuing this work, and Ludwig Schubert for his prompt help in fixing templating issues.
      We also thank <i>The Parametric Press</i> editors and authors for their continued support of the project, and to the Explorables community for their creativity and inspiration.
    </p>
    <p>
      This work was supported in part by a NASA Space Technology Fellowship.
    </p>
    <p>
      The birdsongs were provided by the users of <a href="https://www.xeno-canto.org/">https://www.xeno-canto.org/</a>.
    </p>
    <h3>Author Contributions</h3>
    <p>
      <b>Research:</b> After initial conversations over two years ago, Fred and Matthew jointly conducted the research bootstrapping early ideas from Matthew, including distilling literature, pulling published examples, and formulating the structure of the work.
    </p>
    <p>
      <b>Writing & Graphics:</b> Fred and Matthew also jointly wrote the text and collaborated on the design and implementation of the interactive graphics.
    </p>
    <d-footnote-list></d-footnote-list>
    <d-citation-list></d-citation-list>
  </d-appendix>
<script type="text/javascript" src="/assets/blog/20201010-interactive-paper/index.bundle.js"></script></body>