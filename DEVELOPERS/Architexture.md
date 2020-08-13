## From <img src="docs/images/armirage-logo.svg" alt="Armirage company logo. An 'A' shaped leaf with the internal silhouette shaped like a person." style="width:30px;"> ARMIRAGE

## Webapp Template Folder

> Without requirements and design, programming is the art of adding bugs to an empty text file.<br>
> -- [Louis Srygley](https://www.imdb.com/name/nm3632905/)

This is a generic template for new projects. It has no code.

## Table of contents
* [Documentation](#documentation)
* [README](#readme)
* [LICENSE](#license)
* [template.env](#template.env)
* [template.eslintrc.json](#template.eslintrc.json)
* [template.gitignore](#template.gitignore)
* [Developers and doc](#developers-and-doc)
* [Architecure Pattern](#architecure-pattern)
* [Not the Same Old MVC](#not-the-same-old-mvc)

## Documentation

In a large organization documentation will include things such as style guides, request for changes, transfer of responsibilities, help desk articles, and many more.

These documents can be created in programs like Word, OpenOffice, Libre Office, ect. Once created they are distributed, updated, and revised through systems like Docushare, Sharepoint, again ect.

A discussion on the *pros* and *cons* of such systems is outside the scope of this project. Just be mindful, though missing from this template, organizational level documentation is no less important for the life cycle of an application.

Individual files have been commented for further reading. I suggest removing the comments and deleting this START-HERE.md when publishing your own app.

### Format

The docs are written in [Markdown]. A light weight markup language that allows text files to be rendered stylishly. Closer to creating a rich text file than an HTML.

Before the popularity of Markdown, these files would have been flat text files (.txt). One may recognize the ever present README and LICENSE.

More about Markdown:<br>
[Markdown Wiki Article](https://en.wikipedia.org/wiki/Markdown)<br>
[Github Markdown Guide](https://guides.github.com/features/mastering-markdown/)

## README

A nice README is a good way to help people engage in the project. A project with nice README and screenshots will get the attention of users better since it is a direct way to explain why this project matters, and why people should use and contribute to the project. Good README should also include enough details to help a new user get started, ie how to compile, how to install, and how to start integrating.

You may find some of the other files, CONTRIBUTING, CHANGELOG, CITATION, or SUPPORT are included in an application's README.

For more examples of README:<br>
[Matias Singers' Curated List](https://github.com/matiassingers/awesome-readme)<br>
[One guide to writing a README](https://thejunkland.com/blog/how-to-write-good-readme.html)

## LICENSE

I am not a lawyer and for any legal advice one should consult with a licensed attorney.

Personally, I put a docblock (a comment block at the top of a each file containing meta-data) that reaffirms my copyright, names my license, and a link to the full text of license. Preferably a link to a public website that explicitly relates the application to the license(s).

More on Open Source Licenses:<br>
[Open Source Initiative](https://opensource.org/licenses)<br>
[Free Source Foundation](https://www.fsf.org/licensing) - An earlier movement.<br>
[Creative Commons](https://creativecommons.org/licenses/) - Explicitly not for Code, but for creative work like images (application art) and writing (application guides).

## template.env

In many of my projects I use a dotenv file during development.

The dotenv should be named simply ".env". It becomes a hidden file. From it the application can populate environmental values. For instance if during development, you the application listens on port 8080, but during deployment it needs to listen on port 80, such a thing is done with passing environmental variables. For a simple case scenario they can be recorded in this file. During production it is better to have them passed into an instance by a build script.

Further reading on dotenv:<br>
[dotenv npm package](https://www.npmjs.com/package/dotenv)<br>
[How to use dotenv article (opinionated)](https://dev.to/numtostr/environment-variables-in-node-js-the-right-way-15ad)<br>

## template.eslintrc.json

> Programs must be written for people to read, and only incidentally for machines to execute.<br>
> -- H. Abelson and G. Sussman (in "The Structure and Interpretation of Computer Programs)

Lint was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs). Applied generically to tools that flag suspicious usage in software written in any computer language.

Now linting is being used to enforce style guides. A team of several people can wite code for an application, adhering to a particular *voice*. That voice is the rhythm, syntax, semantics, common patterns of the code.

This makes it easier to follow the logic of code because variable, property and object naming are consistent. There are less jarring effects because there is a consistent use of style. An overall approach to how the application runs is consistent from one part to another. Also aiding in software optimizations.

Further reading about Style Guides:<br>
[Google Style Guides](http://google.github.io/styleguide/)<br>
[Javascript Style Guide](https://javascript.info/coding-style)<br>

Further reading about ESLint (there are other linters):<br>
[ES Lint](https://eslint.org/docs/user-guide/getting-started)

Configure your linting app and rename to ".eslintrc.json".
This particular linting style is only for javascript and a personal preference. Find one that works for you, or your organization, and stick with it.

## template.gitignore

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

It is a protocol used by GitHub, GitLab, and other services. The protocol allows a team to make diverse changes to source code, and to negotiate conflicts. Review and commit external improvements, or tangent experiments with the code.

This file (again rename to ".gitignore") is read by Git applications or extensions as to what files are ignored when uploading to a repository. 

For instance, a developer using VS Code may have hidden workspace folder. Other application create similar artifacts in the working directory. By using a .gitignore file, such additional folders can remain for use by the developers workstation. And be ignored when uploading the app's source code to a shared repository.

More reading:<br>
[Gitignore Documentation](https://git-scm.com/docs/gitignore)

## Developers and doc

There are two folders unrelated to the application logic.

The normal naming convention for web folders is lowercase and hyphenated. Being lowercase for compatibility among servers that are case sensitive. And hyphenated so that if the pathname were displayed as a link, the separator (hyphen) is not ambiguous like a space or underscore would be. 

You will notice I break this convention for Developers. Because it is a quick reference to me that this is a local folder for me to use. "Developers" is git ignored by the ".gitignore" file (when in use). 

Inside "Developers" I may have snippets of code or starting templates for consistency. I may have quick tests of code to see what implementation will work best.

"doc" is not explicitly ignored. And the doc folder holds  documentation broken down by audience. 

The "users" folder may contain a FAQ (Frequently Asked Questions), "legal" may contain complete licenses. And other more detailed information for developers and admins.

A relatively small application can get away with storing these docs close to source code. When an application becomes more complex and the documents shared among audiences, we move the info from these docs into organizational space. Using complex documents as described earlier.

## Architectural Pattern

An [Architectural Pattern](https://en.wikipedia.org/wiki/Architectural_pattern), in reference to applications, is an overall organization of the code base.

There is a lot to be said about Architectures. For further reading check out:<br>
[10 Common Software Architecture Paterns in a Nutshell](https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013)<br>
[Unidirectional Architecture](https://staltz.com/unidirectional-user-interface-architectures.html)<br>

However, for the purpose of these examples we will keep things only as complex as they need to be.

Let us consider the biological cell. To be considered a living organism, biological life exhibit certain characteristics. Attributes like metabolism, movement, growth, ect.

Looking at the single cell we can see there are separate structures that have different primary functions. The mitochondria of the cell are responsible for consuming a fuel source and creating energy, the rest of the cell can utilize. The DNA is responsible for the compressed long term storage of information. The Membrane separates the outside from the inside of the cell, changing physical characteristics to filter incoming chemical messages.

All of those parts coordinate to keep the cell a live. Coalesce in the cell having the characteristics of biological life.

<img src="docs/images/cell-parts.png" alt="Diagram of cell parts." style="width:350px; display: block; margin-left: auto; margin-right: auto;"><br>

From the perspective of a different magnitude a whale also has the characteristics of Biological Life. Instead of mitochondria being responsible for energy, the Whale digestive system is.

And the whale digestive system is an order of magnitude larger and more complex. (at least in the terms of, *the number of different homogenous textures*)

What is more amazing of these similarities between biological creatures, is the whale is composed of trillions of cells.

*Nature crafts new creatures from already present structures in response to environmental conditions.*

What does biology have to do with programming applications? Glad you rhetorically asked.

> All software development is composition: The act of breaking a complex problem down to smaller parts, and then composing those smaller solutions together to form your application.<br>
> -- [Eric Elliott from "Composing Software"](https://medium.com/javascript-scene/composing-software-the-book-f31c77fc3ddc)

Both approaches attempt to solve problems with composition and incremental change of smaller prior existing material. The analogy is not lost on many scientist. With the recent emergence of [Biomimetics](https://en.wikipedia.org/wiki/Biomimetics)

The modular design of the living cell, is like the [separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns) in modern programming. Developers separate their code by role or responsibility as opposed to file type. (folders like img, js, css, arrangements)

In the same way we develop programs to be modular like the parts of a cell. Structures and areas based on role. We should make our programs *cellular*.

> We have also obtained a glimpse of another crucial idea about languages and program design. This is the approach of stratified design, the notion that a complex system should be structured as a sequence of levels that are described using a sequence of languages. Each level is constructed by combining parts that are regarded as primitive at that level, and the parts constructed at each level are used as primitives at the next level. The language used at each level of a stratified design has primitives, means of combination, and means of abstraction appropriate to that level of detail.<br>
-- [H. Abelson and G. Sussman from "The Structure and Interpretation of Computer Programs"](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)

Many of us recognize programs being organized in hierarchial layers. I suggest each layer be of the same modular design, composed of the same responsibilities, similar in look to other peer modules. Essentially, the lowest levels being single cells, and the highest levels being of the same modules. While each module is as complex or simple as needed within its relevant layer

## Not the Same Old MVC

[Model-View-Controller](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) aka MVC is a popular Software Architecture. Originally designed for desktop applications, modern implementations of the pattern usually take a variation of the MVC approach. It is not uncommon to see entities that represent modules, libraries, handlers, authenticators, security, and interfaces in modern renditions of the MVC pattern.

Let us delve right into what Software Architecture is presented by the Webapp Template.

Each Layer is responsible for a different aspect of the application. Generally speaking they are Data, Modifiers, Actuators, Structures, and Presentations.


<img src="docs/images/DMASP.png" alt="Diagram of cell parts."><br>

### Presentations Layer
The Presentation Layer, aka Views, is responsible for the outermost representation of a layer. Like the Membrane of a single cell it is the interface by which signals traverse from outside noise to messages considered by the cell. The Membrane is a kind of [Application Programming Interface](https://en.wikipedia.org/wiki/Application_programming_interface) for the cell. In much the same way Views is the outward appearance of an entity. The cell itself, the App itself, can be a black box to users. Users interact with the presentation layer, which can be text, visual, or an assistive device.

The Presentation Layer is responsible for the interface presented to other modules, apps, and end users. To accomplish this role it may inside itself have Data in the form of language dictionaries or images. It may in itself have ways of modifying the View, a controller, and internal structures. It may in and of itself mirror the DMASP modularity. It becomes a cellular part of the whole.

This layer is also only concern with the underlying Structure. Dependent on the Structure to dictate what is a header, main article, menu or interactive control. One type of View should be able to successfully render similar structures. In a simple single page app this layer could be composed of mostly CSS and images.

### Structures Layer

The Structures Layer is the skeleton that holds and identifies content. It is ambivalent to what the presentation layer is doing. Concerned with only alerting the presentation layer of changes. Just like the View must have an understanding of the structure and thereby be coupled to it. The Structure is dependent or coupled with the Controller (Or Actuator Layer). To receive new information it must communicate to the Structure layer in an agreed upon way. In a web app these structures might take the form of HTML.

But because the DMASP Architecture is cellular in form, we can discover structure being present as XML in a Data module, or as an object inside the Controllers Layer.

### Actuators Layer

In a mechanical sense, Actuators are levers, switches, buttons that initiate the functions of a mechanical device. In essence the actual controls of a machine. And the Actuators (aka Controllers) here do the same thing.

Applications in essence attempt to render Data to an End User, and then manipulate that Data. With the rise of Big Data and multiple sources of truth for different data, the Controllers rely on Modifiers (or Handlers) to dot he actual manipulation of Data. And prefer to keep their hands clean so speak.

### Modifiers Layer

Here we find the Handlers responsible for actually interacting with Data sources. They format the requests from the Controllers in syntax the Data can respond to. They also send instructions to the Data for the Creation, Reading, Updating, and Deletion of Data (CRUD).

### Data Layer

In MVC the Data layer is called the Model. It is a representation of the Data the application as whole is meant to convey or manipulate. One may recognize that the Model is a *representation*.  And certainly so it is. Take for instance a Data Layer that is composed of a SQL database. That database is a cellular part. Itself having the modular roles outlined in the DMASP Software Architecture. The database would have its own presentation layer, its own internal structure (sometimes vastly different than the representation presented to outside agents), its own internal logic of controllers and modifiers, and a source of its own data.

### Additional Notes

DMASP is a way of organizing the different roles of a module. That module itself, may fulfill a single DMASP role for an encapsulating module. In this respect the design is both modular and cellular. MVC architectures are adding multiple new folders along with Models, Controllers, and Views. Development being driven by Seperation of Concerns. While I find it more intuitive to include Handlers and Structures, other folders may appear when cause arises. Folders such as modules or libraries (lib). 
