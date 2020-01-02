# c_plus_plus_tools
demo for json.hpp
~~~
#include "json.hpp"
#include <string>
#include <iostream>
#include <fstream>
 
using namespace std;
using json = nlohmann::json;

int main(){
  json item;
  item["name"] = "name";
  item["name"]["cls"] = "cls";
  item["nothing"] = {"some", 123};
  json temp;
  temp["item"] = item;
  
  string jsonFile = "demo.json";
  ofstream outFile(jsonFile);
  outFile << setw(4) << temp << endl;
  cout << item.dump(4) << endl;
  return 0;
}
~~~
