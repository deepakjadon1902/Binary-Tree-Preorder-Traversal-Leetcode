class Solution {
    List<Integer> result = new ArrayList<>();
    public List<Integer> preorderTraversal(TreeNode root) {
        preOrder(root);
        return result;
    }

    private void preOrder(TreeNode node){
        if(node == null){
            return;
        }

        result.add(node.val);
        preOrder(node.left);
        preOrder(node.right);
    }
}
