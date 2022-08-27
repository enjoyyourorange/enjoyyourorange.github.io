# enjoyyourorange.github.io
Intro to Prog Python Webpage

<html>
<head>

<!-- w3-content defines a container for fixed size centered content, 
and is wrapped around the whole page content, except for the footer in this example -->
<div class="w3-content" style="max-width:1400px">

<!-- Header -->
<header class="w3-container w3-center w3-padding-32"> 
  <h1><b>Assignment 07</b></h1>
   </header>

<p>
  <b>Introduction</b>
</p>

<p>

This assignment is focusing on pickling and utilizing try-exception blocks of code to not allow the user to input anything that may break our program or cause any unintended functionalities. I created a simple program that asks users to enter names or characters, and then simply pickles the entries to a file and unpickles them upon user request. 
</p>


<p>
  <b>Pickling in Python</b>
</p>
<p>
I began this assignment by creating some functions that will pickle, that is, serialize the entries given by the user, as well as append additional entries to our name list. 
	Saving the pickle file, using append binary mode: 
  <img width="400" alt="Screen Shot 2022-08-27 at 12 22 46 PM" src="https://user-images.githubusercontent.com/100233225/187046068-717a29b4-1b84-4513-a02c-c66a3b377ddd.png">
</p>

<p>
	Reading from pickle file using read binary and printing the result from the load:
  </p>

  <p>
  
<img width="413" alt="Screen Shot 2022-08-27 at 12 22 56 PM" src="https://user-images.githubusercontent.com/100233225/187046158-7396b49d-9376-4ea6-8b1e-cb74c9afe45d.png">
</p>
  
<p>
	Then, I needed a function that will append the user entries to a list to be recalled later:
  <img width="380" alt="Picture1" src="https://user-images.githubusercontent.com/100233225/187046284-6857d28b-0e2b-4536-8c07-a9d1ff27a678.png">



</p>
 
<p>
I quickly realized that when reading, or loading from a pickle file, that it will only grab the first entry given. I wanted a function that would allow continuous pickle loads until reaching the end of the file. To do this, we use a try-except block within a while loop that will continue loading until it receives an end of file error:  

  </p>
  <p>
    
<img width="460" alt="Picture2" src="https://user-images.githubusercontent.com/100233225/187046288-daa86c95-f7bb-4cad-9c52-ad3129be9753.png">

 <p>
  <b>Try-Except Handling</b>
</p> 

<p>
  Now that we had established the functions that will pickle user entries, save them to files, and allow them to be unpickled/recalled, I wanted to create some try-except blocks to prevent the user from entering things into my program that would either be pointless, or break my program.
 </p>
  
 <p>
  
Because my menu only has three options, I didn’t want to allow the user to enter anything that was not listed. To do this, I created a try-except block that will raise a value error in the event a user enters a character rather than one of the integers in the menu:
  
 </p>
  
<p>
  
  <img width="468" alt="Pictur3e1" src="https://user-images.githubusercontent.com/100233225/187046336-d5835783-d734-41a3-b3ad-4fa5c18407dc.png">
  </p>
  
<p>
Then, I realized that still allowed the user to enter any integer value that wasn’t listed on my menu. Now, this doesn’t break my program or anything, but it’s a pointless function and doesn’t look very nice. So, I created a couple if statements that would not return the user entry unless it was either a 1, 2, or 3:</p>
  
  
<p>
  <img width="400" alt="Pictur4" src="https://user-images.githubusercontent.com/100233225/187046364-93e75e13-0138-4d08-8e64-e6272d6315b2.png">

  </p>

<p>
	Then, it was time to create the main body of the script that would call my created functions. If the user selects 1, the program will ask the user to enter a list of characters. I specifically did not want to allow integers, but I was having some trouble making this happen, because the value error exception was not working for the inverse of my previous usage. To remedy that, I imported the regular expression module and created an if statement that only allowed characters that match the library’s A-Z characters:
  
  </p>
  
  
<p>
<img width="468" alt="Picture5" src="https://user-images.githubusercontent.com/100233225/187046377-957b3b96-7c7f-4f01-b1e6-03171151f31d.png">
  
  </p>
  
<p>
Next, if the user’s entry was acceptable, I simply called my add_to_pickle and save_to_pickle functions to append the entry and save the pickle file: 
  </p>
  
  
  <p>
  <img width="325" alt="Pictur6e1" src="https://user-images.githubusercontent.com/100233225/187046454-17dba6df-de1b-4ed7-9fe0-5635752f7951.png">

  </p>
  
 <p>
	Finally, if the user’s entry was 2, our program simply calls load_all_pickle to loop through the saved pickle file and keep loading until it reaches the end of file error. And if the user chooses entry 3 the program will simply break and close:  
  
  </p>
  
  
  <p>
<img width="347" alt="Picture7" src="https://user-images.githubusercontent.com/100233225/187046467-b9c8d6ec-4787-4be9-ba6c-d0b0eb58b0e9.png">

  </p>
  
  <p>
    <b>Summary</b>
</p>
  
  
  <p>
  	This assignment was pretty fun and a good learning experience. Working with pickle files was pretty enlightening and confusing at times, I ran into some strange Unicode issues that was a good learning experience to hash out. I really enjoyed creating the try-except blocks, especially with the load_all_pickle function that utilized the EOFError, as trying to find ways to load all the entries was driving me a bit crazy. The importing of modules is really interesting, too, feels like that’s a huge part of programming in Python that we’re just getting into. 
  </p>
    

</html>
