# what-the-F-ck-is-this-

JSONArray jsonArray_weather = response.getJSONArray("weather");
JSONObject jsonObject_main = response.getJSONObject("main");
JSONObject jsonObject_clouds = response.getJSONObject("clouds");
wether_main.setText(jsonArray_weather.getJSONObject(0).getString("main"));
wether_description.setText(jsonArray_weather.getJSONObject(0).getString("description"));
temp.setText(jsonObject_main.getString("temp"));
min_max_temp.setText("Min. "+jsonObject_main.getString("temp_min")+"  Max. "+jsonObject_main.getString("temp_max"));
humidity.setText(jsonObject_main.getString("humidity")+"%\nHumidity");
cloud_coverage.setText(jsonObject_clouds.getString("all")+"%\nCloud");
