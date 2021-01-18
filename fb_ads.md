# Campaign Statistics 
> curl -G \
-d "date_preset=last_7d" \
-d "access_token=<ACCESS_TOKEN>" \
"https://graph.facebook.com/<API_VERSION>/<AD_CAMPAIGN_ID>/insights"

# Making Calls
API Method
>act_<AD_ACCOUNT_ID>/insights  
<CAMPAIGN_ID>/insights  
<ADSET_ID>/insights  
<AD_ID>/insights  

* curl -i - X GET "https://graph.facebook.com/{page-id}/insights/page_impressions_unique&access_token={page-access-token}"