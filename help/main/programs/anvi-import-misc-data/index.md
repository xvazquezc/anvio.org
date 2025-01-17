---
layout: program
title: anvi-import-misc-data
excerpt: An anvi'o program. Populate additional data or order tables in pan or profile databases for items and layers, OR additional data in contigs databases for nucleotides and amino acids (the Swiss army knife-level serious stuff).
categories: [anvio]
comments: false
redirect_from: /m/anvi-import-misc-data
image:
  featurerelative: ../../../images/header.png
  display: true
---

Populate additional data or order tables in pan or profile databases for items and layers, OR additional data in contigs databases for nucleotides and amino acids (the Swiss army knife-level serious stuff).

🔙 **[To the main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Authors

<div class="anvio-person"><div class="anvio-person-info"><div class="anvio-person-photo"><img class="anvio-person-photo-img" src="../../images/authors/meren.jpg" /></div><div class="anvio-person-info-box"><a href="/people/meren" target="_blank"><span class="anvio-person-name">A. Murat Eren (Meren)</span></a><div class="anvio-person-social-box"><a href="http://merenlab.org" class="person-social" target="_blank"><i class="fa fa-fw fa-home"></i>Web</a><a href="mailto:a.murat.eren@gmail.com" class="person-social" target="_blank"><i class="fa fa-fw fa-envelope-square"></i>Email</a><a href="http://twitter.com/merenbey" class="person-social" target="_blank"><i class="fa fa-fw fa-twitter-square"></i>Twitter</a><a href="http://github.com/meren" class="person-social" target="_blank"><i class="fa fa-fw fa-github"></i>Github</a></div></div></div></div>

<div class="anvio-person"><div class="anvio-person-info"><div class="anvio-person-photo"><img class="anvio-person-photo-img" src="../../images/authors/ekiefl.jpg" /></div><div class="anvio-person-info-box"><a href="/people/ekiefl" target="_blank"><span class="anvio-person-name">Evan Kiefl</span></a><div class="anvio-person-social-box"><a href="http://ekiefl.github.io" class="person-social" target="_blank"><i class="fa fa-fw fa-home"></i>Web</a><a href="mailto:kiefl.evan@gmail.com" class="person-social" target="_blank"><i class="fa fa-fw fa-envelope-square"></i>Email</a><a href="http://twitter.com/evankiefl" class="person-social" target="_blank"><i class="fa fa-fw fa-twitter-square"></i>Twitter</a><a href="http://github.com/ekiefl" class="person-social" target="_blank"><i class="fa fa-fw fa-github"></i>Github</a></div></div></div></div>



## Can consume


<p style="text-align: left" markdown="1"><span class="artifact-r">[pan-db](../../artifacts/pan-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[profile-db](../../artifacts/profile-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[misc-data-items-txt](../../artifacts/misc-data-items-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[dendrogram](../../artifacts/dendrogram) <img src="../../images/icons/NEWICK.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[phylogeny](../../artifacts/phylogeny) <img src="../../images/icons/NEWICK.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[misc-data-layers-txt](../../artifacts/misc-data-layers-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[misc-data-layer-orders-txt](../../artifacts/misc-data-layer-orders-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[misc-data-nucleotides-txt](../../artifacts/misc-data-nucleotides-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[misc-data-amino-acids-txt](../../artifacts/misc-data-amino-acids-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span></p>


## Can provide


<p style="text-align: left" markdown="1"><span class="artifact-p">[misc-data-items](../../artifacts/misc-data-items) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[misc-data-layers](../../artifacts/misc-data-layers) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[misc-data-layer-orders](../../artifacts/misc-data-layer-orders) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[misc-data-nucleotides](../../artifacts/misc-data-nucleotides) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[misc-data-amino-acids](../../artifacts/misc-data-amino-acids) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span></p>


## Usage


This program lets you **bring additional information into your anvi'o databases** that will appear when you run <span class="artifact-p">[anvi-interactive](/help/main/programs/anvi-interactive)</span>.   

With this, you can 
- **bring additional data about your items or layers into the anvi'o interactive interface** by putting it into a <span class="artifact-n">[pan-db](/help/main/artifacts/pan-db)</span> or <span class="artifact-n">[profile-db](/help/main/artifacts/profile-db)</span>
- **bring additional data about your nucleotides/amino acids** into a <span class="artifact-n">[contigs-db](/help/main/artifacts/contigs-db)</span> 

You also have the option to associate keys with only a specific data group, or transpose the input before processing (in case you misformatted it). 

If you no longer want to see data you've added with this function, you can export it as the original text file with <span class="artifact-p">[anvi-export-misc-data](/help/main/programs/anvi-export-misc-data)</span> and delete it from the database with <span class="artifact-p">[anvi-delete-misc-data](/help/main/programs/anvi-delete-misc-data)</span>.

## Items, Layers, and the Interactive Interface 

{:.notice}
This process, as well as the definition of an item and a layer, are described in more detail in [this blog post](http://merenlab.org/2017/12/11/additional-data-tables). 

Basically, you can add additional information to the interactive interface by running this program on the database you want to display and a text file containing your information. You can do this with three types of data (see their individual pages for more information on each): 

1. <span class="artifact-n">[misc-data-items](/help/main/artifacts/misc-data-items)</span> by providing a <span class="artifact-n">[misc-data-items-txt](/help/main/artifacts/misc-data-items-txt)</span>. This contains information about *each of your items in the central tree* (whether those are contigs, bins, or genes), and will appear as **additional concentric circles** when you run <span class="artifact-p">[anvi-interactive](/help/main/programs/anvi-interactive)</span>. 

    <div class="codeblock" markdown="1">
    anvi&#45;import&#45;misc&#45;data &#45;p <span class="artifact&#45;n">[profile&#45;db](/help/main/artifacts/profile&#45;db)</span> \
                          &#45;t items \
                          <span class="artifact&#45;n">[misc&#45;data&#45;items&#45;txt](/help/main/artifacts/misc&#45;data&#45;items&#45;txt)</span> 
    </div>
        
2. <span class="artifact-n">[misc-data-layers](/help/main/artifacts/misc-data-layers)</span> by providing a <span class="artifact-n">[misc-data-layers-txt](/help/main/artifacts/misc-data-layers-txt)</span>. This contains information about *each layer (or concentric circle) of the interface* (which usually correspond to your samples), and will appear as **graphs in line with your circles of data** (on the right, similar to how to the titles of each layer are displayed at the top) when you run <span class="artifact-p">[anvi-interactive](/help/main/programs/anvi-interactive)</span>. 

    <div class="codeblock" markdown="1">
    anvi&#45;import&#45;misc&#45;data &#45;p <span class="artifact&#45;n">[pan&#45;db](/help/main/artifacts/pan&#45;db)</span> \
                          &#45;t layers \
                          <span class="artifact&#45;n">[misc&#45;data&#45;layers&#45;txt](/help/main/artifacts/misc&#45;data&#45;layers&#45;txt)</span>                               
    </div>

3. <span class="artifact-n">[misc-data-layer-orders](/help/main/artifacts/misc-data-layer-orders)</span> by providing a <span class="artifact-n">[misc-data-layer-orders-txt](/help/main/artifacts/misc-data-layer-orders-txt)</span>. This contains information about *what order you want the concentric circles to be displayed in*  (which usually correspond to your samples), and will appear as **above the misc-data-layers graphs as a tree** when you run <span class="artifact-p">[anvi-interactive](/help/main/programs/anvi-interactive)</span>. 

    <div class="codeblock" markdown="1">
    anvi&#45;import&#45;misc&#45;data &#45;p <span class="artifact&#45;n">[profile&#45;db](/help/main/artifacts/profile&#45;db)</span> \
                          &#45;t layer_orders \
                          <span class="artifact&#45;n">[misc&#45;data&#45;layer&#45;orders&#45;txt](/help/main/artifacts/misc&#45;data&#45;layer&#45;orders&#45;txt)</span> 
    </div>

## Nucleotides, Amino Acids, and Contigs Databases

This feature lets you import additional data about specfic residues or specific base pairs into your <span class="artifact-n">[contigs-db](/help/main/artifacts/contigs-db)</span>. This is especially useful for strucutral analysis (so when running programs like <span class="artifact-p">[anvi-display-structure](/help/main/programs/anvi-display-structure)</span>) and will be very relevant to the InteracDome functionality when it's added in anvi'o v7 (curious readers can take a look at [this blog post](http://merenlab.org/2020/07/22/interacdome/)). 

When adding additional data, unlike with layers and items, you do not have to provide values for every single nucleotide in your database. With this program, you can easily provide data for only a select few. 

Basically, you can add two types of data to your contigs database:

1. <span class="artifact-n">[misc-data-nucleotides](/help/main/artifacts/misc-data-nucleotides)</span> by providing a <span class="artifact-n">[misc-data-nucleotides-txt](/help/main/artifacts/misc-data-nucleotides-txt)</span>. This contains information about *specific nucleotides in your database.*

    <div class="codeblock" markdown="1">
    anvi&#45;import&#45;misc&#45;data &#45;c <span class="artifact&#45;n">[contigs&#45;db](/help/main/artifacts/contigs&#45;db)</span> \
                          &#45;t nucleotides \
                          <span class="artifact&#45;n">[misc&#45;data&#45;nucleotides&#45;txt](/help/main/artifacts/misc&#45;data&#45;nucleotides&#45;txt)</span> 
    </div>
        
2. <span class="artifact-n">[misc-data-amino-acids](/help/main/artifacts/misc-data-amino-acids)</span> by providing a <span class="artifact-n">[misc-data-amino-acids-txt](/help/main/artifacts/misc-data-amino-acids-txt)</span>. This contains information about *specific amino acid residues in your database*

    <div class="codeblock" markdown="1">
    anvi&#45;import&#45;misc&#45;data &#45;c <span class="artifact&#45;n">[contigs&#45;db](/help/main/artifacts/contigs&#45;db)</span> \
                          &#45;t amino_acids \
                          <span class="artifact&#45;n">[misc&#45;data&#45;amino&#45;acids&#45;txt](/help/main/artifacts/misc&#45;data&#45;amino&#45;acids&#45;txt)</span>                               
    </div>


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-import-misc-data.md) to update this information.


## Additional Resources


* [A primer on anvi&#x27;o misc data tables](http://merenlab.org/2017/12/11/additional-data-tables/)


{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-import-misc-data) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
