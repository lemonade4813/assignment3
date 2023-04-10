# 과제3

DB 경로 : database-1.cgsqdm8ubkh3.ap-northeast-2.rds.amazonaws.com
Database : mysql
PORT : 3306
user : admin
password : password

![image](https://user-images.githubusercontent.com/103189961/230875491-2864a115-f0b7-41b3-901a-6a8844eaf6fd.png)

### * 사전 진행

(1) product_order 테이블

![image](https://user-images.githubusercontent.com/103189961/230875947-c2c9d4c9-40bf-4227-af5b-dab77188d19f.png)


(2) insert 쿼리로 테이블에 데이터를 삽입했습니다.
insert into product_order (date) values 

('2023-03-04 13:47:11.000')
,('2023-03-04 13:47:11.000')
,('2023-03-04 14:44:17.000')
,('2023-03-07 18:36:03.000')
,('2023-03-07 18:36:03.000')
,('2023-03-08 16:49:10.000')
,('2023-03-11 14:05:44.000')
,('2023-03-11 14:05:44.000')
,('2023-03-12 18:46:47.000')
,('2023-03-12 18:46:47.000')
,('2023-03-12 18:46:47.000')
,('2023-03-13 10:10:35.000')
,('2023-03-13 10:10:35.000')
,('2023-03-13 10:10:35.000')
,('2023-03-13 10:15:01.000')
,('2023-03-13 13:30:41.000')
,('2023-03-13 18:23:01.000')
,('2023-03-13 18:23:01.000')
,('2023-03-13 18:23:01.000')
,('2023-03-13 18:28:26.000')
,('2023-03-13 18:28:26.000')
,('2023-03-13 18:28:26.000')
,('2023-03-14 08:30:55.000')
,('2023-03-14 08:30:55.000')
,('2023-03-14 08:30:55.000')
,('2023-03-14 08:30:55.000')
,('2023-03-14 10:01:56.000')
,('2023-03-14 10:01:56.000')
,('2023-03-20 10:05:28.000')
,('2023-03-20 10:05:28.000')
,('2023-03-20 10:05:28.000')
,('2023-04-04 13:27:22.000')
,('2023-04-04 13:27:22.000')
,('2023-04-05 16:54:33.000')
,('2023-04-05 19:46:03.000')

1) 특정 선택일자( 예: 2023년7월7일) 데이터만 선택해서 내림차순으로 보여준다고 할 경우
의 SQL를 작성해 주세요.

select date  from product_order po where DATE_FORMAT(date, '%Y-%m-%d') = '2023-03-13' order by date desc;

![image](https://user-images.githubusercontent.com/103189961/230880314-0d2d2185-52ae-419d-93fc-8428d3bca2c0.png)

2) 금일 날짜의 데이터만 선택하여 오름차순으로 보여야 할 경우의 SQL를 작성해 주세요.

select date  from product_order po where DATE_FORMAT(date, '%Y-%m-%d') = CURDATE()  order by date asc;

![image](https://user-images.githubusercontent.com/103189961/230880799-8a5a0ffe-db94-4cf3-b2df-ac8435c0e973.png)


