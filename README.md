# 修改记录


## 1.0.1

修改一下情况出现的bug


- 会替换掉所有的`/**`字符,应该是只替换第一个

错误生成示例
```kotlin

/**
 * @param a Int?=null : 
 * @param s String : 
 */
class Test(private var a: Int? = null,s:String) {
   
   /**
    * @param a Int?=null : 
    * @param s String : 
    */
    * @param a Int : 
    */
    fun Test(a: Int) {

    }

}

```

- 修复函数 参数 多行 而多余的换行符,以及`paramcurrentPage` 少了空格


```kotlin

   /**
    * @paramcurrentPage Int=0 : 
    * @param
pageSize Int=20 : 
    * @param
isInvoiced Boolean?=null : 
    * @param
observer Observer<BaseHttpBean> : 
    */
    fun listCommonwealPayHistory(currentPage: Int = 0,
                                 pageSize: Int = 20,
                                 isInvoiced: Boolean? = null,
                                 observer: Observer<BaseHttpBean>) {
      }
      

```






## 1.0.0

更改项目组成为idea默认构建,取消gradle构建
