===========
Preface
===========

QCASketcher is meant to be a reimplementation of QCADesigner, the de fact standard software in QCA(Quantum Cellular Automata) circuit design and simulation. 

Emerged in an academic environment, QCADesigner inevitably suffers from  obscure software architecture and is hard to extend.

On the other hand, being an burgeoning research area, lots of new ideas burst out suddenly. So a platform convenient for the implementation and verification of the ideas  will prove its significance. QCASketcher is such an attempt.

The fundamental idea behind QCASketcher is to provide a multi-facet programming interface of QCA design and simulation for the academic community. 

The first interface is a graphical user interface. Despite its similarity  with QCADesigner at first glance, the architecture behind the scene is distinctively different. QCASketcher admits to a rather strict MVC(Model View Controller) paradigm thus achieving a loose coupling with the core algorithms in circuit simulation.

Besides the ordinary GUI interface, a programming interface using C++ classes in OOP(Object Oriented Programming) style is exposed as well. These C++ classes are responsible for the main workload of the computation. And their interfaces are designed to be flexible enough to support the customization of the whole QCA design process, such as new simulation engines or new timing schemes.

For the convenience of users, QCASketcher also provides a scripting interface using Python programming language. Users can embed the core algorithms into a more fluid working flow scripted in Python. So simulation automation as well as statistical analysis of simulation results will be achieved  in an easy manner. 

At the end, a fourth interface appears in a form of a DSL(Domain Specific Language). DSL is a kind of "killer app" for domain experts. Fortunately, researchers in QCA field is exactly the domain experts of QCA. Through the DSL interface, researchers need not to program the simulation process in either C++ or Python, rather they describe their ideas in a more natural way similar to speaking a natural language. 

With all the interfaces mentioned above, we believe that a solid and extensible environment for QCA computation can be established. And the whole academic community  in QCA area will benefit from it. 