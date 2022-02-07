struct Node* reverseList(struct Node *head)
    {
        // code here
        // return head of reversed list
        if(head==NULL && head->next==NULL)
        {
            return head;
        }
        Node* t=head;
        Node* p=NULL;
        Node* f=NULL;
        while(t)
        {
            f=t->next;
            t->next=p;
            p=t;
            t=f;
        }
        return p;
    }
