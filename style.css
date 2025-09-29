var welcomeMessage = "As you follow the neon footprints, you arrive to the enchanted forest. For your surprise, at its entrance you are greeted by Boitatá, the serpent guardian of the forests, who has been waiting for you. It coils gently around you and whispers that together you will reveal your purpose in this adventure. The Macaloba ceremony is about to start share the day and month of your birth and the first letter of your name and let the forest reveal what it holds for you.";

// stores the data
var purposeData;

// when page loads
window.onload = function() {
    // show welcome text immediately
    document.getElementById('text').textContent = welcomeMessage;
    
    // load data
    fetch('data.json')
        .then(function(response) {
            return response.json();
        })
        .then(function(data) {
            purposeData = data;
        })
        .catch(function(error) {
            console.log('error loading data:', error);
        });
};

// finds the purpose based on what user picked
function findPurpose() {
    var day = document.getElementById('day').value;
    var letter = document.getElementById('letter').value;
    var month = document.getElementById('month').value;
    
    // check if everything is filled out
    if (day == '' || letter == '' || month == '') {
        alert('Please fill in all fields to discover your purpose!');
        return;
    }
    
    // get the texts from data
    var dayText = purposeData.days[day];
    var letterText = purposeData.letters[letter];
    var monthText = purposeData.months[month];
    
    // put them together
    var fullPurpose = dayText + ' ' + letterText + ' ' + monthText;
    
    // show the result
    document.getElementById('purposeText').textContent = fullPurpose;
    document.getElementById('intro').className = 'hide';
    document.getElementById('result').className = '';
}

// if they like their purpose
function celebrate() {
    alert('✨ Your adventure through the enchanted forest begins now! ✨');
}

// lets them try again
function tryAgain() {
    document.getElementById('result').className = 'hide';
    document.getElementById('intro').className = '';
    
    // clear the form
    document.getElementById('day').value = '';
    document.getElementById('letter').value = '';
    document.getElementById('month').value = '';
}
