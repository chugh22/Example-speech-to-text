# Example-Text-to-Speech
Example use of text to speech api

### Code snippet
```java
public void speechToText(){
           /* RecognizerIntent.ACTION_RECOGNIZE_SPEECH
                          * Start an activity that will prompt the user  ,
                            for speech and send it through speech recognizer .

                          * Intent can be passed as startActivityforResult() or pending intents

                          * Intent cannot be passed as startActivty() */
         Intent i = new Intent(RecognizerIntent.ACTION_RECOGNIZE_SPEECH) ;
         i.putExtra(RecognizerIntent.EXTRA_LANGUAGE_MODEL , RecognizerIntent.LANGUAGE_MODEL_FREE_FORM) ;
         i.putExtra(RecognizerIntent.EXTRA_LANGUAGE , Locale.getDefault()) ;
         i.putExtra(RecognizerIntent.EXTRA_PROMPT , "Say Something ......") ;
         try{
             startActivityForResult(i ,SPEECH_REQUEST_CODE);
         }catch (ActivityNotFoundException anfe){
             Toast.makeText(this , "Activity not found exception" ,Toast.LENGTH_SHORT ).show();
         }

     }
 ```



