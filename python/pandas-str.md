## 문제
- 수정 방법: 문자열 값에는 .str 접근자만 사용할 수 있습니다.

## 해결
> [참고자료](https://www.statology.org/can-only-use-str-accessor-with-string-values/)


```python
 #   Column        Non-Null Count  Dtype         
---  ------        --------------  -----         
 0   show_id       8807 non-null   object        
 1   type          8807 non-null   object        
 2   title         8807 non-null   object        
 3   director      6173 non-null   object        
 4   cast          7982 non-null   object        
 5   country       7976 non-null   object        
 6   date_added    8797 non-null   datetime64[ns]
 7   release_year  8807 non-null   int64         
 8   rating        8803 non-null   object        
 9   duration      8804 non-null   object        
 10  listed_in     8807 non-null   object        
 11  year          8797 non-null   float64       
 12  month         8797 non-null   float64  

cond1 = df["date_added"].astype("str").str.contains("2018")
cond2 = df["date_added"].astype("str").str.contains("January")
```
