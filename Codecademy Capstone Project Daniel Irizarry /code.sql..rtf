{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf600
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;\f1\froman\fcharset0 TimesNewRomanPSMT;}
{\colortbl;\red255\green255\blue255;\red72\green72\blue72;}
{\*\expandedcolortbl;;\csgenericrgb\c28235\c28235\c28235;}
\margl1440\margr1440\vieww28600\viewh15140\viewkind0
\deftab720
\pard\pardeftab720\ri0\partightenfactor0

\f0\fs26 \cf2 --1. How many campaigns and sources does CoolTShirts use? Which source is used for each campaign?\
\
select count (distinct(utm_campaign)) as distinct_campaings\
  from page_visits;                      \
----------------------\
\
select count (distinct(utm_source)) as distinct_sources\
  from page_visits;\
----------------------\
\
select distinct utm_campaign as campaigns,utm_source as sources\
from page_visits\
order by sources desc;\
----------------------\
\
--2. What pages are on the CoolTShirts website? \
\
select distinct page_name as user_journey_process\
 from page_visits\
  order by 1 asc;            \
\
--3. How many first touches is each campaign responsible for?\
\
WITH first_touch AS (\
    SELECT user_id,\
        MIN(timestamp) as first_touch_at\
    FROM page_visits\
    GROUP BY user_id),\
ft_attr AS (\
  SELECT \
         ft.user_id,\
         ft.first_touch_at,\
         pv.utm_source,\
         pv.utm_campaign\
  FROM first_touch ft\
  JOIN page_visits pv\
    ON ft.user_id = pv.user_id\
    AND ft.first_touch_at = pv.timestamp\
)\
SELECT \
       ft_attr.utm_campaign as Campaign_Name,              \
       COUNT(distinct(ft_attr.user_id)) as Number_of_FIRST_Touches\
FROM ft_attr\
GROUP BY ft_attr.utm_campaign\
ORDER BY Number_of_FIRST_Touches DESC;\
\
--4. How many last touches is each campaign responsible for? \
                      \
WITH last_touch AS (\
    SELECT user_id,\
        MAX(timestamp) as last_touch_at\
    FROM page_visits\
    GROUP BY user_id),\
lt_attr AS (\
  SELECT \
         lt.user_id,\
         lt.last_touch_at,\
         pv.utm_source,\
         pv.utm_campaign\
  FROM last_touch lt\
  JOIN page_visits pv\
  ON lt.user_id = pv.user_id\
  AND lt.last_touch_at = pv.timestamp\
)\
SELECT \
       lt_attr.utm_campaign as Campaign_Name,\
       COUNT(distinct(lt_attr.user_id)) as Number_of_LAST_Touches\
FROM lt_attr\
GROUP BY lt_attr.utm_campaign\
ORDER BY Number_of_LAST_Touches DESC;\
                  \
--5. How many visitors make a purchase? \
\
select count (distinct(user_id)) as Buyers\
from page_visits\
where page_name = '4 - purchase'\
group by page_name;\
  \
--6. How many last touches on the purchase page is each campaign responsible for?\
\
WITH LT_page AS (\
    SELECT user_id, \
           page_name,\
           utm_campaign,\
           MAX(timestamp) as last_touch_at\
    FROM page_visits\
    GROUP BY user_id)\
SELECT \
     LT_page.utm_campaign as Campaign,\
     count (distinct(LT_page.user_id)) as Number_of_Purchases\
FROM LT_page\
WHERE LT_page.page_name = '4 - purchase'           \
GROUP BY Campaign\
ORDER BY Number_of_Purchases DESC;\
\pard\pardeftab720\ri-5548\partightenfactor0
\cf2              
\f1\fs24 \cf0 \
\pard\pardeftab720\ri0\partightenfactor0
\cf0                        \
}