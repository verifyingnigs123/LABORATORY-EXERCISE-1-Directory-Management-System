#include <iostream>
#include <filesystem>
#include <fstream>
#include <string>

name space fs = std::filesystem;
using namespace std;

void listFiles (conts string & path) {
  cout << "Listing files in Directory": << path << endl;
  try {
     for ( conts auto & entry :fs::directory_iterator(path)) {
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
     }catch (const fs :: filesystem_error& e ) {
         cout << "Error:" << e.what() << endl;
     }
  }
     void changeDirectory (string & currentPath, const string& newPath){
     cout << "Changing directory to:" << newPath << endl;
     try{
          fs::current_path(newPath);
          currentPath = fs::current_path().string ();
          cout << "Current working directory
  

     
int main(){
string Now
int choice;





reurtn 0;
}
