##### to fit properly on the screen:
      Expanded(
             child:Image(
               image: AssetImage('images/dice1.png'),
             ),
           ),
### Material App:
            void main() => runApp(MaterialApp(home:Text('Hello world'));
            
            
      1. center widget:
                void main() => runApp(   // => / {}  this are the same;
                  MaterialApp(
                     home:Center(
                     child:Text('hello world')
                  ),
                  ),
                 );
         use , in every ')' end + reformat code with dartfmt;
         
      2. finding extra stuff in android studio like (//Center):  preferences -> editor -> general -> appearance -> click show closing labels in Dart source code.
            
         
  ### Scaffold: 
     1. in scaffold there are many other widget like appbar.
     
           void main() => runApp(
            MaterialApp(
              home: Scaffold(
              ),
            ),
          ),
          
     2. appBar :
     
         void main() => runApp(
      MaterialApp(
        home: Scaffold(
          appBar: AppBar(
            title:Text('I am a rich'),
          ),
        )
      ),
    );
           
         
      
