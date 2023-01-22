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
