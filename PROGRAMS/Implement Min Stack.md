class MinStack {
public:
    stack<int> st;
    stack<int> minSt;
    MinStack() {
    }
    void push(int value) {
        st.push(value);

        if (minSt.empty() || value <= minSt.top())
            minSt.push(value);
    }
    void pop() {
        if (st.top() == minSt.top())
            minSt.pop();

        st.pop();
    }
    int top() {
        return st.top();
    }
    int getMin() {
        return minSt.top();
    }
};

<img width="380" height="172" alt="image" src="https://github.com/user-attachments/assets/526a4c5a-0974-4052-93b1-3bd0ce1509f6" />

