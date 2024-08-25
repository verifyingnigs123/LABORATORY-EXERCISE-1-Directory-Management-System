#include <iostream>
#include <fstream>
#include <string>

namespace fs = std::filesystem;
using namespace std;

void listFiles (const string & path) {
  cout << "Listing files in Directory": << path << endl;
  try {
     for ( const auto & entry fs::directory_iterator(path)) {
       cout << entry.path().filename().string () << endl;
     }
} catch (const fs::filesystem_error & e) {
   cout << "Error : " << e.what () << endl;
   }
}
void createDirectory (const string & path) {
    cout << "Creating Directory: " path << endl;
    try {
       if (fs::create_directory:(path)) {
          cout << "Directory created successfully."<<endl;
}  else {
         cout << "Failed to creat directory. It may already exist. << endl;
         }
     }catch (const fs¹:: filesystem_error& e ) {
         cout << "Error:" << e.what() << endl;
     }
  }
     void changeDirectory (string & currentPath, const string& newPath){
     cout << "Changing directory to:" << newPath << endl;
     try{
          fs::current_path(newPath);
          currentPath = fs::current_path().string ();
          cout << "Current working directory:" << currentPath << endl;
       } catch (const fs:: filesystem_error& e ) {
          cout << "Error:" << e.what() << endl;
      }
  }
  void showMenu () {
       cout << "\n Menu:\n";
       cout << "1. List Files <<endl;
       cout << "2. Creat Directory <<endl;
       cout << "3. change Directory <<endl;
       cout << "4.Exit <<endl;
       cout << "Enter your choice:";
   }   
int main(){
string currentPath = fs::current_path().string();
int choice;

do {
    showMenu();
    cin >> choice;
     switch (choice) {
       case 1: {
            listFiles(currentPath);
            break;
          }
          case 2: {
             string newDir;
             cout << "Enter the name of the new directory:";
             cin >> newDir;
             createDirectory (currentPath + "/" + newDir);
             break;
          case 3: { 
             string newPath;
             cout << "Enter the path to change to:";
             cin >> newPath;
             creatDirectory (currentPath, newPath);
          break;
        }
          case 4:{
          cout << "Enter Exits"<<endl;
          break;
          }
       default:{
       cout<< "Invalide choice. Please try again"<< endl;
       break;
       }
    }

  }while(cioice !=4);
          
          
reurtn 0;
}
