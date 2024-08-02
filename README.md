    from datetime import datetime, timedelta
    day = int(input("enter the day of the Year "))
    year = int(input("enter the year "))

    leap = (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0)

    if day < 1 or day > (366 if leap else 365):
         print("Invalid day for this year.")
    else:
   
         date = datetime(year, 1, 1) + timedelta(days=day - 1)
    
    
         dateformat = date.strftime('%d/%m/%Y')

         week = date.isocalendar()[1]

         print("date " , dateformat)
         print("week" , week)
    
         if leap : 
              print("Leap? : yes")
         else :
              print ("Leap?: no")
    
