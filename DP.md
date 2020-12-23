### 12.23 Wed
重新开刷。

Jump Game  
m[i]: represents 能否从开头跳到 i  
但我那种方法是错的，（set 了将来的 m[i+xx]），穿越了，穿越到将来，但是站在 i 是不知道未来的。  
只能 leaner scan 回头看，看我基于过去的信息，能否到达今天这个点  
Greedy 难证明，不建议面试时使用。  
DP：
- 基于过去已有的信息，确定现在；  
- 不能再改过去的信息，也不能预知将来的事情，只能把握现在。  

不对，我这种方法是对的，何必每次都查一遍呢？  

```java 
public boolean Jump(int[] array) {
  boolean[] m = new boolean[array.length];
  m[0] = true;
  for (int i = 0; i < array.length; i++) {
      if (m[i] == false) {
        continue;
      }
      for (int j = i+1; j <= Math.min(array.length-1, i + array[i]); j++) {
        m[j] = true;
      }
  }
  return m[array.length-1];
}

```


