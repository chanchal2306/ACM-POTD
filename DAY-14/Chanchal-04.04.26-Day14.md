## Solution

class Solution {
    ListNode *front;
public:
    bool recursivelyCheck(ListNode *current ){
            if(current== nullptr){
                return true;
            }
            bool res = recursivelyCheck(current -> next);
            if (!res){
                return false;
            }
            if (front -> val != current -> val){
                return false;
            }
            front = front -> next;
            return true;
        }

    bool isPalindrome(ListNode* head) {
    front= head;
    return recursivelyCheck(head);
    }
        
};