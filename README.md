# nodejs_backend_example2(Postman)


## API測試(1)-Register

* HTTP Method: POST
* URL:http://localhost:3000/member
* Body(x-www-form-urlencoded):
  * name: test
  * email: test@gmail.com
  * password: test

## API測試(2)-Log In

* HTTP Method: POST
* URL:http://localhost:3000/member/login
* Body(x-www-form-urlencoded):
  * email: test@gmail.com
  * password: test
ps. headers 有token哦

## API測試(3)-Modify 

* HTTP Method: PUT
* URL:http://localhost:3000/member
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上剛剛登入取得的token
* Body(x-www-form-urlencoded):
  * name: test123123
  * password: test

## API測試(4)-Modify Image

* HTTP Method: PUT
* URL:http://localhost:3000/updateimg
* Headers:
  * Content-Type: application/form-data
* Body(form-data):
  * name: test123123
  * password: test
  * file: test.png(隨意上傳一張做測試)

## API測試(5)-Get Product Data

* HTTP Method: GET
* URL:http://localhost:3000/product

## API測試(6)-Order Multi thins

* HTTP Method: POST
* URL:http://localhost:3000/order
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上剛剛登入取得的token
* Body(x-www-form-urlencoded):
  * productID: 1,2
  * quantity: 3,4
  
## API測試(7)-Get Order All Data

* HTTP Method: GET
* URL:http://localhost:3000/order
* Headers:
  * token: 貼上剛剛登入取得的token

## API測試(8)-Get Order One Data(只能查該用戶自己的訂單)

* HTTP Method: GET
* URL:http://localhost:3000/order/member
* Headers:
  * token: 貼上剛剛登入取得的token
  
## API測試(9)-Modify Order List

* HTTP Method: PUT
* URL:http://localhost:3000/order
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上有訂單的會員的token
* Body(x-www-form-urlencoded):
  * orderID: 1
  * productID: 1
  * quantity: 5

## API測試(10)-Delete Order List

* HTTP Method: DELETE
* URL:http://localhost:3000/order
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上有訂單的會員的token
* Body(x-www-form-urlencoded):
  * orderID: 2
  * productID: 1,2(這裡改成1就可以只刪除一筆資料)
  
## API測試(11)-Order One Thing

* HTTP Method: POST
* URL:http://localhost:3000/order/addoneproduct
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上會員的token
* Body(x-www-form-urlencoded):
  * orderID: 1
  * productID: 3
  * quantity: 2
  
## API測試(12)-Confirm Order and Sent Mail

* HTTP Method: PUT
* URL:http://localhost:3000/order/complete
* Headers:
  * Content-Type: application/x-www-form-urlencoded
  * token: 貼上會員的token
* Body(x-www-form-urlencoded):
  * orderID: 1

