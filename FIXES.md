In Snowflake views relied on MarketPlace Data.  The name of the company changed so the view broke.  

Changed from WEATHER_SOURCE_LLC_FROSTBYTE:
```diff 
+ FROM PELMOREX_WEATHER_SOURCE_FROSTBYTE.onpoint_id.history_day hd
+ JOIN PELMOREX_WEATHER_SOURCE_FROSTBYTE.onpoint_id.postal_codes pc
- FROM WEATHER_SOURCE_LLC_FROSTBYTE.onpoint_id.history_day hd
- JOIN WEATHER_SOURCE_LLC_FROSTBYTE.onpoint_id.postal_codes pc
```

Also note my branches has / in them Snowflake does not like that. 

```shell
git branch -m setup/init setup-init
git push origin setup-init
git push origin --delete setup/init
```

Then on Snow cli
```shell
snow git fetch advanced_data_engineering_snowflake --database=COURSE_REPO --schema=PUBLIC --connection advanced_data_engineering_snowflake
```
