# 🛡️ SENTINELLE GRC & OPS (v3.1 Unified Suite)

> **Démonstrateur interactif d'Architecture de Gouvernance Opérationnelle, Régulation de Flux Critiques (VCT), Guardrails IA & Audit Cryptographique Immuable.**

🔗 **[Accéder à la Démo Live Interactive](#)** *(Remplace le `#` par ton lien GitHub Pages une fois activé, ex: `https://ton-pseudo.github.io/sentinelle-grc-ops/`)*

---

## 🎯 Objectif du Projet & Proposition de Valeur

Dans les environnements critiques (Cloud, API Gateways, passerelles LLM d'entreprise, systèmes industriels et opérations à haute volumétrie), les directions techniques et générales font face à trois défis simultanés :
1. **Résilience & Anti-Battement (SLA) :** Absorber les pics de charge ou attaques applicatives sans provoquer d'effet de pompage (*flapping*) ni d'interruption sèche.
2. **Gouvernance Financière & FinOps :** Chiffrer en temps réel l'arbitrage entre le coût de la prévention (PRA, cache, rate-limiting) et le coût de l'indisponibilité ou de la dérive OPEX.
3. **Opposabilité & Conformité Réglementaire :** Garantir la séparation des pouvoirs (**ISO 27001**, **NIS 2**, **DORA**) et l'intégrité mathématique des journaux d'audit (**ISO 9001**, **EU AI Act**).

**SENTINELLE GRC & OPS** est une implémentation de référence *Zero-Dependency / Edge-First* démontrant comment résoudre ces problématiques en temps réel directement côté client.

---

## 💼 Cas d'Usage Entreprise & Scénarios Simulés (Playbooks)

Le démonstrateur intègre des scénarios interactifs directement transposables aux enjeux d'un COMEX, d'une DSI, d'un SOC ou d'une Direction Industrielle :

### 1. Arbitrage Stratégique & Financier (Module 2 — COMEX / DSI / DAF)
| Scénario Entreprise | Problématique Métier | Réponse SENTINELLE & Impact ROI |
| :--- | :--- | :--- |
| **Cas A — Continuité d'Activité & SLA (PRA)** | Rupture d'exploitation (arrêt ERP, e-commerce ou chaîne logistique) entraînant de lourdes pénalités SLA. | Régulation dynamique VCT et bascule *Failover* sans perte de transaction (**RTO < 2 min**, **Disponibilité 99,95 %**). |
| **Cas B — FinOps Cloud & Passerelle IA** | Explosion des coûts OPEX liée aux boucles d'appels API, requêtes redondantes et consommation de jetons LLM. | Lissage de flux, cache déterministe à *Cooldown* et télémétrie binaire 24 octets (**-42 % d'OPEX Cloud**, **-82 % bande passante**). |
| **Cas C — Risque Cyber & Tiers (NIS 2 / DORA)** | Compromission d'un flux partenaire, frais d'investigation forensique élevés et risque de sanction réglementaire. | Séparation des pouvoirs par Quorum 3/3 et scellement probatoire SHA-256 (**-75 % sur le MTTR**, **opposabilité juridique 100 %**). |

### 2. Sécurité Opérationnelle, Cyber & IA Temps Réel (Module 6 — Industrie / SOC / AI Safety)
* **Sécurité Industrielle HSE (ISO 13849) :** Détection par capteurs LiDAR/Vision d'un opérateur franchissant le périmètre d'une cellule robotisée $\rightarrow$ Arbitrage multi-agents déclenchant l'arrêt *Safe Torque Off* immédiat.
* **Continuité Logistique & Chaîne du Froid (ISO 9001 / GDP) :** Détection d'une dérive thermique (+4,8 °C) sur chambre froide pharmaceutique $\rightarrow$ Bascule automatique sur groupe froid redondant N+1 avant perte de lot.
* **Défense SOC & Anti-Exfiltration API (NIS 2) :** Identification d'un export massif anormal depuis un ASN inhabituel $\rightarrow$ Révocation préventive du jeton tiers et scellement forensique des preuves.
* **Pare-Feu LLM Polyphasique (EU AI Act / OWASP LLM) :** Neutralisation en direct des tentatives de *Prompt Injection* obfusquées en Base64/Homoglyphes et dé-procéduralisation automatique des requêtes à risque.

---

## ⚙️ Architecture & Les 6 Modules Fonctionnels

### 1. Régulation de Flux VCT & Filtrage Entropique (API / LLM / IoT)
* **Analyseur d'Entropie de Shannon :** Calcul en temps réel de $H(X) = -\sum P(x)\log_2 P(x)$ sur les charges utiles entrantes pour détecter l'obfuscation et les motifs d'injection avant admission.
* **Loi de Contrôle à Hystérésis & Lissage EMA :** Régulation continue de l'ouverture de la valve selon :
  $$V_{\text{out}}(t) = \epsilon + (1 - \epsilon) \cdot \sigma\Big( a(\hat{\lambda}_t - \kappa_{\text{eff}}) - b(\hat{R}_t - \theta_{\text{eff}}) \Big)$$
* **Télémétrie Binaire 24 Octets (`FRCv3`) :** Sérialisation Big-Endian (`ArrayBuffer` / `DataView` au format `>HBBffQI`) réduisant de **82 %** l'empreinte réseau par rapport au JSON verbeux.

### 2. Moteur Décisionnel COMEX / DSI (ROI, FinOps & Détection $\Delta\text{AIC}$)
* **Simulateur d'Arbitrage TCO / EBITDA :** Évaluation financière sur 3 scénarios d'entreprise universels (Continuité PRA/SLA, FinOps Cloud & Passerelle IA, Risque Cyber & Tiers).
* **Qualification Statistique de Dérive :** Sélection automatique de modèle par critères d'information d'Akaike ($\text{AIC} = 2k + n\ln(\text{RSS}/n)$) et Bayésien ($\text{BIC}$) pour éliminer les faux positifs liés au bruit capteur ($\sigma$).

### 3. Quorum Multi-Parties (3/3) & Proxy d'Audit IA
* **Séparation des Pouvoirs (MPC 3/3) :** Déblocage des opérations critiques conditionné à la convergence des signatures **COO (Opérations)**, **QSE/GRC (Risques)** et **RSSI (Cyber)**.
* **Proxy de Diagnostic à Haute Disponibilité :** Moteur d'assertion déterministe local avec cache *Cooldown* anti-spam et synthèse vocale (`Web Speech API`) pour briefing en salle de crise.

### 4. Registre d'Audit Immuable (`ContextLedger` SHA-256)
* **Chaînage Cryptographique Natif :** Chaque événement validé selon le schéma d'invariants `S0` est haché via l'API `Web Crypto (SHA-256)` en incluant le hash du bloc précédent.
* **Simulateur Forensique d'Altération BDD :** Permet de simuler une corruption malveillante en mémoire et d'exécuter un audit cryptographique qui identifie et répare la rupture de chaîne.
* **Décroissance Temporelle EWMA :** Pondération dynamique des risques historiques selon $W(t) = W_0 \cdot e^{-\lambda \Delta t}$.

### 5. Matrice de Conformité Réglementaire
* Cartographie directe entre les mécanismes algorithmiques de la plateforme et les exigences **NIS 2 (Art. 21)**, **DORA**, **ISO/IEC 27001:2022 (A.5.3 / A.8.15)** et **ISO 9001:2015 (§9.1 / §10.2)**.

### 6. AI Safety Guardrails (COR / CSD / CBC) & Orchestration Multi-Agents « Losange »
* **Pipeline Sentinelle Polyphasique :** Canonisation Unicode/NFKC, suppression des caractères invisibles, détection d'homoglyphes et décodage Base64 (`COR`), graphe de co-occurrence (`Tripwires`), score de dérive procédurale (`CSD`) et barrière de contrôle (`CBC`).
* **Architecture Cognitive en Losange (`C1-L1-S1-Moi-R1`) :** Séparation stricte entre la perception factuelle brute (`C1`), l'inférence probabiliste (`L1`), les invariants de sécurité (`S1`), l'arbitrage exécutif (`Moi-IA`) et la trace réflexive scellée (`R1`).

---

## 🚀 Déploiement & Exécution Locale

Aucune étape de compilation (*build*) ni dépendance serveur n'est requise :

1. **Cloner ce dépôt :**
   `git clone https://github.com/VOTRE-PROFIL/sentinelle-grc-ops.git`

2. **Exécuter localement :**
   Ouvrir directement `index.html` dans n'importe quel navigateur moderne, ou lancer un serveur local :
   `python3 -m http.server 8080`

---

## 📄 Exports & Interopérabilité SIEM

La plateforme permet de générer en un clic :
* **Le Certificat d'Homologation Complet (`.md`)** incluant l'état mathématique du régulateur et les empreintes SHA-256.
* **L'Export SIEM (`.csv`)** directement ingérable par Splunk, Elastic SIEM ou Datadog.