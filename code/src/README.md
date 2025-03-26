Step-1.) Access https://dashboard.ngrok.com/ 
Step-2.) Register with the Gmail ID
Step-3.) Generate Auth token
Step-4.) Run the notebook from Google colab: HyperPersonalization_Recommendation.ipynb
Step-5.) Copy the URL exposed by ngrok. Example - https://86f0-34-125-62-208.ngrok-free.app/
Step-6.)Execute the below end points from Postman:

Method: GET
URL: {ngrokUrl}
Response: {"message": "AI-driven API for predictive insights, personalization, sentiment analysis, and risk assessment"}

Method: POST
URL: {ngrokUrl}/api/v1/predictiveInsight
Request Body: {"message": "Purchased a DELL laptop last time for 10000 dollars. Also trying to buy an internet connection"}
Sample Response from model: 
{
    "Predictive insights": "1. Based on your past purchase of a high-end Dell laptop, you may consider investing in a premium business or fiber optic internet plan for optimal performance and reliability. The cost could range from $50 to $200 per month depending on the provider and location.\n2. Given that you have recently spent a significant amount on a new laptop, it might be wise to explore budget-friendly internet options such as DSL or cable plans which can cost around $30-$60 per month.\n3. Considering your previous expensive purchase, there's also an opportunity for bundling deals with your laptop vendor (Dell) or Internet Service Provider (ISP). Look out for packages that offer discounted prices on both the laptop and internet connection to save some money in the long run."
}

Method: POST
URL: {ngrokUrl}/api/v1/sentiment
Request Body: {"message": "I'm very happy with the product"}
Sample Response from model: 
{
    "User sentiment": "1. Positive feedback received: You have expressed satisfaction with the product.\n2. High level of happiness: Your sentiment towards the product is extremely positive.\n3. Product meets expectations: Based on your statement, it can be inferred that the product has met or exceeded your expectations."
}

Method: POST
URL: {ngrokUrl}/api/v1/personalizeRecommendation
Request Body: {"message": "I'm very happy with the laptop purchased"}
Sample Response from model: 
{
    "recommendation": "1. I'm glad to hear that you're satisfied with your new laptop purchase! If you need any software or applications, feel free to ask for recommendations.\n2. Your positive feedback is appreciated. Here are some tips to maximize your laptop usage: regular updates, organizing files, and using productivity apps.\n3. I'm thrilled that the laptop meets your expectations. Consider joining online communities related to laptops or technology for troubleshooting tips and user experiences."
}

Method: POST
URL: {ngrokUrl}/api/v1/assessRisk
Request Body: {"message": "Product seems to be a fake one which I had purchased"}
Sample Response from model: 
{
    "Risk_assessment": "1. Verify purchase details: Check the authenticity of the seller, transaction history, and product description from the original purchasing platform or marketplace to confirm if it was indeed a fake product.\n2. Contact customer support: Reach out to the customer service team of the brand or manufacturer for assistance in identifying whether the product is genuine or not based on its serial number, model number, or other unique identifiers.\n3. Inspect physical features: Examine the product closely for any inconsistencies such as missing logos, poor quality materials, incorrect labeling, and mismatched parts that could indicate it's a counterfeit item."
}
