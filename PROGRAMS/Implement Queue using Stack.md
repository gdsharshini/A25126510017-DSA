#include <stack>
using namespace std;

class MyQueue {
private:
    stack<int> input;
    stack<int> output;

    
    void transfer() {
        if (output.empty()) {
            while (!input.empty()) {
                output.push(input.top());
                input.pop();
            }
        }
    }

public:
    MyQueue() {
        
    }
    
   
    void push(int x) {
        input.push(x);
    }
    
    
    int pop() {
        transfer();
        int val = output.top();
        output.pop();
        return val;
    }
    
    
    int peek() {
        transfer();
        return output.top();
    }
    
    
    bool empty() {
        return input.empty() && output.empty();
    }
};

<img width="387" height="181" alt="image" src="https://github.com/user-attachments/assets/1607132e-f709-4b4d-8787-f7f6a6eab4d2" />

