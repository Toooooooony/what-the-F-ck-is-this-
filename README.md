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


System.out.println("\n  w "+r.get("weather"));
System.out.println("des "+r.get("weather_description"));
System.out.println("tem "+r.get("temp"));
System.out.println("hum "+r.get("humidity"));
System.out.println("temp_min "+r.get("temp_min"));
System.out.println("temp_max "+r.get("temp_max"));
System.out.println("clouds "+r.get("clouds"));
