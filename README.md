# twitter_ads
Gem to simplify access to TwitterAds API

Usage:

You need to instanciete the client with a whitlsted Twitter Ads application and a user token allowed for this app:

     ads=TwitterAds::Client.new({consumer_key:"YOUR_CONSUER_KEY",
	                         consumer_secret:"YOUR CONSUMER SECRET",
	                        access_token:"YOUR ACCESS TOKEN",
	                        access_secret:"YOUR ACCESS SECRET"})
 get the list of accounts:

     ads.accounts

 get info on a specfic account

    account=ads.account(account_id)

Note that using this form, the account won't be fetched unless you do a refresh call:

     account.refresh

 get tailored_audience change

    accounts.tailored_audience_changes

get tailored audience change on a specific list

    accounts.tailoered_audience_changes list_id