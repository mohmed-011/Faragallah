<h1 align="center">GNDecorator</h1>
<h6 align="center"> This project is part of the set of custom components created for JavaFx. </h6>
<h1></h1>

[![Sonatype Nexus (Releases)](https://img.shields.io/nexus/r/io.github.gleidsonmt/gndecorator?server=https%3A%2F%2Fs01.oss.sonatype.org&style=for-the-badge)](https://central.sonatype.dev/artifact/io.github.gleidsonmt/gndecorator/2.1.25)
[![Release](https://img.shields.io/badge/Release-v2.2.25-green.svg?style=for-the-badge)](https://github.com/gleidsonmt/GNDecorator/releases/tag/2.1.25)
![Build](https://img.shields.io/badge/Build-2.2.31+253-gold.svg?style=for-the-badge)
[![License](https://img.shields.io/github/license/Gleidson28/GNDecorator.svg?style=for-the-badge)](https://github.com/gleidsonmt/GNDecorator/blob/master/LICENSE)

<p align="center">
  <img src="./src/main/resources/logo/logo_flier.png"  />
</p>

# π Contents

<!-- TOC -->
* [π Contents](#-contents)
* [π» Environment](#-environment)
* [π Installing Decorator](#-installing-decorator)
* [β Using Decorator](#-using-decorator)
* [π§¬  Basic Structure](#-basic-structure)
  * [Structure - by Scenic View](#structure---by-scenic-view)
    * [Default Structure](#default-structure)
        * [View Default](#view-default)
        * [View Darkula](#view-darkula)
* [πΊ On Youtube](#-on-youtube)
* [π  Enhancements](#-enhancements)
* [π« Contributing to Project](#-contributing-to-project)
* [π Be a contritubutor<br>](#-be-a-contritubutor-br)
* [π License](#-license)
<!-- TOC -->

# π» Environment


This lib is a compnent for JavaFx:   Get in the offical website [JavaFx](https://openjfx.io/), Tutorial [Getting Started](https://openjfx.io/openjfx-docs/)

I have a great workstation here, then I've using a gradle 7.2 and Java and JavaFx +16 on Windows. (I really want to test in other systems in future).


# π Installing Decorator

Now you have many ways to get that!
!ποΈNote ** The release has the first changes I made and releases in nexus are more stable π₯Έ***

πIn code blocks find the copy button... is cooler, it automatically knows if your target is a pom.xml or gradle.build

For installing decorator, you have this options:

* For Pros - Click on the badge release or click badge nexus on the top of this document, and you're going to redirect to hosted sources.
* For Github Users - On the right side, you can see the packages and releases, click on them and download it, in case you are in packages just copy them into your build file.
* For Faster users - Just copy and paste the code bellow

If you use maven add in pom.xml:
```xml
<dependency>
  <groupId>io.github.gleidsonmt</groupId>
  <artifactId>gndecorator</artifactId>
  <version>2.2.25</version>
</dependency>
```

.. or in gradle.build:
```groovy
    implementation 'io.github.gleidsonmt:replaceVersionInREADME:2.2.25'
```

# β Using Decorator

Begin to use... Java Code!

```java
  GNDecorator decorator = new GNDecorator();
  decorator.setTitle("JavaFx Application");
  decorator.setContent(content);
  decorator.fullBody() // the content occupies all of size
    
 // Adding menus 
  Menu menu = new Menu("File");
  menu.getItems().add(new MenuItem("Open"));
  menu.getItems().add(new MenuItem("Close"));
  decorator.addMenu(menu);
  decorator.addMenu(1, menu);// add with a index
        
  // Adding custom controls
  ButtonTest a1 = new ButtonTest("Button 1");
  decorator.addControl(a1);
  decorator.addControl(index, a1); // add with a index
  ```


# π§¬  Basic Structure

        root -> SstackPane
                body -> AnchorPane
                        top_left -> Path
                        top_right -> Path -- rotation 90Β°
                        bottom_left -> Path -- rotation 270Β°
                        bottom_right -> Path -- rotation 180Β°


## Structure - by Scenic View
![Structure](src/main/resources/screens/primarySctructure.png)

### Default Structure
![gif2](src/main/resources/screens/explanation.jpg)


##### View Default
![demo1](src/main/resources/screens/default.png)
##### View Darkula
![demo1](src/main/resources/screens/dark.png)
##### With gradient and image
![demo1](src/main/resources/screens/mac.png)

# πΊ On Youtube
Short Presentation
[here](https://youtu.be/hZsYU7UbWmU)

# π  Enhancements

Next steps:

- [x] Add Yosemite Theme
- [ ] Add Windows Theme
- [ ] The decoratorTheme in blank to customize
- [ ] Public methods to update window icons with css.
- [X] Better pratices for one class receives state scope event (Clean Code)
- [ ] Default Property to change bar height
- [ ] Float options (css too)

# π« Contributing to Project
<!---Se o seu README for longo ou se vocΓͺ tiver algum processo ou etapas especΓ­ficas que deseja que os contribuidores sigam, considere a criaΓ§Γ£o de um arquivo CONTRIBUTING.md separado--->
To contributing to project, follow these steps:

1. Fork this repository.
2. Creates a branch: `git checkout -b <branch_name>`.
3. Do your changes and commit: `git commit -m '<commit_message>'`
4. Send a branch to origin: `git push origin GNDecorator / <local>`
5. Creates pull request.

However, if you don't know [How to create a pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

# π Be a contritubutor<br>

π€I really need more friends.. Send me a  <a href='mailto:gleidisonmt@gmail.com?subject=Hi, I see you need my help!.. I am here.'> email <a/>.

# π License

This project is under license. See the file [LICENSE](LICENSE.md) to more details.

[β¬ Back to the top](#GNDecorator)<br>
