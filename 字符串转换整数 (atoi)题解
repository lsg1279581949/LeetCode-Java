class Solution {
    public int myAtoi(String s) {
        //转换为数组
        char[] chars=s.toCharArray();
        //计算字符总数
        int n=chars.length;
        //初始化idx
        int idx=0;
        //判断前导空格
        while(idx<n && chars[idx]== ' ')
        {
            idx++;
        }
        //判断是否为越界
        if(idx==n)
        {
            return 0;
        }
        //正负号标志位
        boolean negative=false;
        //正负号以及非数字判断
        if(chars[idx]=='-')
        {
            negative=true;
            idx++;
        }else if(chars[idx]=='+')
        {
            idx++;
        }else if(!Character.isDigit(chars[idx])){
            return 0;
        }
        //初始化返回的数值
        int ans=0;
        while(idx<n && Character.isDigit(chars[idx]))
        {
            //把字符转换为正数
            int digit=chars[idx]-'0';
            //防止越界
            if(ans>(Integer.MAX_VALUE-digit)/10){
                return negative?Integer.MIN_VALUE:Integer.MAX_VALUE;
            }
            //进位相加
            ans=ans*10+digit;
            //下标相加
            idx++;
        }
        //最后返回结果
        return negative?-ans:ans;



    }
}
