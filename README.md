# Create-two-dimensional-table-headers-with-DAX

![grafik](https://user-images.githubusercontent.com/84840321/168978093-c225f6d5-e0f8-482d-a516-94fe56eb32a6.png)

Creating a two-dimensional table header can be implemented with DAX.
First you need to create a table for all titles

![grafik](https://user-images.githubusercontent.com/84840321/168978911-732e2013-bcca-497b-a98f-78bab91a8cd4.png)

Second create the corresponding measures

Third 
In Excel,You can use IF HASONEVALUE instead of SELECTEDVALUE in Power BI
werte = SWITCH (
	TRUE();

	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=1;[Measure1];	
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=2;[Measure12];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=3;[Measure13];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=4;[Measure14];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=5;[Measure15];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=6;[Measure16];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=1&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=7;[Measure17];

	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=2&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=1;[Measure18];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=2&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=2;[Measure19];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=2&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=3;[Measure10];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=2&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=4;[Measure11];


	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=3&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=1;[Measure2];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=3&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=2;[Measure3];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=3&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=3;[Measure4];
	IF(HASONEVALUE('Title'[Index]);VALUES('Title'[Index]))=3&&IF(HASONEVALUE('Title'[Sub-Index]);VALUES('Title'[Sub-Index]))=4;[Measure5]
	
	)
