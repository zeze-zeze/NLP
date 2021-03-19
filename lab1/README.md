# N-Gram model

## 課程資訊
* [spec](https://docs.google.com/presentation/d/1bbLf33uwLiP1JxGaeaivT997bsozRlJNDoZbm2mM9lc/edit#slide=id.gc848a1df39_0_11)
* [TODO](https://colab.research.google.com/drive/1HkDuHOl6ca2HsRs-WMjNwM76-DIBRStn?authuser=2#scrollTo=h17uKROx-FZG)
* [問題討論](https://hackmd.io/CIZaBgt5QAqzSb5JuKICGQ?view)

## 原理
計算在前 N-1 個詞的情況下，會出現的每個詞的機率，接著排序，預測時就把機率最大的那個取出來

## 步驟
1. 前處理: 把特殊字元全都過濾掉、句子前候補 \<s>、<\s>
2. 每 N-1 個詞一組為一個，和每 N 個詞為一組，分別計算兩者的數量
3. 算前 N-1 個詞的情況下，出現下一個詞為某一個詞的機率
4. 預測時看 model 中有沒有規定的前綴詞，有的話就回傳有最大機率的詞；沒有的話就報錯
