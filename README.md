# Utkarsh Path Lab HRMS – setup (lagbhag 30 minute)

Files: `index.html` = staff page (staff ka link), `admin.html` = admin page (sirf aapka link), `firestore.rules` = security.

1. https://console.firebase.google.com par naya project banao. Plan: Spark (free) hi rakho, card ki zaroorat nahi.
2. Build > Authentication > Sign-in method > **Email/Password** enable karo.
3. Build > Firestore Database > Create (Mumbai region `asia-south1`).
4. Project settings > Your apps > **Web app** banao, jo config mile use `firebase-config.js` me paste karo.
5. Apna admin account banao: Authentication > Users > Add user (aapka email + strong password). Uska **User UID** copy karo.
6. Firestore > Start collection `admins` > Document ID = wo UID, ek field `ok: true`.
7. Computer par: `npm i -g firebase-tools`, `firebase login`, is folder me `firebase init` (project chuno, purani files overwrite mat karo), phir `firebase deploy`.
8. Links: staff = `https://<project>.web.app/`, admin = `https://<project>.web.app/admin.html`.

Pehli baar: admin login > Manage Branch me branch add karo > branch ke andar khade hokar "Location set karo" > Employees me staff add karo (mobile + 4 digit PIN). Staff ko sirf staff link do; wo "Add to Home Screen" kar le.

Dhyan do: PIN reset ke liye abhi staff ko delete karke dobara add karna padega. Isse upar ka security chahiye to OTP login baad me jodenge.
