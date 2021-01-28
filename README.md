# customer-segregation-for-a-travel-company-website
using k-means clustering so that based on the users input on the final webbsite on a travel company, they can be segregated so that the under and overperforming asesets for the company is seen and which new cities to launch in is clearer. this helps increase the user booking rate

outperforming segments:
    sample.groupby('channel')['is_booking']\
       agg({'booking_rate':'mean', 'num_of_bookings':'sum'})\
       reset_index()\
       sort_values(by = 'booking_rate')
       
 clustering--similar user cities:
    from sklearn import cluster
    import matplotlib.pyplot as plt
    model.predict(): predict labels in a clustering algorithm
    
 decision tree--increase in user booking:
    from sklearn import tree, decomposition
    from sklearn.cross_validation import train_test_split
    model.fit(): fit training data
    model.predict(): given a trained model, predict a label of  a new set of data
    Model.score: larger score indicating  a better fit
