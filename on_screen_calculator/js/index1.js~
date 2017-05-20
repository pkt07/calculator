$(document).ready(function() {

  var btnValue = $(".btn");
  var screen = $(".screen");
  var valueArr = [];
  var isFloat = 0;
  var onScreenResult = 0;
  var hasCalculated = false;
  var ceSlice = 0;

  function sliced() {
    var a = valueArr.lastIndexOf('+');
    var b = valueArr.lastIndexOf('-');
    var c = valueArr.lastIndexOf('/');
    var d = valueArr.lastIndexOf('*');
    var arr = [a, b, c, d];
    ceSlice = Math.max.apply(null, arr);
  }

  function check() {
    if (hasCalculated === true) {
      valueArr = [];
      screen.html(" ");
      hasCalculated = false;
    }
  }

  function operationCheck() {
    if (hasCalculated === true) {
      $(screen).html(onScreenResult);
      valueArr = [onScreenResult];
      hasCalculated = false;
    }
  }
  //operations
  $("clear").click(function() {
    valueArr = [];
    screen.html(" ");
  });
  $("#divide").click(function() {
    operationCheck();
    valueArr.push("/");
    $(screen).append("/");
    isFloat = 0;
  });
  $("#multiply").click(function() {
    operationCheck();
    valueArr.push("*");
    $(screen).append("*");
    isFloat = 0;
  });
  $("#add").click(function() {
    operationCheck();
    valueArr.push("+");
    $(screen).append("+");
    isFloat = 0;
  });
  $("#subtract").click(function() {
    operationCheck();
    valueArr.push("-");
    $(screen).append("-");
    isFloat = 0;
  });
  $("#equal").click(function() {
    operationCheck();
    onScreenResult = valueArr.reduce(function(a, b) {
      return a + b;
    });
    onScreenResult = eval(onScreenResult);
    $(screen).html(onScreenResult);
    hasCalculated = true;

  });
  $('#decimal').click(function() {
    check();
    if (isFloat != 1) {
      valueArr.push('.');
      $('#screen').append('.');
      isFloat = 1;
    }
  });
  //digits

  $("#one").click(function() {
    check();
    valueArr.push("1");
    screen.append(1);
  });
  $("#two").click(function() {
    check();
    valueArr.push("2");
    screen.append(2);

  });
  $("#three").click(function() {
    check();
    valueArr.push("3");
    screen.append(3);

  });
  $("#four").click(function() {
    check();
    valueArr.push("4");
   screen.append(4);

  });
  $("#five").click(function() {
    check();
    valueArr.push("5");
    screen.append(5);

  });
  $("#six").click(function() {
    check();
    valueArr.push("6");
    screen.append(6);

  });
  $("#seven").click(function() {
    check();
    valueArr.push("7");
    screen.append(7);

  });
  $("#eight").click(function() {
    check();
    valueArr.push("8");
    screen.append(8);
  });
  $("#nine").click(function() {
    check();
    valueArr.push("9");
    screen.append(9);

  });
  $("#zero").click(function() {
    check();
    valueArr.push("0");
    screen.append(0);

  });

});


