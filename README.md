class UnusualAdd {
public:
    int addAB(int A, int B) {
        // write code here
        int sum=A;
        while(B!=0)
        {
            sum=A^B;
            B=(A&B)<<1;
            A=sum;
        }
        return sum;
    }
};
