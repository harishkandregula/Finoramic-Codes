# Finoramic-Codes Code to root to leaf path with sum.
#include<iostream>
#include<stdlib.h>
#include<bits/stdc++.h>
#include<vector>
using namespace std;
struct Node
{
    int key;
    struct Node *left, *right;
};
Node* newNode(int key)
{
    Node* temp = new Node;
    temp->key = key;
    temp->left = temp->right = NULL;
    return (temp);
}
 
 void printPathsUtil(Node* curr_node, int sum,
             int sum_so_far, vector<int> &path)
{
    if (curr_node == NULL)
        return;
 
    sum_so_far += curr_node->key;
 
    path.push_back(curr_node->key);
 
    if (sum_so_far == sum )
    {
        cout << "Path found: ";
        for (int i=0; i<path.size(); i++)
            cout << path[i] << " ";
 
        cout << endl;
    }
 
    if (curr_node->left != NULL)
        printPathsUtil(curr_node->left, sum, sum_so_far, path);

    if (curr_node->right != NULL)
        printPathsUtil(curr_node->right, sum, sum_so_far, path);
    path.pop_back();
}
void printPaths(Node *root, int sum)
{
    vector<int> path;
    printPathsUtil(root, sum, 0, path);
}
int main()
{
  Node *root  = newNode(5);
    root->left  = newNode(4);
    root->right = newNode(8);
 
    root->left->left   = newNode(11);
    root->left->left->left  = newNode(7);
    root->left->left->right = newNode(2);
    
    root->right->right = newNode(4);
    root->right->left = newNode(13);
 
    root->right->right->left   = newNode(5);
    root->right->right->right  = newNode(1);
 
    int sum = 22;
 
    printPaths(root, sum);
 
    return 0;
}
