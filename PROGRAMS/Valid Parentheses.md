class Solution {
public:
    bool isValid(string s) {
        stack<char> st;
        
        for (char c : s) {
          
            if (c == '(' || c == '{' || c == '[') {
                st.push(c);
            } 
           else {
                
                if (st.empty()) return false;
                
                char top = st.top();
                st.pop();
                
               
                if ((c == ')' && top != '(') ||
                    (c == '}' && top != '{') ||
                    (c == ']' && top != '[')) {
                    return false;
                }
            }
        }
        return st.empty();
    }
};

<img width="420" height="122" alt="image" src="https://github.com/user-attachments/assets/81e1b7e3-ef3f-4544-8de2-e6b0306b4963" />

