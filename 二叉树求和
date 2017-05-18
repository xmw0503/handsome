/**
 * Definition of TreeNode:
 * class TreeNode {
 * public:
 *     int val;
 *     TreeNode *left, *right;
 *     TreeNode(int val) {
 *         this->val = val;
 *         this->left = this->right = NULL;
 *     }
 * }
 */
class Solution {
public:
    /**
     * @param root the root of binary tree
     * @param target an integer
     * @return all valid paths
     */
    void hanshu(TreeNode *root, int target, vector<vector<int>>& a, vector<int>& b){
        if(root==NULL){
            return;
        }
        b.push_back(root->val);
        if(target==root->val&&root->right==NULL&&root->left==NULL){
            a.push_back(b);
            b.pop_back();
            return;
        }
        hanshu(root->right,target-(root->val),a,b);
        hanshu(root->left,target-(root->val),a,b);
        b.pop_back();
    }
    vector<vector<int>> binaryTreePathSum(TreeNode *root, int target) {
        // Write your code here
        vector<vector<int>> a;
        vector<int> b;
        if(root==NULL){
            return a;
        }
        b.push_back(root->val);
        if(root->right==NULL&&root->left==NULL&&root->val==target){
            a.push_back(b);
        }
        hanshu(root->right,target-(root->val),a,b);
        hanshu(root->left,target-(root->val),a,b);
        return a;
    }
};
