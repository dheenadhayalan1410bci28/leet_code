/**
 * Definition for a binary tree node.
 * struct TreeNode {
 * int val;
 * struct TreeNode *left;
 * struct TreeNode *right;
 * };
 */
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
#include <stdlib.h>

void preorder_helper(struct TreeNode* node, int* result, int* index) {
    if (node == NULL) {
        return;
    }
    result[(*index)++] = node->val;
    preorder_helper(node->left, result, index);
    preorder_helper(node->right, result, index);
}

int* preorderTraversal(struct TreeNode* root, int* returnSize) {
    int max_nodes = 200; // LeetCode constraints usually specify max nodes
    int* result = (int*)malloc(max_nodes * sizeof(int));
    if (result == NULL) {
        *returnSize = 0;
        return NULL;
    }
    
    int index = 0;
    preorder_helper(root, result, &index);
    *returnSize = index;
    
    // It's good practice to reallocate to the exact size, though not strictly required
    // for this problem if constraints are small.
    // result = (int*)realloc(result, *returnSize * sizeof(int));
    return result;
}
