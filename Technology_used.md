# Technology used

The key underlying technology used is 
[Modelica](https://modelica.org)
and an easyt to read concise introduction you find
[here](https://marcobonvini.com/modelica/2020/06/29/all-about-modelica.html)
and a comprehenisve online book
[here](https://mbe.modelica.university).
There is a number of commercial implementations of Modelica for example 
[Impact](https://modelon.com/modelon-impact/) and 
[Dymola](https://www.3ds.com/products-services/catia/products/dymola/), 
as well as  open source 
[OpenModelica](https://www.openmodelica.org)
and discontinued
[JModelica](https://jmodelica.org//).
I am in the process of developing
[Bioprocess Library *for* Modelica](https://www.openmodelica.org/images/M_images/OpenModelicaWorkshop_2021/Design%20aspects%20of%20BPL%20v4b.pdf)
that facilitate the modelling you see examples of at this site. But I do not expose you to much Modelica code and you so far only have access to compiled models in the form of FMU based on the international 
[FMI-standard](https://fmi-standard.org).
You can interact with an FMUs from different software and I use Python and the package I use is 
[PyFMI](https://github.com/modelon-community/PyFMI), 
but here are alternatives. You can also interact with FMUs in Julia and from commercial software like Matlab. To simplify interaction with FMU I am developing a package 
[FMU-explore](https://www.openmodelica.org/images/M_images/OpenModelicaWorkshop_2022/1505_Axelsson%202022,%20Design%20aspects%20of%20FMU-explore%20a%20Python%20module%20to%20complement%20PyFMI.pdf).
In my examples I use
[Jupyter notebooks](https://realpython.com/jupyter-notebook-introduction/) 
to combine text, small pieces of Python-code, and visualisation of results. 
In recent years Google offers 
[Colab](https://colab.research.google.com) 
which is a personal virtual  machine (on their servers) with Python pre-installed and where  you can run Jupyter notebooks. My examples let you use Colab and just follow the instructions in the README-texts in the repositories. After the session you can just go on and continue interaction.
