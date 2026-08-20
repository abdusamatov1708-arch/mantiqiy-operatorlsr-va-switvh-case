# mantiqiy-operatorlsr-va-switvh-case
/**
 * Loyiha: Virtual Kafedra Yordamchisi
 * Mavzu: switch-case va mantiqiy operatorlar (&&, ||)
 */

// Kirish o'zgaruvchilari
const dayOfWeek = "Dushanba"; // Haftaning kuni
const imtihonBor = false;      // Imtihon mavjudligi (true / false)
const vazifaBajarildi = true;  // Vazifa bajarilganligi (true / false)
const darsQoldirildi = false;  // Darslar rasman qoldirilganligi

// 1-qism: switch-case yordamida kun tartibini aniqlash
switch (dayOfWeek) {
    case "Dushanba":
    case "Chorshanba":
    case "Juma":
        console.log("Bugun asosiy dars kunlari.");
        break;
    case "Seshanba":
    case "Payshanba":
        console.log("Bugun amaliyot va laboratoriya kuni.");
        break;
    case "Shanba":
    case "Yakshanba":
        console.log("Dam olish kuni.");
        break;
    default:
        console.log("Noto'g'ri kun kiritildi!");
}

// Dars kuni ekanligini tekshirib olish uchun yordamchi o'zgaruvchi
const isSchoolDay = (dayOfWeek !== "Shanba" && dayOfWeek !== "Yakshanba");

// 2-qism: Mantiqiy operatorlar (&&, ||) yordamida shartlarni tekshirish
if (isSchoolDay && imtihonBor) {
    console.log("Darhol imtihon zaliga kiring!");
} 
else if (!imtihonBor && vazifaBajarildi) {
    console.log("Siz darsga tayyorsiz, kirishingiz mumkin.");
} 
else if (isSchoolDay && !imtihonBor && !vazifaBajarildi) {
    console.log("Vazifani bajarmaganingiz uchun darsga kiritilmaysiz!");
} 

if (!isSchoolDay || darsQoldirildi) {
    console.log("Miriqib dam oling!");
}
