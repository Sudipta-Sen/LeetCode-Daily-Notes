#  [LeetCode 3203 - Find Minimum Diameter After Merging Two Trees](https://leetcode.com/problems/find-minimum-diameter-after-merging-two-trees/description/) 

## Concept: Finding Diameter in an N-ary Tree

### Key Approach:
- Definition: The diameter of an N-ary tree is the longest path between any two nodes in the tree.
- YouTube Link: [Click Here](https://www.youtube.com/watch?v=vTcQjheqTVs)
- Steps:
    1. Start from any random node in the N-ary tree.
    2. Perform a DFS or BFS to find the node that is the farthest from this starting node.
    3. From the furthest node found in step 2, perform another DFS or BFS to find the furthest node from it.
    4. The distance between these two nodes is the diameter of the tree.

### Why This Works:
- The first search helps identify one end of the longest path in the tree.
- The second search ensures we find the other end of this longest path.

### Complexity:
- **Time Complexity:** `O(n)` where `n` is the number of nodes in the tree.
- **Space Complexity:** `O(h)` where `h` is the height of the tree due to the recursion stack in DFS.