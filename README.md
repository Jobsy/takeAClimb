# takeAClimb
ALC 2.0 Web Beginner : Take A Climb Challenge

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Take A Climb Challenge</title>
    <meta charset="utf-8">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
    <link href='https://fonts.googleapis.com/css?family=Roboto:300,400,700' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.6-rc.0/css/select2.min.css" rel="stylesheet" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.6-rc.0/js/select2.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
  
    <style>
      .jumbotron {
        display: flex;
        align-items: center;
        background-image: url("https://image.freepik.com/darmowe-wektory/wielok%C4%85tne-kszta%C5%82ty-na-przezroczystym-tle_1035-7123.jpg");
        background-size: cover;
        color: #ffffff;
        height: 500px;
        text-shadow: 0.25px 0.25px 0.25px #000000;
      }

      img {
        max-width: 180px;
      }

      #addressId {
        padding-left: 300px;
      }
      #contactId {
        padding-left: 350px;
        margin-top: 50px;
      }
      #newId {
        margin-top: 50px;
      }
      .newClass {
        padding: 0px 40px;
      }
      .col-sm-4 {
      }
      .col-sm-2 {
      }
      .col-sm-12 {
        margin: 5px;
      }
      #imgbox2 {
        margin-bottom: 50px;
      }
      .newForm {
        background: brown;
        padding: 0px 0px 50px 20px;
      }
      /*the container must be positioned relative:*/
      .custom-select {
        position: relative;
        font-family: Arial;
      }
      .custom-select select {
        display: none; /*hide original SELECT element:*/
      }
      .select-selected {
        background-color: DodgerBlue;
      }
      /*style the arrow inside the select element:*/
      .select-selected:after {
        position: absolute;
        content: "";
        top: 14px;
        right: 10px;
        width: 0;
        height: 0;
        border: 6px solid transparent;
        border-color: #fff transparent transparent transparent;
      }
      /*point the arrow upwards when the select box is open (active):*/
      .select-selected.select-arrow-active:after {
        border-color: transparent transparent #fff transparent;
        top: 7px;
      }
      /*style the items (options), including the selected item:*/
      .select-items div,
      .select-selected {
        color: #ffffff;
        padding: 8px 16px;
        border: 1px solid transparent;
        border-color: transparent transparent rgba(0, 0, 0, 0.1) transparent;
        cursor: pointer;
        user-select: none;
      }
      #yourname {
        width: 640px;
      }
      #exitBtn {
        padding-left: 450px;
      }
      input {
        color: grey;
        width: 413px;
        padding: 8px 16px;
        border: 1px solid;
        border-radius: 4px;
        border-color: transparent transparent rgba(0, 0, 0.4, 0.1) transparent;
        cursor: pointer;
        user-select: none;
      }
      /*style items (options):*/
      .select-items {
        position: absolute;
        background-color: DodgerBlue;
        top: 100%;
        left: 0;
        right: 0;
        z-index: 99;
      }
      /*hide the items when the select box is closed:*/
      .select-hide {
        display: none;
      }
      .select-items div:hover {
        background-color: rgba(0, 0, 0, 0.1);
      }

      #contacts-table {
        border-collapse: collapse;
      }
      #contacts-table,
      #contacts-table th,
      #contacts-table td {
        padding: 8px 16px;
        text-align: left;
        border: 10px solid blue;
      }
      #contacts-table th {
        font-weight: bold;
        font-size: 14px;
        color: green;
      }
      #contacts-table td {
        color: #000;
      }
      #contacts-table tr:nth-child(2n) {
        background: lightblue;
      }

      #contacts-form {
        padding: 10px;
      }
      #contacts-form label,
      #contacts-form .field {
        display: inline-block;
        color: #0c0b07;
      }
      #contacts-form label {
        width: 110px;
        font-size: 15px;
        font-weight: bold;
        color: black;
        background: red;
        padding-left: 18px;
        margin-top: 10px;
      }

      #contacts-form .button {
        display: inline-block;
      }
      #contacts-form .button-wrapper {
        padding-left: 113px;
      }
    </style>
</head>
<body>
    <section class="jumbotron page1">
  <div class="container">
    <div id="addressId">
      <h1>ADDRESS BOOK</h1>
    </div>

    <div class="row">
      <div class="col-sm-6" id="contactId">
        <button onclick="resetElement2()"><h2>CONTACTS</h2></button>
      </div>

      <div class="col-sm-6" id="newId">
        <button class="newClass" onclick="resetElement()"><h2>+ NEW</h2></button>
      </div>
    </div>
  </div>
</section>

<section id="imgbox2">
  <h1>Contacts</h1>
  <table id="contacts-table">
    <th>ID</th>
    <th>Name</th>
    <th>Phone Type</th>
    <th>Number</th>
    <th>Email Type</th>
    <th>Email Address</th>
    <th>Address Location</th>
    <th>Address</th>
    <th>Group</th>
    <th>Remarks</th>
    <th>Actions</th>
  </table>

  <div id="exitBtn" class="col-sm-12">
    <input type="button" onclick="removeElement2()" value="Exit contact" />
  </div>
</section>

<section id="imgbox1">
  <div class="newForm">
    <form id="contacts-form">
      <h1>New Contact</h1>

      <!-- The Name div -->
      <div class="item text">
        <label for="name">NAME</label><br>
        <div class="field">
          <input type="text" id="yourname" placeholder="Enter your full name" name="name" required/>
        </div>
      </div>

      <!-- The Phone div -->
      <div class="item text">
        <label for="phone"><b>PHONE</b></label><br>
        <div class="row">
          <div class="col-sm-2">
            <div class="custom-select" style="width:200px;">
              <select name="selPhone">
                <option value="Choose an option">Select:</option>
                <option value="Mobile">Mobile</option>
                <option value="Home">Home</option>
                <option value="Work">Work</option>
                <option value="Others">Others</option>
              </select>
            </div>
          </div>

          <div class="col-sm-4">
            <input type="number" placeholder="Enter Number" name="phone">
          </div>
        </div>
      </div>

      <!-- The Email div -->
      <div class="item text">
        <label for="email"><b>EMAIL</b></label><br>
        <div class="row">
          <div class="col-sm-2">
            <div class="custom-select" style="width:200px;">
              <select name="selEmail">
                <option value="Choose an option">Select:</option>
                <option value="Home">Home</option>
                <option value="Work">Work</option>
                <option value="Others">Others</option>
              </select>
            </div>
          </div>

          <div class="col-sm-4">
            <input type="text" placeholder="Enter Email" name="email">
          </div>
        </div>
      </div>

      <!-- The Address div -->
      <div class="item text">
        <label for="address"><b>ADDRESS</b></label><br>
        <div class="row">
          <div class="col-sm-2">
            <div class="custom-select" style="width:200px;">
              <select name="selAddress">
                <option value="Choose an option">Select:</option>
                <option value="Home">Home</option>
                <option value="Work">Work</option>
                <option value="Others">Others</option>
              </select>
            </div>
          </div>

          <div class="col-sm-4">
            <input type="text" placeholder="Enter Address" name="address">
          </div>
        </div>
      </div>

      <!-- The Group  & Remarks div -->
      <div class="item text">
        <div class="row">
          <div class="col-sm-2">
            <label for="group"><b>GROUP</b></label>
          </div>
          <div class="col-sm-4">
            <label for="remarks"><b>REMARKS</b></label>
          </div>
        </div>
        <div class="row">
          <div class="col-sm-2">
            <div class="custom-select" style="width:200px;">
              <select name="selGroup">
                <option value="Choose an option">Select:</option>
                <option value="Family">Family</option>
                <option value="Friends">Friends</option>
                <option value="Coworker">Coworks</option>
                <option value="Others">Others</option>
               </select>
            </div>
          </div>
          <div class="col-sm-4">
            <textarea name="txtRemarks" class="form-control" rows="1" placeholder="Write a remarks or comment"></textarea>
          </div>
        </div>

        <div class="button-wrapper">
          <div class="row">

            <div class="col-sm-12">
              <input type="submit" id="contacts-op-save" value="Save" />

            </div>

            <div class="col-sm-12">
              <input type="button" id="contacts-op-discard" value="Reset" />
            </div>
            <div class="col-sm-12">
              <input type="button" onclick="removeElement()" value="Discard" />
            </div>
          </div>
        </div>

        <input type="hidden" name="id_entry" value="0" />
    </form>
    </div>
</section>

<script>
        function removeElement() {
          document.getElementById("imgbox1").style.display = "none";
        }
        function removeElement2() {
          document.getElementById("imgbox2").style.display = "none";
        }
        function resetElement() {
          document.getElementById("imgbox1").style.display = "block";
        }
        function resetElement2() {
          document.getElementById("imgbox2").style.display = "block";
        }

        var x, i, j, selElmnt, a, b, c;
        /*look for any elements with the class "custom-select":*/
        x = document.getElementsByClassName("custom-select");
        for (i = 0; i < x.length; i++) {
          selElmnt = x[i].getElementsByTagName("select")[0];
          /*for each element, create a new DIV that will act as the selected item:*/
          a = document.createElement("DIV");
          a.setAttribute("class", "select-selected");
          a.innerHTML = selElmnt.options[selElmnt.selectedIndex].innerHTML;
          x[i].appendChild(a);
          /*for each element, create a new DIV that will contain the option list:*/
          b = document.createElement("DIV");
          b.setAttribute("class", "select-items select-hide");
          for (j = 1; j < selElmnt.length; j++) {
            /*for each option in the original select element,
            create a new DIV that will act as an option item:*/
            c = document.createElement("DIV");
            c.innerHTML = selElmnt.options[j].innerHTML;
            c.addEventListener("click", function(e) {
              /*when an item is clicked, update the original select box,
                and the selected item:*/
              var i, s, h;
              s = this.parentNode.parentNode.getElementsByTagName("select")[0];
              h = this.parentNode.previousSibling;
              for (i = 0; i < s.length; i++) {
                if (s.options[i].innerHTML == this.innerHTML) {
                  s.selectedIndex = i;
                  h.innerHTML = this.innerHTML;
                  break;
                }
              }
              h.click();
            });
            b.appendChild(c);
          }
          x[i].appendChild(b);
          a.addEventListener("click", function(e) {
            /*when the select box is clicked, close any other select boxes,
              and open/close the current select box:*/
            e.stopPropagation();
            closeAllSelect(this);
            this.nextSibling.classList.toggle("select-hide");
            this.classList.toggle("select-arrow-active");
          });
        }
        function closeAllSelect(elmnt) {
          /*a function that will close all select boxes in the document,
          except the current select box:*/
          var x,
            y,
            i,
            arrNo = [];
          x = document.getElementsByClassName("select-items");
          y = document.getElementsByClassName("select-selected");
          for (i = 0; i < y.length; i++) {
            if (elmnt == y[i]) {
              arrNo.push(i);
            } else {
              y[i].classList.remove("select-arrow-active");
            }
          }
          for (i = 0; i < x.length; i++) {
            if (arrNo.indexOf(i)) {
              x[i].classList.add("select-hide");
            }
          }
        }
        /*if the user clicks anywhere outside the select box,
        then close all select boxes:*/
        document.addEventListener("click", closeAllSelect);

        var Contacts = {
          index: window.localStorage.getItem("Contacts:index"),
          $table: document.getElementById("contacts-table"),
          $form: document.getElementById("contacts-form"),
          $button_save: document.getElementById("contacts-op-save"),
          $button_discard: document.getElementById("contacts-op-discard"),

          init: function() {
            // initialize storage index
            if (!Contacts.index) {
              window.localStorage.setItem("Contacts:index", (Contacts.index = 1));
            }

            // initialize form
            Contacts.$form.reset();
            Contacts.$button_discard.addEventListener(
              "click",
              function(event) {
                Contacts.$form.reset();
                Contacts.$form.id_entry.value = 0;
              },
              true
            );
            Contacts.$form.addEventListener(
              "submit",
              function(event) {
                var entry = {
                  id: parseInt(this.id_entry.value),
                  name: this.name.value,
                  selPhone: this.selPhone.value,
                  phone: this.phone.value,
                  selEmail: this.selEmail.value,
                  email: this.email.value,
                  selAddress: this.selAddress.value,
                  address: this.address.value,
                  selGroup: this.selGroup.value,
                  txtRemarks: this.txtRemarks.value
                };
                if (entry.id === 0) {
                  // add
                  Contacts.storeAdd(entry);
                  Contacts.tableAdd(entry);
                } else {
                  // edit
                  Contacts.storeEdit(entry);
                  Contacts.tableEdit(entry);
                }

                this.reset();
                this.id_entry.value = 0;
                event.preventDefault();
              },
              true
            );

            // initialize table
            if (window.localStorage.length - 1) {
              var contacts_list = [],
                i,
                key;
              for (i = 0; i < window.localStorage.length; i++) {
                key = window.localStorage.key(i);
                if (/Contacts:\d+/.test(key)) {
                  contacts_list.push(JSON.parse(window.localStorage.getItem(key)));
                }
              }

              if (contacts_list.length) {
                contacts_list
                  .sort(function(a, b) {
                    return a.id < b.id ? -1 : a.id > b.id ? 1 : 0;
                  })
                  .forEach(Contacts.tableAdd);
              }
            }
            Contacts.$table.addEventListener(
              "click",
              function(event) {
                var op = event.target.getAttribute("data-op");
                if (/edit|remove/.test(op)) {
                  var entry = JSON.parse(
                    window.localStorage.getItem(
                      "Contacts:" + event.target.getAttribute("data-id")
                    )
                  );
                  if (op == "edit") {
                    Contacts.$form.name.value = entry.name;
                    Contacts.$form.selPhone.value = entry.selPhone;
                    Contacts.$form.phone.value = entry.phone;
                    Contacts.$form.selEmail.value = entry.selEmail;
                    Contacts.$form.email.value = entry.email;
                    Contacts.$form.selAddress.value = entry.selAddress;
                    Contacts.$form.address.value = entry.address;
                    Contacts.$form.selGroup.value = entry.selGroup;
                    Contacts.$form.txtRemarks.value = entry.txtRemarks;
                    Contacts.$form.id_entry.value = entry.id;
                  } else if (op == "remove") {
                    if (
                      confirm(
                        'Are you sure you want to remove "' +
                          entry.first_name +
                          " " +
                          entry.last_name +
                          '" from your contacts?'
                      )
                    ) {
                      Contacts.storeRemove(entry);
                      Contacts.tableRemove(entry);
                    }
                  }
                  event.preventDefault();
                }
              },
              true
            );
          },

          storeAdd: function(entry) {
            entry.id = Contacts.index;
            window.localStorage.setItem("Contacts:index", ++Contacts.index);
            window.localStorage.setItem("Contacts:" + entry.id, JSON.stringify(entry));
          },
          storeEdit: function(entry) {
            window.localStorage.setItem("Contacts:" + entry.id, JSON.stringify(entry));
          },
          storeRemove: function(entry) {
            window.localStorage.removeItem("Contacts:" + entry.id);
          },

          tableAdd: function(entry) {
            var $tr = document.createElement("tr"),
              $td,
              key;
            for (key in entry) {
              if (entry.hasOwnProperty(key)) {
                $td = document.createElement("td");
                $td.appendChild(document.createTextNode(entry[key]));
                $tr.appendChild($td);
              }
            }
            $td = document.createElement("td");
            $td.innerHTML =
              '<a data-op="edit" data-id="' +
              entry.id +
              '">Edit</a> | <a data-op="remove" data-id="' +
              entry.id +
              '">Remove</a>';
            $tr.appendChild($td);
            $tr.setAttribute("id", "entry-" + entry.id);
            Contacts.$table.appendChild($tr);
          },
          tableEdit: function(entry) {
            var $tr = document.getElementById("entry-" + entry.id),
              $td,
              key;
            $tr.innerHTML = "";
            for (key in entry) {
              if (entry.hasOwnProperty(key)) {
                $td = document.createElement("td");
                $td.appendChild(document.createTextNode(entry[key]));
                $tr.appendChild($td);
              }
            }
            $td = document.createElement("td");
            $td.innerHTML =
              '<a data-op="edit" data-id="' +
              entry.id +
              '">Edit</a> | <a data-op="remove" data-id="' +
              entry.id +
              '">Remove</a>';
            $tr.appendChild($td);
          },
          tableRemove: function(entry) {
            Contacts.$table.removeChild(document.getElementById("entry-" + entry.id));
          }
        };

        Contacts.init();
</script>
</body>
</html>
