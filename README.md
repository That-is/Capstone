1.Background of the research:
     Taxi drivers are facing the same problem that the destination has no
     passenger to pick up after their previous order has been delivered, so they
     have to go back with an empty car. Unfortunately, no existing model can
     support their decision-making process by providing the passenger demand
     on a specific time period at a specific location where they are heading to. So
     the project planned to use the knowledge in machine learning to deliver a
     model with the power to predict the aggregated passenger demand in the
     next 15 minutes from when their cars are empty at a specific location.
     
2.Data set location:
          https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page
          (1) Selected data from June 2018 to August 2018.
          (2) Yellow trips data.
          
3.Research problems:
         (1)Predict the passenger demand in the next 15 minutes in New York.
         (2)Predict the averaged profit in 15 minutes for driver.
        
4.Application Area:
         (1) Provide drivers with predicted demand and their average profit, so that they can decide whether to hunt or wait 
             in the same place.
             
5.Some justifications:
        (1)Reason for 15 minutes interval:
           The second-largest zone in New York is Bloomfield/Emerson Hill, and it takes 13 minutes from one side of this zone to the other side. So I think 15 minutes would be a reasonable time for driver from one location to another to pick up a passenger if he decided to hunt.
           
         (2)Reason for three months data(summer):
            A seasonal specific prediction would be more useful, if the prediction rate is pretty high, I would consider putting other months' dataset into the model.
