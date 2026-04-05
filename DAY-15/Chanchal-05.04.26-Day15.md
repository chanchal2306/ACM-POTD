# Solution

class Solution {
public:
    bool isValid(string s) {
        stack<char> par;

        for (char c : s){
            if (c == '('){
                par.push(')');
            }
            else if ( c == '{'){
                par.push('}');
            }
            else if ( c == '['){
                par.push(']');
            }
            else if (  par.empty() || par.top() != c) {
                return false;
            }
            else{
                par.pop();
            }
        }
        return par.empty();    
    }

};