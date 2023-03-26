# orderAndShippingGCPWorkflow
This workflow can be used to orchestrate streaming pipelines

Use the following json to run the workflow

{
    "project": "#PROJECT_ID",
    "maxRetry": "#MAX_RETRY_COUNT",
    "orderParams" : {
        "flexTemplate": "#ORDER DATAFLOW FLEX TEMPLATE",
        "region": "#REGION",
        "parameters": {
                "inputTopicSubscription": "#INPUT TOPIC",
                "bigQueryTable": "#BIGQUERY TABLE"
        },
        "environment": {
                "tempLocation" : "#TEMP LOCATION",
                "workerZone": "#WORKER ZONE"
        }
    },
    "shippingParams" : {
        "flexTemplate":"#SHIPPING FLEX TEMPLATE",
        "region": "#REGION",
        "parameters": {
                "inputTopicSubscription": "#INPUT TOPIC",
                "bigQueryTable": "#BIGQUERY TABLE"
        },
        "environment": {
                "tempLocation" : "#TEMP LOCATION",
                "workerZone": "#WORKER ZONE"
        }
    }
}
