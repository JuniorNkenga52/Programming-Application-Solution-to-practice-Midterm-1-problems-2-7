# Programming-Application-Solution-to-practice-Midterm-1-problems-2-7
#Question 2
public static void stretch(ArrayList<String> a, int b){
  if(b>=0){
  for(int i=0; i<a.size(); i+=b){
      String x=a.get(i);
      a.remove(i);
      for(int j=0; j<b; j++){
          a.add(i,x);
      }
   }
  }else{
      int k=0;
     while(a.size()>0){
         a.remove(k);
     }
  }
}

#Question 3
public static void compressDuplicates(Stack<Integer> t){
    if(t.size()==0) return;
    Stack<Integer> b=new Stack<>();
    
    while(!t.isEmpty()){
    int count=1;
        int num=t.pop();
        while(!t.isEmpty() && t.peek()==num){
            count++;
             t.pop();
        }
        b.push(num);
         b.push(count);
   }
    while(!b.isEmpty()){
    t.add(b.pop());
    }
}

#Question 4
public static int countInAreaCode(Map<String,String> b, String x){
    Set<String> q=new TreeSet<>();
    for(String a:b.keySet()){
        if(b.get(a).startsWith(x)) {
            q.add(b.get(a));
        }
     }
    return q.size();
}
#Question 5
list.next=list2;
ListNode current=list2.next.next;
list2.next.next=null;
ListNode temp=list2.next;
list2.next=null;
current.next=list;
list=current;
list2=temp;

#Question 6
public boolean isSortedBy(int a){
    if(size()==0 || size()==1) return true;
    if(a>=size())return true;
    if(a<=0) throw new IllegalArgumentException();
    for(int j=0; j<a; j++){
     for(int i=j; i<size()-a; i+=a){
        if(get(i+a)<get(i)) return false;
     }
    }
    return true;
}
#Question 7
public int compareTo(BankAccount2 b){
  if(this.getBalance()!=b.getBalance()){
      return (int)this.getBalance()-(int)b.getBalance();
  }else if(this.getID()!=b.getID()){
      return this.getID()-b.getID();
  }else{
   return 0;   
  }
}
