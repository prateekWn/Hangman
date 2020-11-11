#include<iostream>
#include<fstream>
#include<vector>
#include<ctime>

using namespace std;

void printmessage(string message, bool top = true, bool bottom = true){
    
    if(top){
        cout<<"+----------------------------------------------+"<<endl;
        cout<<"|";
    }
    else{
        cout<<"|";
    }

    bool space = true;

    for(int i = message.length(); i<46; i++){

        if(space)
            message = " " + message;
        
        else
            message = message + " ";
        
        space = !space;

    }

    cout<<message;

    if(bottom){
        
        cout<<"|"<<endl;
        cout<<"+----------------------------------------------+"<<endl;
        
    }
    else{
        cout<<"|"<<endl;
    }

}

void dyingMan(int guessCount = 0){

    if(guessCount >= 1)
        printmessage("|", false, false);
    else
        printmessage("",false, false);


    if(guessCount >= 2)
        printmessage("|", false, false);
    else
        printmessage("",false, false);


    if(guessCount >= 3)
        printmessage("o", false, false);
    else
        printmessage("",false, false);


    // if(guessCount == 4)
    //     printmessage("/", false, false);

    // if(guessCount == 5)
    //     printmessage("/|", false, false);
    

    if(guessCount >= 4)
        printmessage("/|\\", false, false);
    else
        printmessage("",false, false);


    if(guessCount >= 5)
        printmessage("|", false, false);
    else
        printmessage("",false, false);


    // if(guessCount == 8)
    //     printmessage("/ ", false, false);


    if(guessCount >= 6)
        printmessage("/ \\", false, false);
    else
        printmessage("",false, false);    


    if(guessCount >= 7)
        printmessage("+----------+", false, false);
    else
        printmessage("",false, false);

    if(guessCount >= 8)
        printmessage("|          |", false, false);
    else
        printmessage("",false, false);

}

void displayLetters(string input, char from, char to){

    string s;

    for(char i = from; i<=to; i++){

        if(input.find(i) == string::npos)
        {
            s = s + i + "  ";
            // s += "  ";
        }
        else
            s += "  ";
    }

    

    printmessage(s , false , false);
}

void callTheGuessing(string guess){

    printmessage("AVAILABLE LETTERS");
    
    displayLetters(guess , 'A' , 'M');
    
    displayLetters(guess , 'N' , 'Z');

    printmessage("GUESS THE WORD");
}

bool checkTheWord(string word, string guess){

    bool won = true;

    string s;

    for(int i = 0; i<word.length(); i++){

        if(guess.find(word[i]) == string::npos)
        {
        
            s = s + "_ ";

            won = !won;
        
        }
        
        else
        
            s = s + word[i] + " ";
    
    }

    printmessage(s, false);

    return won;

}

string loadWordsFromFile(string path){

    int countLine = 0;

    vector<string> v;
    
    ifstream readPath(path);

    if(readPath.is_open()){

        // while()
    }


}

int main(){

    string guess = "GURISHA";

    printmessage("HANG MAN");

    dyingMan(11);

    callTheGuessing(guess);

    checkTheWord("PRATEEK" , guess);

    return 0;
}
