#include <iostream>
#include <filesystem>
#include <fstream>
#include <string>
using namespace std;

void listFiles (conts string & path) {
  cout << "Listing files in Directory": << path << endl;
  try {
     for ( conts auto & entry : directory_iterator(path)) {
       cout << entry.path().filename().string () << endl;
     }
} catch (const filesystem_error & e) {
   cout << "Error : " << e.what () << endl;
   }
}


int main(){
string Now
int choice;





reurtn 0;
}
