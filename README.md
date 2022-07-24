# Kotlin Navigation Project
This is a Kotlin project that uses navigation feature to navigate between fragments. You can clone it and use it or follow the instructions and make one yourself.  
Here is the complete guide to make such project yourself. To make a project I will be using IntelliJ IDEA.

## Creating a project

First thing you have to is to create a project. To do so, go to the File – New – New Project

<img src="README%20Images/createnewproject.jpg" width="400">

For the purposes of demonstration, we will be starting from an Empty Activity. So, select Empty Activity.

<img src="README%20Images/empact.jpg" width="400">

Name you application and click Finish.

## Setting up the gradle files

Lets setup the Gradle files. In this project we will be using View binding feature, so we have to add it to our project, as well as the necessary imports and dependencies for using the navigation feature. The build.gradle files are located here.

<img src="README%20Images/Gradle.jpg" width="400">

Add the following code to the Project build.gradle file in the dependencies block:

```Kotlin
classpath "androidx.navigation:navigation-safe-args-gradle-plugin:2.5.0"
```
Should look like this:

<img src="README%20Images/projectGradle.jpg" width="400">

Now we will edit the Module build.gradle file. Add the following implementations to the dependencies block:

```Kotlin
implementation 'androidx.navigation:navigation-fragment-ktx:2.5.0'
implementation 'androidx.navigation:navigation-ui-ktx:2.5.0'
```
Should look like this:

<img src="README%20Images/mbuildgradle.jpg" width="400">

Add the following plugin to the plugins block 

```Kotlin
id 'androidx.navigation.safeargs'
```

Should look like this:

<img src="README%20Images/Plugins .jpg" width="400">

Add the following code to the android block:

```Kotlin
buildFeatures {
    viewBinding true
}
```
Should look like this:

<img src="README%20Images/androids.jpg" width="400">

## Creating a navigation graph

Now we are ready to start creating the project itself. To start, go to the resources manager on the left side of android studio. Select the navigation tab and click the plus sign. 

<img src="README%20Images/resmeng.jpg" width="400">

Name your nav file and click ok 

<img src="README%20Images/mynavname.jpg" width="400">

Now we will create two fragments, to later setup the navigation between them. To do so click the little phone icon with a green plus

<img src="README%20Images/addfragment.jpg" width="400">

Click create new destination and select blank Fragment and name it.

<img src="README%20Images/createnewdest.jpg" width="400">
<img src="README%20Images/fragmentname.jpg" width="400">

Do the same steps for the second fragment. The result should look like this:

<img src="README%20Images/createdfragemnts.jpg" width="400">

Now click and drag the little bubble on the right side of the mainFragment and connect it to secondFragment. Then do the same thing back, it should look like this:

<img src="README%20Images/dothesameback.jpg" width="400">

Now you have to create a Nev Host fragment (our Main activity). To do so go to the XML of the main activity and in the search bar type "frag…". A NavHostFragment will show up. Click and drag the NavHostFragment to the main activity layout:

<img src="README%20Images/nevhost.jpg" width="400">

Select my_nev and click ok 

<img src="README%20Images/selectnev.jpg" width="400">

After that go to the code section of the main_activity xml and add the constraints for the fragment. Add the following code to the bottom of fragment code:

```Kotlin
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent"
```

It should look like this:

<img src="README%20Images/codexml.jpg" width="400">

Now we will go to the fragment_main.xml and add a button and some text to the fragment. To do so go to the xml file and select the code view:

<img src="README%20Images/mainfrag.jpg" width="400">

Check if the layout type is constraintlayout or not. If its not replace FrameLayout with the following code 

```Kotlin
androidx.constraintlayout.widget.ConstraintLayout
```
Should look like this:

Before                                                    |  After
:--------------------------------------------------------:|:-----------------------------------------------------:
 <img src="README%20Images/cahnge.jpg" width="400">     |  <img src="README%20Images/cahngegg.jpg" width="400">



