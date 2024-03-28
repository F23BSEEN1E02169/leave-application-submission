from flask import FLASK,  request, render _template
app = Flask(__name__)

#mock database of employees and their leave balances 
employees = {
   "john" : {"annual_leave": 10, "sick leave" :5}
   "Alice": {"annual_leave": 15,"sick_leave": 7}
   #Add more employees as needed}
@app.route('/')
def index():
    return
render_template('index.html',employees=employes)

@app.route('/'submit_leave',methods=['post] )
def submit _leave():
    employees_name=
request.form['employee_name']
    leave_type=
request.form['leave_type]
    leave_duration=
int(request.form['leave __ duration'])
    #check if the employees exists
    if employee_ name is employees:
        check if sufficient leave balance 
        if leave duration <=employees[employee_name]  
        [leave_type]:
                     #Deduct leave from balance
                     employees[employees_name]
 [leave_type] -=leave_duration
                     return"leave application submitted successfully!"
                else
                     return "Insufficcient leave balance!"
            else:
                return "employees not found!"
if __name__ == '__main__':
    app.run(debug=true)








-
                     

       
        









=
