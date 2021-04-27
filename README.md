................................. Dart ....................................................................

### Dart OOP.
 Every object is an instance of a class
Dart has NO method overload
Every member is public by default unless you append
an underscore (_) which makes it private to its library


















................................................ Flutter .......................................................

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
        
    ##### Deploying flutter apps on a physical android device
    
  ### layout user interface :
    ##### Hot reload and hot restart: 1. stless
    
 
  ### layout widgets :
            2 types of layout widget : * single child widget -> container, *multi-child widget
  ##### container widget: 
    1. container with no children try to be as big as possible:
                        
              void main() {
              runApp(MyApp());
            }

            class MyApp extends StatelessWidget {
              @override
              Widget build(BuildContext context) {
                return MaterialApp(
                  home: Scaffold(
                    backgroundColor: Colors.red,
                    body:Container(
                      color: Colors.teal,
                    ),
                  ),
                );
              }
            }
    * container only have one child.  
            
    2.bezel problem: use safe area.-> Alt+enter
    3. margin: Edgeinsets
    4.  * EdgeInsets.symmetric(vertical:50.0, horizontal:10.0) 
        * vertical(ups and down:50.0 , horizontal:10.0) 
        * view from: flutter ispector 
        * EdgeInsets.fromLTRB(), EdgeInsets.only(30.0),
        
    5. vertical:
     * MainAxisSize: 
     * verticalDirection
     * mainAxisAlignment
     
     6. Horizontal Axis:
      * crossAxisAlignment
      
     7. if we knew how much space need :
         Container(),
         SizedBox(height:20.0 // for column, in row need width.
         ),
         
   ### custom font in our project:
     1.  fonts.google.com -> downlod font
     2.  create a fonts directory
     3.  drop dowmload file in fonts
     4.  https://flutter.dev/docs/cookbook/design/fonts
     
     
  ### Adding metarial icon:
      https://www.materialpalette.com/
      
  ### Visibility :
  
    child: Visibility(
      visible: storyBrain.buttonShouldBeVisible(),
       )
       
    buttonShouldBeVisible is a boolean type function that returns true or false.
    
    
   ##### Editing Theme :
               1. theme: ThemeData.dark().copyWith(  // .copywith make the theme dark.
                    primaryColor: Color(0xFF0A0E21),
                    scaffoldBackgroundColor: Color(0xFF0A0E21),
                  ),
    
       
               2. theme:ThemeData(
                     primaryColor: Colors.red, // it change the appbar.
                    ),
                    
   ##### Dart borderradius:
            decoration: BoxDecoration(
          color:Color(0xff1d1e33),
          borderRadius: BorderRadius.circular(10.0),
        ),
        
   ##### Create reuseable card widget:
             use container + Flutter Outline + Extract Widget 
            
            
             Expanded(child: ReuseableCard(
                   colour:Color( 0xFF1D1E33),
                )),
                
                
                
            class ReuseableCard extends StatelessWidget {
              ReuseableCard({@required this.colour});
               final Color colour;

              @override
              Widget build(BuildContext context) {
                return Container(
                  margin: EdgeInsets.all(15.0),
                  decoration: BoxDecoration(
                      color: colour,
                      borderRadius: BorderRadius.circular(10.0)),
                );
              }
            }
         
         
   ##### Full Screen Size :
            Container(
            color:Color(0xFFEB1555),
            margin:EdgeInsets.only(top:10),
            width:double.infinity,
            height: 80.0,
          )
           
  
              
  ### press + button then we can put some input :
  
  
               void _startAddNewTransaction(BuildContext ctx) {
                showModalBottomSheet(
                  context: ctx,
                  builder: (_) {
                    return GestureDetector(
                      onTap: (){},
                      child: NewTransaction(_addNewTransaction),  // _addNewTransaction list 
                      behavior: HitTestBehavior.opaque,
                    );
                  },
                );
              }
              
              
              IconButton(
            icon: Icon(Icons.add),
            onPressed: () => _startAddNewTransaction(context),
          ),
         
         
   ### ListView:
      child: ListView.builder
      (
       itemBuilder: (ctx, index) {},
        itemCount: transactions.length,
      )
      
   ### fonts :
   
               theme: ThemeData(
                 
                   
                    fontFamily: 'OpenSans',  // this will make a global font
                    
                    textTheme: ThemeData.light().textTheme.copyWith(
                      title: TextStyle(
                        fontFamily: 'OpenSans',
                        fontWeight: FontWeight.bold,
                        fontSize: 18
                      )
                    )
                    
                    use it like this 
                       style: Theme.of(context).textTheme.title,

                   
