CREATE TABLE IF NOT EXISTS `d_purchase` (
  `order_id` bigint(20) NOT NULL AUTO_INCREMENT,![image](https://user-images.githubusercontent.com/82856473/123732261-963a4680-d8d4-11eb-947b-4c6129d0c1cc.png)
`customer_code` varchar(50) NOT NULL,
  `purchase_date` date NOT NULL,
  `total_price` int(11) NOT NULL,
  PRIMARY KEY (`order_id`)
)
![image](https://user-images.githubusercontent.com/82856473/123732286-a2260880-d8d4-11eb-910a-d871cdd975d9.png)

