/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 */
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
void traverse(struct TreeNode *root, int *index, int *returnArray) {
    if (root == NULL) {
        return;
    }

    traverse(root->left, index, returnArray);

    returnArray[*index] = root->val;
    (*index)++;

    traverse(root->right, index, returnArray);
}

int countNodes(struct TreeNode *root) {
    if (root == NULL) {
        return 0;
    } 
    return 1 + countNodes(root->left) + countNodes(root->right);
}

int* inorderTraversal(struct TreeNode* root, int* returnSize) {
    *returnSize = countNodes(root); 
    int *returnArray = malloc((*returnSize) * sizeof(int));
    int index = 0;
    traverse(root, &index, returnArray);
    return returnArray;
}
