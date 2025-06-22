```
#include<vector>
#include<string>
#include<unordered_map>
#include<algorithm>
#include<iostream>
using namespace std;

using vecStr = vector<string>;
vector<pair<string,int>> fun(vecStr& dic) {
    unordered_map<string, int> um;
    vector<pair<string,int>> out;

    //Count anagrams after sort
    for (auto i:dic){
        sort(i.begin(), i.end());
        um[i]++;
        //um will have
        //art:3, act:1, bsu:1
    }

    //Search word inside map after sort
    for (auto i:dic){
        string word = i;
        sort(i.begin(), i.end());
        auto it = um.find(i);
        if (it != um.end()){
            int count = it->second;
            out.push_back({word, count-1});
        }
    }
    return out;
}

int main() {
    //output:
    //rat:2, cat:0, bus:0, art:2, tar:2
    //rat,art,tar are anagrams
    vector<string> dictionary = {"rat", "cat", "bus", "art", "tar"};
    vector<pair<string,int>> out = fun(dictionary);
    for (auto i:out){
        cout << i.first << "," << i.second;
    }
}
```
