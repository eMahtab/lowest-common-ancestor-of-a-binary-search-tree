# Lowest Common Ancestor of a Binary Search Tree (BST)
### https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree

Given a binary search tree (BST), find the lowest common ancestor (LCA) of two given nodes in the BST.

According to the definition of LCA on Wikipedia: "The lowest common ancestor is defined between two nodes p and q as the lowest node in T that has both p and q as descendants (where we allow a node to be a descendant of itself)."

```
Note:

1. All of the nodes' values will be unique.
2. p and q are different and both values will exist in the BST.
```

## Implementation :

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode lowestCommonAncestor(TreeNode root, TreeNode p, TreeNode q) {
        if(root == null)
            return null;
        if(p.val < root.val && q.val < root.val){
            return lowestCommonAncestor(root.left, p, q);
        } else if(p.val > root.val && q.val > root.val){
            return lowestCommonAncestor(root.right, p, q);
        }
        return root;
    }
}
```

# References :
https://www.youtube.com/watch?v=kulWKd3BUcI
