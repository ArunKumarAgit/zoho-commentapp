                             Comment App
You are required to build a feedback application that has
the following functionalities,
1. Sign-up where the user will be allowed to enter his emailID and password along
with a secret code. This data will be validated and sent to the backend where the
data will be stored in a Database.


2. Sign-in where the user will be allowed to enter his emailID and password. This
data will be sent to the backend where it will be cross-checked with the data
available in the database and a proper response is returned to the frontend.


3. Forget-password where the user will be allowed to enter the email id and
secret code. This data will be sent to the backend and If the data matches with
any record already in the database then the password should be shown to the
user In frontend.


4. After sign-in the user will be presented with a text area where he will be able to
type any comments. After submitting, the comment will be taken to the backend
and saved in database.


5. Below the text area, the user will also see other users' comments along with
the respective email ids next to them.


6. There will be a filter button on click it, the comment area will show only the
comments of the logged in user.


json-- "test": "echo \"Error: no test specified\" && exit 1"

//get request
app.get('/sign_up',async(req,res) => {
    try{
           const aliens = await Alien.find()
           res.json(aliens)
    }catch(err){
        res.send('Error ' + err)
    }
})

app.get("/reset",(req,res)=>{
    var email = req.body.email;
    var number = req.body.number;

    var data = {
        "email" : email,
        "number" : number
    }

    db.collection('users').insertOne(data,(err,collection)=>{
        if(err){
            throw err;
        }
        console.log("Record Inserted Successfully");
    });

    return res.redirect('textarea.html')

})
//---

// app.get("/textarea",(req,res)=>{


//     db.collection('comments').find({},(err,collection)=>{
//         if(err){
//             throw err;
//         }
//         console.log(collection);
//         return res.send(collection);
//     });

//    // return res.send({});
    
// })#   z o h o  
 #   z o h o  
 