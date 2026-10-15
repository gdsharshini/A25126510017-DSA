class Solution {
public:
    void inorder(TreeNode* root, vector<int>& result) {
        if (root == NULL) {
            return;
        }

        inorder(root->left, result);
        result.push_back(root->val);
        inorder(root->right, result);
    }

    vector<int> inorderTraversal(TreeNode* root) {
        vector<int> result;
        inorder(root, result);
        return result;
    }
};


<img width="210" height="83" alt="inorder traversal" src="https://github.com/user-attachments/assets/a21b48d8-aac1-4349-8e5f-ca96ca10418b" />
