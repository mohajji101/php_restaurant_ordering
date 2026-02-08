# Nidaamka Dalbka Maqaayadda (PHP Restaurant Ordering System)

Mashruucan waa nidaam casri ah oo loogu talagalay maareynta iyo dalbka cuntada maqaayadda. Wuxuu u qeybsan yahay laba qeybood oo waaweyn: Qeybta Macaamiisha (User Side) iyo Qeybta Maamulka (Admin Side). Mashruucan waxaa lagu dhisay **PHP** iyo **MySQL**.

## Tilmaamaha Muhiimka ah (Key Features)

### 1. Qeybta Macaamiisha (User Features)
- **Koonto Sameysasho (Registration)**: Macaamiishu way is-diiwaangelin karaan si ay u dalbadaan cunto.
- **Galitaanka (Login)**: Galitaanka koontada si loo maamulo dalabaadka iyo macluumaadka shaqsiga.
- **Daalacashada Cuntada (Browse Menu)**: Eegidda liiska cuntada, qiimaha, iyo sawirada cuntada.
- **Dalbka (Ordering)**: Ku darista cuntada "Cart"-ka iyo dhameystirka dalabka (Checkout).
- **La Socodka Dalabka (Order Tracking)**: Macaamiishu waxay arki karaan heerka dalabkooda (Pending, Completed, Cancelled).
- **Profile-ka**: Wax ka bedelka macluumaadka shaqsiga sida magaca iyo lambarka taleefanka.

### 2. Qeybta Maamulka (Admin Features)
- **Dashboard**: Warbixin guud oo ku saabsan dalabaadka, dakhliga, iyo tirada macaamiisha.
- **Maareynta Cuntada (Menu Management)**: Ku darista, wax ka bedelka, iyo tirtirka cuntada (Categories & Products).
- **Maareynta Dalabaadka (Order Management)**: Maamulaha wuu arki karaa dalabaadka cusub, wuxuuna bedeli karaa heerka dalabka (Status update).
- **Warbixinada (Reports)**: Eegidda taariikhda dalabaadka iyo dakhliga soo galay.

## Tignoolajiyada La Isticmaalay (Technologies Used)
- **Luqadda Backend-ka**: PHP (Native)
- **Keydka Xogta**: MySQL
- **Frontend-ka**: HTML, CSS, JavaScript
- **Web Server**: Apache (via XAMPP/WAMP)

## Shuruudaha (Requirements)
Si aad u kiciso mashruucan, waxaad u baahan tahay:
1.  **XAMPP** ama **WAMP** server (oo wata PHP iyo MySQL).
2.  Web Browser (Google Chrome, Firefox, etc.).
3.  Text Editor (VS Code) haddii aad rabto inaad wax ka bedesho koodka.

## Sida Loo Rakibo (Installation Steps)

Raac tillaabooyinkan si aad u kiciso mashruuca kombiyuutarkaaga:

### Tallaabada 1aad: Diyaarinta Faylasha
1.  Soo deji mashruuca (Download/Clone).
2.  Nuqul ka samee gal-ka (folder) mashruuca oo gee `C:\xampp\htdocs\` (haddii aad isticmaaleyso XAMPP).
    - Tusaale: `C:\xampp\htdocs\php_restaurant_ordering`

### Tallaabada 2aad: Diyaarinta Database-ka
1.  Kici **XAMPP Control Panel** oo start dheh **Apache** iyo **MySQL**.
2.  Fur browser-kaaga oo tag `http://localhost/phpmyadmin`.
3.  Samee Database cusub oo magaciisu yahay **`restaurant_db`**.
4.  Soo deji (Import) faylka SQL-ka ah ee ku jira `scripts/` (haddii uu jiro `schema.sql`) ama isticmaal `scripts/create_db.php` iyo `scripts/init_db.php` si aad u sameyso tables-ka loona shubo xogta bilowga ah.
    - Haddii aad aqoon u leedahay isticmaalka terminal-ka, waxaad wadi kartaa:
      ```bash
      php scripts/init_db.php
      ```

### Tallaabada 3aad: Hagaajinta Xiriirka (Configuration)
1.  Fur faylka `config/database.php`.
2.  Hubi in macluumaadka database-ka ay sax yihiin (Host, Username, Password, Database Name).
    ```php
    define('DB_HOST', 'localhost');
    define('DB_USER', 'root');
    define('DB_PASS', '');
    define('DB_NAME', 'restaurant_db');
    ```

### Tallaabada 4aad: Kicinta Mashruuca
1.  Fur browser-kaaga.
2.  Qor cinwaankan: `http://localhost/php_restaurant_ordering/views/home.php`
    - (Hubi in magaca folder-ka uu sax yahay).

## Qaab Dhismeedka Mashruuca (Project Structure)

- **`config/`**: Faylasha habeynta (Configuration files) sida `database.php`.
- **`public/`**: Faylasha dadweynaha sida sawirada (images), CSS, iyo JS.
- **`scripts/`**: Saxeexyada (Scripts) loogu talagalay abuurista iyo buuxinta database-ka.
- **`src/`**: Koodka asalka ah (Source code) sida Helpers iyo Classes.
- **`views/`**: Bogagga (Pages) uu arko isticmaaluhu.
    - **`admin/`**: Bogagga maamulka (Dashboard, Products, Orders).
    - **`auth/`**: Bogagga galitaanka iyo diiwaangelinta (Login, Register).
    - **`partials/`**: Qeybaha soo noqnoqda (Header, Footer, Navbar).
    - **`home.php`**: Bogga hore ee maqaayadda.
    - **`cart.php`**: Bogga "Cart"-ka ama dambiisha dalabka.
    - **`checkout.php`**: Bogga lacag bixinta iyo dhameystirka dalabka.

---
Mahadsanid!
