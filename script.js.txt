//-------------------------------------------------------------- Add Shipment --------------------------------/
const formToggleBtn = document.getElementById('formToggleBtn');
const floatingForm = document.getElementById('floatingForm');

// 1. Safe Event Listener Check
if (formToggleBtn && floatingForm) {
  formToggleBtn.addEventListener('click', () => {
    floatingForm.classList.toggle('active');
    formToggleBtn.classList.toggle('active-btn');
  });
}

//---------------------------------------------------------------Date & Time --------------------------------/
// 2. Optimized Clock Function
function showTime() {
  const timeDisplay = document.getElementById('currentTime');
  if (timeDisplay) {
    timeDisplay.innerHTML = new Date().toUTCString();
  }
}
// Run the clock immediately and update every second
showTime();
setInterval(showTime, 1000);
