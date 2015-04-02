# AVL-Tree
AVL Dynamic Link Library

/* API of manipulation to Avl tree */

/* 1. Create avl tree with node comparsion function. (void*)key is the pointer of user-defined element that needs to be stored in AVL tree, and some elements in (void*)key are used to act as index of node in the tree. */

void* creatAvlTree(COMPARE_AVLNODE compareFunc);

/* 2. Insert an element into AVL tree. (void*)key is the pointer of user-defined structure that stores information. */

avl_ret insertIntoAvlTree(void* avlTreeVar, void* key);

/* 3. Delete an element from AVL tree. */

avl_ret deleteFromAvlTree(void* avlTreeVar, void* key);

/* 4. Retrieve an element from AVL tree. Use some elements in (void*)key and get whole information back. */

void* findFromAvlTree(void* avlTreeVar, void* key);

/* 5. Delete the whole AVL tree. */

void deleteAvlTree(void* avlTreeVar);

/* Other definitions. */

typedef int (*COMPARE_AVLNODE)(void* key1, void* key2);

typedef enum{
    AVL_SUCCESS = 0,
    AVL_FAILURE
}avl_ret;
