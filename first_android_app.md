## [The new step by step guide detailing how to get started developing Android apps, with no prior experience necessary. Includes every resource I used, simple explanations and an interesting first app tutorial. Everything you need to get started in Android Development is here.](https://www.reddit.com/r/Android/comments/2tpjep/the_new_step_by_step_guide_detailing_how_to_get/)

A year ago, almost to the day, I compiled a post of all the resources that would be required for a complete programming noob to set out making an Android app. At the time the post was one of the highest on r/Android of all time. This year, having vastly improved my own skills, I’m out to make the ultimate guide to creating Android apps without prior experience.
 
[Here is a link to the old post, in case you’re interested.](http://www.reddit.com/r/Android/comments/1w3woc/a_step_by_step_guide_about_how_to_get_started_and/)
 
##There are two ways of approaching this post:

1.      Be at a computer, follow the explanations and instructions and you’ll have an app and some basic skills to branch off by the end of it.
2.      Just read the post and learn some basic app skills.
 
**What is Java?**
 
Java is a programming language like C++, Python and Ruby. Essentially, most apps on the Android platform (most games and other apps are written in different languages) are written in Java. Approaching a programming language without prior experience is challenging, but with a little patience it is doable. 
 
**Java is an OOP or Objected Oriented-Programming Language**
 
This means that Java is a programming language based on the concept of objects, which are essentially fields of data that can run code and store variables.
For example, a String object is an object that contains any combination of letters, numbers and other characters. A String is formatted in quotation marks, here is an example use:
 
    String name = "Dennis";
 
    String surname = "Cometti";
 
    String FullName = name + " " + surname;
 
 
After this runs, the variable FullName will equal “Dennis Cometti”.  A String is an example of a basic object, other basic Objects in Java include Integers (any whole number), booleans (a true or false value) and floating points (decimal values like 3.0).
 
I HIGHLY recommend checking out [this website for a more detailed explanation.](http://code.tutsplus.com/tutorials/java-tutorial--mobile-2604)

Objects can also contain other objects and variables, for example you could define a ‘Quote’ Object that contains two values: The actual quote and the name of the quoted person.
 
**A lot of the fundamentals in Java are essentially plain English**
 
All of Java is written in English, the structure of the words change but if enough attention is given to it can actually be very easy to understand. For example:
 
    String name = "DENNIS";
 
    name = name.toLowerCase();
 
 
It couldn’t be any clearer, this will assign the lower case converted “DENNIS” ("dennis") to the 'name' variable.
After you have typed ‘name.’ Android Studio will give you a list of possible methods (like toLowerCase() or toUpperCase()) that can be used, so you get some guidance.
 
**Classes, methods and objects in Java**
 
•     A **variable** holds a field of data. A variable might be a surname, your weight or the distance travelled by your car. A String is a variable that could contain “Dennis” and an int is a variable that could contain the number 89.
 
•     A **method** is a function (like name.toLowerCase()). Basically a method does things using variables or any number of lines of code. You can write your own methods, for example in the app we will be making soon we will be making a method called getQuote(). A method might display a quote on a screen or change the text in a TextView.
 
•     An **object** holds both variables and methods; one object might be the details of your car, a second object might represent my car.
 
•     A **class** is a template that holds variables, methods and other objects.
 
**So what is the difference between classes and objects?**
 
A class would be a Car (containing no details but rather a template).
An object would be your Car (containing all the details about the car).
 
A class would be a String (containing no details but rather a template).
An object would be a ‘name’ (containing the String “Dennis”).
 
If you are confused, don’t worry, once you have followed the instructions you’ll understand it much clearer.
 
**Some Java related resources**
 
- [The basics of Java](http://code.tutsplus.com/tutorials/java-tutorial--mobile-2604)
- [The syntax of Java](http://www.tutorialspoint.com/java/java_basic_syntax.htm)
 
 
##How do you get started making an app? 
 
**Get Android Studio**

Android Studio is the new (just out of beta) Android Integrated Development Environment, don’t let the words confuse you – it’s essentially a program that has all the tools you need to make an app. Some people come across some issues installing Android Studio make sure you are Googling any issues that you come across in this stage, but you should be fine.  You’ll come across many things you don’t understand when making apps but I guarantee you 1000 people have had the same problem before and there will be help or tutorials online (you shouldn’t need them for this exercise).
 
#Instruction #1: [Download and install the Java JDK]( http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)

#Instruction #2: [Download and install Android Studio, but don’t open it yet.]( https://developer.android.com/sdk/index.html)
 
**Strings in Android**

Strings as mentioned earlier, are used everywhere: App Dialogs, Titles, Messages, Error Logs and literally wherever you see characters. The problem is, when you are making an app with many Strings it can become quite fiddly. So Google created a solution: a single file that stores all of your Strings in one place, so you can get that one file translated and refer to those strings in tons of different parts of the code.
[Here’s a link from Google that can explain it in more detail]( http://developer.android.com/guide/topics/resources/string-resource.html)
 
**How Android Studio works**

Android Studio contains all the tools you need to make an app: for this tutorial you won’t be using many. When you create a new ‘Project’ (App) Android Studio will generate all the files and folders necessary to begin a project.
[This screenshot shows what it generates](http://i.imgur.com/HOX9B7S.png)
This looks quite complex but it’s actually quite simple. For example the ‘layout’ folder will contain all the layouts of the app screens you’ll use, which brings us to the next few steps.
 
 
 
 
 
#####We are going to make a simple Quote app! It will show a quote plus the name of the person who made the quote and loop through as many quotes as you like when you tap the screen.

>

 
#Instruction #3: Open Android Studio and click the create new project button.

 
#Instruction #4: [Follow these screenshots exactly to set up the new project]( http://imgur.com/a/o7NdR)

 
#Instruction #5: [You should land on this page, if not, open the layouts folder and click the file inside it](http://imgur.com/JM4BIMV.png)

 
#Instruction #6:
The screen you are on now is the layout screen, if you click the design button towards the bottom you will be greeted with a drag and drop editor. For now replace all of the text in the text tab with this: http://pastebin.com/pRisAsPF

This has formatted the layout of the main app Activity, but you can change some things around. Try changing the text from “Tap the screen to begin” to something else. Extra points to anyone who can change the font color.
 
#Instruction #7:
Now we have to make a new class, and the quote Object we spoke about earlier. These screenshots show how to make a new class: http://imgur.com/a/3I7v9

You’ll now land on the empty Quote class, but we are going to fill it with a bit of code now.
You will see ‘public class Quote{}’, in between these two squiggly brackets paste this code: http://pastebin.com/VhHbWwSN 
Just click OK to any popup boxes.

What this class does is allows the app to create a Quote object that we can use, you ‘instantiate’ the class and pass through a quote and name (where it says public Quote(String mQuote, String mPerson)) and then you can retrieve the quote or person name later. More on this soon.
 
#Instruction #8:
Click on the Quotebook class here: http://i.imgur.com/bG2d0VD.png
Then copy and paste this code in between the onCreate(){ brackets but after all of the other code inside: http://pastebin.com/wz8gbWWA

You’ll notice some red squiggly lines telling you there is an error, so just under the line that says public class Quotebook extends Activity {  add in this variable/line: int count = 0;

This is what the two sections should look like after the have been copied and pasted: http://pastebin.com/3FXi14XZ
 
 
 
 
 
#Explanation time!
 
    setContentView(R.layout.activity_quotebook);
 
    RelativeLayout touch = (RelativeLayout) findViewById(R.id.touch);
    final TextView quoteText = (TextView) findViewById(R.id.quote);
    final TextView personText = (TextView) findViewById(R.id.person);
 
 
The first line sets the app page (Activity) to be the layout we created earlier. The following lines just declare the Textboxes on the layout we created so we can change the text in them.

____________________


     final ArrayList<Quote> quoteList = new ArrayList<Quote>();
 
     Quote quote1 = new Quote("You're more of a fun vampire. You don't suck blood, you just suck.", "Troy Barnes");
     quoteList.add(quote1);
 
     Quote quote2 = new Quote("Cool Beans", "Rod Kimble");
     quoteList.add(quote2);
 
 
The first line here creates an Array/List that we can add as many quotes as we like to, note how the List is called ‘quoteList’.
 
The next 4 lines are where the Quote class we created earlier are coming in to play. What we are doing here is passing a quote and a person’s name (separated by a comma) through to the Quote class and it becomes a variable, we then add that Variable to the quoteList.

____________________


This is where it gets a little tricky:
 
    touch.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
 
                if (count < quoteList.size()) {
 
                   Quote q = quoteList.get(count);
                   quoteText.setText(q.getQuote());
                   personText.setText(q.getPerson());
 
                   count = count + 1;
 
                } else{
 
                    count = 0;
 
           }}});
 
 
This looks complex but if you imagine it as a plain English sentence it makes far more sense.

*If every quote has been cycled through, set the count to 0 so it starts again.
If we have not gone through every quote, get the Quote variable in the quoteList at the count we are up to, then set the text on the quote and person textboxes to the quote data we just grabbed*

If you read through the code and the English algorithm above a few times you should be able to understand what this code is doing.
 
 
 
#Instruction #9:
Find the two folders on the left hand side labelled ‘values’ and ‘values-v21’, they should both contain a file called styles.xml
In the ‘values’ folder, change the parent= value to be:

    parent="android:Theme.Holo.NoActionBar"
 
In the ‘values-v21’ folder, change the parent= value to be:

    parent="android:Theme.Material.NoActionBar"
 
This just changes the App Theme, you could every try change to other themes.
 
#Instruction #10:
To do this next step, you have to:
- Ensure that you have your phones USB drivers properly installed.
 
- [Enable Developer Settings](http://www.greenbot.com/article/2457986/how-to-enable-developer-options-on-your-android-phone-or-tablet.html) then enable USB Debugging.
 
- Have your phone plugged in and accept the popup that checks if you would like to connect to your computer (Android Studio/ADB)
 
Then, you have to click the [green play button](http://i.imgur.com/cOkY2Ep.png), the app will compile and if you have set it up correctly it should send it to your phone and open the app!
 
If you have issues here, Google your phone + abd drivers/android studio.
 
#Instruction #11:

Change the quotes around, try and add more! If you have a particular interest in an area change the quotes and make a targeted app like a movie quotes app that has all your favourite quotes or lines.
 
Change the font, colours, formatting or use.
Share your own versions in the comments!
 
#If you enjoyed that, here are all the resources you need to dive deeper in to Android Development.
 
**Libraries**
 
Libraries are like pre-made bundles of code that you can use instead of coding everything yourself.
For example the IO Commons library  contains a huge range of methods that manipulate files in one line, like copyFile(), moveFile() and getExtension() instead of having to do them manually.
There are specifically made Android libraries from Google that allow you to use newer Android features like the navigation drawer on older devices.
 
Android Arsenal is a great site for finding Android Libraries:
https://android-arsenal.com/
 
And here is how to add them to Android Studio:
http://stackoverflow.com/questions/16588064/how-do-i-add-a-library-project-to-the-android-studio
 
 
**More advanced Pro-Tips**
 
- Stack Overflow is a fantastic community if you have any development questions - but Google it first.
- Check out /r/androiddev
- Follow Google Design Guidelines.
- If you don't really understand some code or how to do a particular task, Google it, comment what you are trying to do and ask around.
- Use libraries wherever you can.
 
 

**A list of advanced development related resources**
 
- [A huge resources list](https://github.com/thecodepath/android_guides/wiki/Beginning-Android-Resources)
 
- [Activity Lifecycle IMPORTANT](http://developer.android.com/reference/android/app/Activity.html)
 
- [Fragments IMPORTANT](http://www.vogella.com/tutorials/AndroidFragments/article.html)
 
- [More Fragments](http://developer.android.com/guide/components/fragments.html)
 
- [Dialogs](http://stackoverflow.com/questions/2478517/how-to-display-a-yes-no-dialog-box-in-android)
 
- [Navigation Drawer](http://developer.android.com/training/implementing-navigation/nav-drawer.html)
 
- [Toasts - popups](http://www.mkyong.com/android/android-toast-example/)
 
 
**A list of design related resources**
 
- [Material Design Guidelines](http://www.google.com/design/spec/material-design/introduction.html)
 
- [Material Design Icon Downloads](https://github.com/google/material-design-icons)
 
- [Material Design Icon Index](https://google.github.io/material-design-icons/)
 
- [Design Inspiration](http://androidniceties.tumblr.com/)
 
*Well that’s it for now!*
If you need any motivation: I’m 17 years old and started doing this when I was 15. If I can do it, you can.
 
If you’d like to thank me in some way for the post, give my app a look: [Redirect File Organizer](https://play.google.com/store/apps/details?id=com.tobino.redirectspaid&hl=en).
I only need 2000 downloads to pay for university starting next year!
 
Please leave as many comments, screenshots and queries as you can – I’d love to hear what you think!
