# LAB 10 : Démo Navigation Drawer et Fragments

Ce projet est une application Android développée entièrement en **Java** démontrant l'utilisation d'un menu de navigation latéral (**Navigation Drawer**) pour gérer dynamiquement plusieurs fragments au sein d'une seule activité principale.

---

## 🚀 Fonctionnalités

1. **Navigation Drawer (Menu Latéral) :**
   - Intègre un menu coulissant avec un en-tête d'application personnalisé (`nav_header_main.xml`).
   - Icônes vectorielles personnalisées pour chaque option du menu (Home, Dashboard, List).

2. **Gestion Dynamique des Fragments :**
   - Les transitions entre les écrans se font sans recharger l'activité principale, en utilisant `FragmentManager` et `FragmentTransaction`.
   - Trois fragments distincts :
     - **Fragment 1 (BlankFragment) :** Un fond rose (#F8BBD0) avec le texte "Fragment 1".
     - **Fragment 2 (BlankFragment2) :** Un fond bleu (#3F51B5) avec le texte "Fragment 2".
     - **Fragment List (FragmentList) :** Un `ListFragment` affichant une liste simple de 10 éléments (Item 1 à Item 10).

---

## 📁 Structure du Projet

Les fichiers principaux créés et modifiés sont :

* **[MainActivity.java](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/java/com/example/lab_10_sas_houda/MainActivity.java) :** Initialise le DrawerLayout, la Toolbar, l'ActionBarDrawerToggle pour ouvrir/fermer le menu, et gère les clics avec `onNavigationItemSelected`.
* **[BlankFragment.java](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/java/com/example/lab_10_sas_houda/BlankFragment.java) & [BlankFragment2.java](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/java/com/example/lab_10_sas_houda/BlankFragment2.java) :** Contrôleurs simples pour les deux premiers fragments.
* **[FragmentList.java](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/java/com/example/lab_10_sas_houda/FragmentList.java) :** ListFragment utilisant un `ArrayAdapter` pour générer et lier une liste d'éléments.
* **[activity_main.xml](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/res/layout/activity_main.xml) :** Contient le composant racine `DrawerLayout`, la Toolbar, la vue incluse pour le contenu principal et le `NavigationView`.
* **[content_main.xml](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/res/layout/content_main.xml) :** Contient le conteneur `FrameLayout` (`@+id/contenu`) recevant les fragments.
* **[activity_main_drawer.xml](file:///c:/Users/HP%20PRO/AndroidStudioProjects/LAB_10_SAS_Houda/app/src/main/res/menu/activity_main_drawer.xml) :** Menu XML liant les boutons du Drawer à leurs icônes respectives.

---

## 🛠️ Instructions d'Installation et d'Exécution

### Prérequis
- **Android Studio** (Koala ou plus récent).
- **JDK 11** ou supérieur.
- Un émulateur ou appareil de test avec **API 24** au minimum.

### Compilation et Lancement
1. Ouvrez le projet dans Android Studio :
   `File -> Open -> Sélectionner LAB_10_SAS_Houda`
2. Compilez le projet via le terminal Gradle de votre choix :
   ```bash
   .\gradlew assembleDebug
   ```
3. Lancez l'application sur votre appareil/émulateur de test.
