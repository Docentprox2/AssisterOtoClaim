# AssisterOtoClaim
AssisterClaim

function clickGrabTokenButton() {
    // Butonu text içeriğine göre bul
    const buttons = Array.from(document.getElementsByTagName('button'));
    const targetButton = buttons.find(button => button.textContent.includes('Grab Daily Tokens'));
    
    if (targetButton) {
        // Butonu tıkla
        targetButton.click();
        console.log('Token button clicked at:', new Date().toLocaleString());
    } else {
        console.log('Button not found!');
    }
}

// İlk tıklamayı hemen yap
clickGrabTokenButton();

// 1 saat = 60 * 60 * 1000 milisaniye
const oneHour = 60 * 60 * 1000;

// Her saatte bir tekrarla
setInterval(clickGrabTokenButton, oneHour);

console.log('Auto clicker started! Will click every 1 hour.');
