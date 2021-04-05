# Will-it-be-jacket-or-T-shirt-
This project uses API Open Weather Map

Summary:
This project uses API Open Weather Map. The intention of this project is to be able to know what to wear within a 5 day period. The weather's temperature is provided every three hours. The location where the weather is being observed is in the Rockville, MD with zip code 20850. The units in the temperature was change from the default which is a standard to imperial. The data was gathered from the period of Oct. 5, 2020 to Oct. 10, 2020. 

Now that the weather is changing from summer to fall. The weather is getting cooler. The t-shirt and shorts attire is being replaced to long-sleeved shirts and long pants with light jacket. Leaving the house unprepared for the weather will either make ourselves too warm or too cold.

Data Description, Analysis, Rationale and Conclusion
Requests, pandas, and json were used in this project. For loops are used to gather temperature, date, and description of the data. Initialy, the data type of the different data are as follows: Date: object, Description: object, Temperature: float. The date was converted to datetime 64 data type and was split into time and date. Eventually, the date and time data became object data. The data are appended and put into a data frame. 

The weather data on the temperature is described, so information on the maximum and minimum temperature are generated. The weather data is also sorted. After sorting, the first 5 warmest time and date are gathered as well as the last 5 coldest time and date is also gathered. Knowing the warmest and coldest dates and times allow a person to prepare what clothes to wear during the 5 days period. The description of the weather indicates if a person is to prepare for rain or snow clothing.

Using the mathplotlib, a box plot is created. Information gathered from this plot is that the temperature is very stable but slowly shifting. There is no eratic weather changes because there is no outliers.

Based on the data, the morning and noon of Oct 9 are the coldest in the 5 day forecast while the night of Oct 6 and 7 are warmest.  The rationale that morning was warmer than evening and afternoon does not hold true to this data. There is a slow shift of weather temperature because the fall weather is slowly dawning upon us. 

The weather plays an important role in the clothing that we choose. For the early week of October, my personal preference is a light jacket, short sleeve shirt, and long pants. However, for those who like cooler weather, short sleeve and short pants can still be the clothing of choice.

Limitations and Further Research
This project gives a weather forecast every 3 hours for 5 days. It has 40 indexes because everyday there are 8 indexes multiply by 5 days. It is known that weather changes can be abupt, so weather can be very unpredictable. Constant updates could be helpful. However, the closer to the time of the forecast gives a better idea what the weather will be truly like.

Summary of the folders/files in the repo
HW2 Will it be jacket or T-shirt is a github repo folder. The folder will contain HW2 API Open Weather Map, ReadMe, and License. HW2 API Open Weather Map is the name of the Jupyter file. From HW2 API Open Weather Map, a data.cvs can be generated. This data.cvs is a file where information of weather data that has the date and time separated.

References
Open Weather Map. Map. Open Weather Ltd. By Denn Ukolov and Olga Ukolova. London: 5 Oct 2020 <http://api.openweathermap.org/data/2.5/forecast?zip=20850,us&units=imperial&appid=d7bb4169bffbbdccbe072168d0db38e7>





