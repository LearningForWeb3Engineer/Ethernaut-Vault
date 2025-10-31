# Ethernaut-Vault
Ethernaut Vault解題思路

<img width="1588" height="674" alt="image" src="https://github.com/user-attachments/assets/9bbe83d6-7d58-42bb-91ce-8ae3e980fe4f" />

***這題主要是在說private只能保證這個變數不被其他合約存取，但還是可以靠查詢slot找到裡面的內容***


這題看起來就只是要找出答案並且回傳給unlock函式而已，但是我們也不可能一個一個慢慢猜，所以就可以利用web.eth.getStorageAt()找到藏在裡面的slot槽的答案。


找到之後就可以呼叫unlock回傳就可以提交答案。

所以並不是只要加上了private就很安全，這只是在限制合約跟合約之前沒辦法互相access而已，不然隨便一個有心人都可以輕易取得密鑰，這樣你的資料隱私就會蕩然無存


zk-SNARKs 提供了一個可以驗證是否某使用者 A 有某一個秘密(secret)的方法，但是驗證的過程中又不需要揭露這個秘密。

