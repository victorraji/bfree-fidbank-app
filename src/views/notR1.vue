<template>
<div class="home">
<header class="headerBlock">
<HeaderR/>
</header>
<div class="header2">
  <div class="userDetail"><UserDetailR/></div>
</div>
<aside class="nav2"><TheNavR/></aside>
<!-- group 89 drop downs -->
<div class="dropdown89">
<div class="feedbacks">
<ejs-dropdownlist :data-source='localData1' :fields='localField1' placeholder="Feedbacks">

</ejs-dropdownlist>
</div>
<div class="responses">
<ejs-dropdownlist :data-source='localData2' :fields='localField2' placeholder="Responses">

</ejs-dropdownlist>
</div>
<div class="sort">
<ejs-dropdownlist :data-source='localData3' :fields='localField3' placeholder="Sort">

</ejs-dropdownlist>
</div>
<div class="receivingD">
<ejs-dropdownlist :data-source='localData' :fields='localField' placeholder="Receiving department">

</ejs-dropdownlist>
</div>
</div>
<!-- main body -->
<div class="mainBody">
<div id="list">
<ul>
<li class="survey">
<span>S/N</span>
<span>Name</span>
<span>Team</span>
<span>Date/Time</span>
<span>Status</span>
</li>

<!-- row 2 -->

<li v-for='notlist in notlists' :key='notlist.id' class="survey">
<span>1.</span>
<span>Micheal</span>
<span>FairMoney</span>
<span>11/03 09/33</span>
<span><button>pending</button></span>
</li>
<!-- row 3 -->
<li v-for='notlist in notlists' :key='notlist.id' class="survey">
<span>2.</span>
<span>Bimpe</span>
<span>Branch</span>
<span>11/03 09/33</span>
<span><button>Completed</button></span>
</li>
<!-- row 4 -->
<li v-for='notlist in notlists' :key='notlist.id' class="survey">
<span>2.</span>
<span>Bimpe</span>
<span>Umba</span>
<span>11/03 09/33</span>
<span><button>Pending</button></span>
</li>
</ul>

</div>
</div>
<div>
<button class="buttons">Previous</button>
<button class="buttons1">Next</button>
</div>
</div>

</template>

<script>
import TheNavR from '@/components/responder/TheNavR.vue'
import HeaderR from '@/components/responder/HeaderR.vue'
import UserDetailR from '@/components/responder/UserDetailR.vue'

export default {
  name: 'HomeView',

  components: {
    TheNavR,
    HeaderR,
    UserDetailR
  },
  data: function () {
    return {
      localData1: [
        { Id: 'fb1', level: 'Positive Feedbacks' },
        { Id: 'fb2', level: 'Negative Feedbacks' }
      ],
      localField1: { value: 'Id', text: 'level' },

      localData2: [
        { Id: 'r1', level2: 'Responded' },
        { Id: 'rb2', level2: 'Not Responded' }
      ],
      localField2: { value: 'Id', text: 'level2' },

      localData3: [
        { Id: 's1', level3: 'Last Week' },
        { Id: 's2', level3: 'Last Month' },
        { Id: 's3', level3: '3 Months Ago' }
      ],
      localField3: { value: 'Id', text: 'level3' },

      localData: [
        { Id: 'team1', Level: 'Account Manager' },
        { Id: 'team2', Level: 'TeamLead-Branch' },
        { Id: 'team3', Level: 'TeamLead-Fairmoney' },
        { Id: 'team4', Level: 'TeamLead-Kuda' },
        { Id: 'team5', Level: 'TeamLead-Carbon' },
        { Id: 'team6', Level: 'TeamLead-Quickcheck' },
        { Id: 'team7', Level: 'TeamLead-Growth' },
        { Id: 'team8', Level: 'TeamLead-Float' },
        { Id: 'team9', Level: 'Operations-HR' },
        { Id: 'team10', Level: 'Operations-QA' },
        { Id: 'team11', Level: 'Operations-Head' },
        { Id: 'team12', Level: 'Engineering' }
      ],
      localField: { value: 'Id', text: 'Level' },

      notlists:
{
  name: 'Micheal',
  ReceivingDepartment: 'Engineering',
  datetime: 'Team-Lead Branch',
  Status: 'read'
}

    }
  }
}

</script>

<style scoped>
.dropdown89 {
position: absolute;
height: 40px;
left: 284px;
right: 60px;
top: 239px;
width: 1096;
}
.feedbacks {
position: absolute;
width: 251px;
height: 40px;
left: 0px;
top: 0px;
background: #C0DAE3;
border-radius: 5px 5px 0px 0px;
border: 1px #00A4DB;
}
.responses {
position: absolute;
width: 251px;
height: 40px;
left: 300px;
top: 0px;
background: #C0DAE3;
border-radius: 5px 5px 0px 0px;
border: 1px #00A4DB;
box-sizing: border-box;
}
.sort {
position: absolute;
width: 251px;
height: 40px;
left: 600px;
top: 0px;
background: #C0DAE3;
border-radius: 5px 5px 0px 0px;
border: 1px solid #00A4DB;
box-sizing: border-box;
}
.receivingD {
background: #C0DAE3;
border: 1px solid #00A4DB;
box-sizing: border-box;
border-radius: 5px 5px 0px 0px;
position: absolute;
width: 251px;
height: 40px;
left: 900px;
top: 0px;
}
.mainBody {
position: absolute;
width: 1096px;
height: 616px;
left: 284px;
top: 309px;
filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}
.survey {
display: flex;
justify-content: space-between;
flex-direction: row;
padding: 10px;
width: 1139px;
margin-left: -40px;
}
.firstBox {
width: 2vw;
}
li:nth-child(odd) {
background-color: rgba(181, 215, 227, 0.9);
}
li:nth-child(even) {
background-color: rgba(181, 215, 227, 0.31);;
}
li:first-child {
background-color:#00A4DB;;
}
.home {
display: grid;
grid-template-columns: 240px 1fr;
grid-template-rows: 20px 140px;
grid-template-areas:
"nav2 header"
"nav2 header2"
"nav2 main";
height: 100vh;
background: linear-gradient(0deg, #FFFFFF, #FFFFFF), rgba(0, 164, 219, 0.32);
}
.survey {
font-family: 'Poppins';
font-style: normal;
font-weight: 500;
font-size: 16px;
line-height: 24px;
color: #000000;
}

.nav2 {
grid-area: nav2;
}
.header {
grid-area: header;
padding-left: -40px;
}
.buttons {
background-color: #00A4DB;
border: 1px solid #FFFFFF;
box-sizing: border-box;
border-radius: 5px;
font-family: 'Poppins';
font-style: normal;
font-weight: 500;
font-size: 13px;
line-height: 20px;
color: #FFFFFF;
margin: -10px 20px 30px 40px;
padding: 5px 40px;
position: absolute;
width: 161px;
height: 30px;
left: 657px;
top: 942px;
}
.headerBlock{
margin-left: -250px;
}
.buttons1 {
background-color: #00A4DB;
border: 1px solid #FFFFFF;
box-sizing: border-box;
border-radius: 5px;
font-family: 'Poppins';
font-style: normal;
font-weight: 500;
font-size: 13px;
line-height: 20px;
color: #FFFFFF;
margin: -10px 20px 30px 40px;
padding: 5px 40px;
position: absolute;
width: 161px;
height: 30px;
left: 830px;
top: 942px;
}
.userDetail{
  margin: 80px 0 0 -280px;
}
</style>
