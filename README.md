# code_day

数组，栈

2022 Nov 1st

leecode 989: 数组形式整数加法
注意边界，整数和数组长度关系。

leecode 414: 第三大的数
sort reverse 注意有相等情况

leecode 821: 字符串的最小距离
先找到字母的位置，求出所有可能的距离，最后找最小值。
（这可能是最tm烂的答案了，还得多练。。。。
class Solution:
  def shortestToChar(self, s:str, c:str)->List[int]:
    result=[]
    c_position=[]
    for i in range(len(s)):
      if s[i]==c:
          c_position.append(i)
    for i in c_position:
      for j in range(len(s)):
        dis=abj(j-i)
        result.append(dis)
    result = np.array(result)
    result = result.reshape(-1,len(s))
    result1 = np.min(result,axis=0)
    result = result1.tolist()
    return result
    
