QUES. **create a table st\_info with 3 subjects and calculate total and %age.**



ANS. 



create table st\_info(PRN int, name varchar2(20), S1 int,S2 int,S3 int);



insert into st\_info values(101,"XYZ",88,90,77); **#error**



*# double quotes (" ") are for column or table names, not for text values.*



insert into st\_info values(101,'abc',88,90,77);



select \* from st\_info;



\#but u forgot to add total and percentage ;



alter table st\_info add total number;



alter table st\_info add perc number;



**# shows the structure of table**.



desc st\_info; 



insert into st\_info values(101,"XYZ",88,90,77,null,null);

or 



**#multiple data together:**



insert into st\_info(PRN, name,S1,S2,S3) values(101,'XYZ',88,90,77);

insert into st\_info(PRN ,name,S1,S2,S3) values(101,'TCQ',88,90,77);

insert into st\_info(PRN ,name,S1,S2,S3) values(101,'ABC',88,90,77);



\#**to calculate total \& percent we used update command:**



update st\_info set total = s1+s2+s3;



\#to update multiple cols .



update st\_info  set total = S1+S2+S3,

&nbsp;                   perc = total / 3;





**#drop table :**

**s**

drop table st\_info;



**#to delete all rows and cols i.e date in the table** 



truncate table st\_info;







