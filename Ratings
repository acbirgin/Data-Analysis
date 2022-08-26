#!/usr/bin/env python
# coding: utf-8

# In[3]:


# Andrew Birgin
# BMGT 302
# 0201
# 10/15/21

def ratings_data():
    #Code before the student_rating input act as the constraint values and count values for which 
    #the problem revolves around 
    
    entree_name = input("Enter entree name for which you want feedback: ")
    terminated = False
    ratings_list = []
    min_rating = 0
    max_rating = 5
    max_attempts = 3
    popular_dish = 4.3
    total_rating_count = 0
    invalid_rating_count = 0
    minimum_user_input = 1
    while not terminated: #Needed a while loop so that input continues until the termination
        #condition is met
        termination_condition = 302
        
        student_rating = int(input(f"Enter a rating for {entree_name} from 0 to 5 stars. "))
        #Initiate the termination condition value to assert "302" as the termination sequence
        if student_rating != termination_condition:
            termination_condition = False
            #Count the student input ratings if they are between 0 and 5 (inclusive) and add
            #the input to the student_rating to the ratings_list list.
            if student_rating >= min_rating and student_rating <= max_rating:
                total_rating_count += 1
                ratings_list.append(student_rating)
                
            print(f'You gave {entree_name} a {student_rating} out of {max_rating}. ')
            #Necessary step to count the number of ratings that don't fall between 0 and 5
            #will need this later when determining if the student has maxed out their attempts
            #at rating an entree
            if student_rating < min_rating or student_rating > max_rating:
                invalid_rating_count += 1
                
                #Since the students are allowed 3 attempts to enter a valid entree rating until
                #the program moves onto the next student, this "if" condition will print that
                #they need assistance if they don't provide a valid rating after 3 tries.
                if invalid_rating_count % max_attempts == 0:
                    print("Failure to provide a valid entry, contact staff for assistance. \nNext student: ")
            
        else:
            #Counting the total sum of the list to be used for the mean calculation later on
            total_val = sum(ratings_list)
            if total_rating_count < minimum_user_input:
                print("Report could not be generated because no ratings were provided.")
            
            else:
                #Variables created below needed to print out the reports of the ratings, giving
                #the average, max, min, and checking to see if the average >= 4.3, and if it is,
                #The entree is a popular dish.
                total_val = sum(ratings_list)  
                mean_val = (total_val / total_rating_count) if total_rating_count >= minimum_user_input else total_rating_count
                min_val = min(ratings_list) if total_rating_count >= minimum_user_input else total_rating_count
                max_val = max(ratings_list)if total_rating_count >= minimum_user_input else total_rating_count
                print(f'{entree_name} statistics:')
                print(f'The mean rating is {mean_val:.1f}.')
                print(f'The highest rating was {max_val} out of {max_rating}. ')
                print(f'The lowest rating was {min_val} out of {max_rating}. ')
                print("Popular Entree!" if mean_val >= popular_dish else "")
            #If the termination condition is met and the user types in "302," the program ends
            terminated = True
                    
ratings_data()

#I pledge on my honor that I have not given nor received any unauthorized assistance on this
#Assignment 
#<Andrew Birgin>


# In[ ]:




