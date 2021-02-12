
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
          
     ##### appBar :
         void main() => runApp(
           MaterialApp(
           home: Scaffold(
           appBar: AppBar(
             title:Text('I am a rich'),
          ),
        )
      ),
    );
    
    1. material color system : https://material.io/design/color/the-color-system.html#tools-for-picking-colors
    
    
    ##### body :
    1.  body: Image(
            image:NetworkImage(''),
          ),
         
      
      
     2. working with Assets in flutter & the pubspec file:
     
        * create an images directroy.
        * use pubspec.yml file -> assets sector -> - images/
        * widget : AssetImage('images/diamond.png')
        
    ##### App icon :
        * first projec last tutorial -> flutter with dart
        
         
