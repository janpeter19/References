# Technology used

The key underlying technology used is Modelica and brief readable introduction you find
[here](https://marcobonvini.com/modelica/2020/06/29/all-about-modelica.htmlhttps://marcobonvini.com/modelica/2020/06/29/all-about-modelica.html) 
There is a number of commercial implementations of Modelica for example 
[Impact](https://modelon.com/modelon-impact/) and 
[Dymola](https://www.3ds.com/products-services/catia/products/dymola/), 
as well as  open source 
[OpenModelica](https://www.openmodelica.org).
I am in the process of developing  
[Bioprocess Library *for* Modelica](https://www.openmodelica.org/images/M_images/OpenModelicaWorkshop_2021/Design%20aspects%20of%20BPL%20v4b.pdf)
that facilitate the modelling you see examples of at this site. But I do not expose you to much Modelica code and you so far only have access to compiled models in the form of  FMU and more on the underlying international 
[FMI-standard](https://fmi-standard.org)
You can interact with an FMUs from other software and I use Python and the package I use is PyFMI, but here are alternatives. You can also interact with FMUs in Julia and from commercial software like Matlab. To simplify interaction with FMU I am developing a package FMU-explore that you can read about here.  Jupyter notebooks that is used in the example to combine text, small pieces of Python-code, and visualisation of results, you can read more about here. In recent years Google offers Colab which is a personal virtual  machine (on their servers) with Python pre-installed and where  you can run Jupyter notebooks. My examples let you use Colab and just follow the instructions in the README-texts in the repositories. After the session you can just go on and continue interaction.









