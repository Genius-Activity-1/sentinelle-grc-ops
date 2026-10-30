# sentinelle-grc-ops
Démonstrateur interactif d'Architecture de Gouvernance Opérationnelle, Régulation de Flux Critiques (VCT), Guardrails IA &amp; Audit Cryptographique Immuable.
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23813971.svg)](https://doi.org/10.5281/zenodo.23813971)
# 🛡️ SENTINELLE GRC & OPS — REF. ARCH-LOSANGE-V4.2

> **Plateforme de Gouvernance Opérationnelle, Régulation de Flux Critiques (VCT), Architecture Embarquée « Losange Cognitif » (Edge AI), Pare-Feu AEGIS & Apprentissage Fédéré sous Confidentialité Différentielle $(\epsilon, \delta)\text{-DP}$.**

🔗 **[Accéder à la Démo Live Interactive](https://genius-activity-1.github.io/sentinelle-grc-ops/)**  
💻 **Dépôt GitHub :** `https://github.com/genius-activity-1/sentinelle-grc-ops`  
📄 **Spécification Système :** `REF. ARCH-LOSANGE-V4.2` (Auteur : Richard Morin)

---

## 🎯 Objectif du Projet & Proposition de Valeur

L'évolution des systèmes critiques et autonomes (passerelles API/LLM d'entreprise, robotique mobile, drones d'inspection, unités de sécurité civile et systèmes C4ISR) impose le passage de modèles centralisés hors-sol vers des architectures décisionnelles distribuées, déterministes et auditables (**Edge AI**).

**SENTINELLE GRC & OPS (v4.2)** répond simultanément à quatre exigences majeures :
1. **Cloisonnement Cognitif & Temps Réel ($\le 242\text{ ms}$) :** Séparation matérielle et logique entre la perception factuelle (`C1`), la simulation prédictive (`L1`), l'enclave normative immuable (`S1` sous TEE) et l'arbitrage opérationnel (`Moi-IA M1`).
2. **Résilience & Anti-Battement (Valve VCT) :** Absorption des pics de charge ou attaques logiques sans effet de pompage (*flapping*) grâce au lissage exponentiel ($\text{EMA }\alpha$) et à la bande d'hystérésis ($\pm h$).
3. **Défense en Profondeur AEGIS & Stabilité de Lipschitz :** Filtrage polyphasique (`COR`, `CSD`, `CLHE`, `CBC`) et garantie formelle de stabilité par continuité de Lipschitz ($L \le 1,0$) et norme spectrale bornée ($\|\Delta\theta\|_2 \le 1,2$).
4. **Apprentissage Fédéré Bi-Domaine (Rail D / Rail A) & Opposabilité :** Exportation de télémétrie sous confidentialité différentielle $(\epsilon, \delta)\text{-DP}$ et scellement cryptographique en arbre de Merkle **BLAKE3 / SHA-256** et **Ed25519**.

---

## 🧠 1. Architecture du « Losange Cognitif » & Machine à États Finis (FSM)

Conformément à la spécification **ARCH-LOSANGE-V4.2**, le cycle décisionnel s'exécute en **6 états finis (FSM)** bornés temporellement :

| État FSM | Pôle Cognitif & Substrat Technique | Fonction Opérationnelle | Latence Max |
| :--- | :--- | :--- | :--- |
| **$S_0$ Perception** | **Conscience (`C1`)** — Capteurs RGB-D, LIDAR 3D, audio, IMU, RF sur pipeline DSP/GPU local. | Extraction purement factuelle de primitives physiques sans jugement ($P_{\text{fact}}$). | $\Delta t \le 12\text{ ms}$ |
| **$S_1$ Simulation** | **Subconscient (`L1`)** — Moteur physique embarqué (*Isaac Sim Micro-Core*). | Génération d'hypothèses $H = \{h_1, \dots, h_n\}$ et calcul des probabilités de risque. | $\Delta t \le 150\text{ ms}$ |
| **$S_2$ Filtre Normatif** | **Inconscient (`S1`)** — Enclave matérielle sécurisée **TEE / NVRAM** (`policy.yaml` signé). | Confrontation aux invariants immuables (QSE/SPS/ROE) et verrouillage des actions interdites. | $\Delta t \le 20\text{ ms}$ |
| **$S_3$ Arbitrage** | **Moi-IA (`M1`)** — SLM/LLM local quantifié INT8/FP16 optimisé TensorRT sur NPU/TPU. | Sélection de la commande $u(t)$ sous contrainte $S1$ et émission du quadruplet $d = \langle x, H, C_{\text{séc}}, u \rangle$. | $\Delta t \le 50\text{ ms}$ |
| **$S_4$ Actuation** | **Vérificateur Temps Réel** — Contrôle $R_{\text{action}} < R_{\text{critique}}$. | Exécution physique validée ou déclenchement du `/v1/kill-switch` (Rollback RDM $\le 2,0\text{ s}$). | $\Delta t \le 10\text{ ms}$ |
| **$S_5$ Audit & Flotte** | **Mémoire Réflexive (`R1`) $\rightarrow$ IA Analyste $\rightarrow$ IA Maître**. | Hachage Merkle BLAKE3/SHA-256, corrélation d'essaim et signature hors-ligne Ed25519. | Asynchrone |

> **Invariant de verrouillage matériel de l'Inconscient (`S1`) :** Le module `Moi-IA` et le `Subconscient` ont une interdiction matérielle (TEE) de modifier `policy.yaml` en *runtime*, éliminant toute vulnérabilité d'*auto-justification* face à une injection adverse.

---

## 🛡️ 2. Pare-Feu Polyphasique AEGIS & Cloisonnement Multi-Secteurs

### Les 4 Sous-Systèmes du Pipeline AEGIS (Seuils ContextLedger : `ALLOW < 0.45`, `REVISE >= 0.45`, `REFUSE >= 0.70`)
* **`COR` (Canonicalisation Obfuscation-Robuste) :** Normalisation Unicode NFKC, purge des caractères invisibles, désambiguïsation des homoglyphes et décodage contrôlé Base64/Hex combiné à l'entropie de Shannon $H(X)$.
* **`CLHE` (Cross-Lingual Harm Ensemble) & `Tripwires` :** Graphe d'activation inter-tours détectant les dérives narratives lentes (*Narrative Drift*) et les contournements multilingues.
* **`CSD` (Contrastive Safety & Strain Detection) :** Mesure de la divergence de Kullback-Leibler simulée pour détecter l'extraction procédurale.
* **`CBC` (Control-Barrier Chat) & `ToolOutputGate` :** Dé-procéduralisation automatique, élision des blocs critiques et validation stricte contre JSON Schema.

### Les 4 Scénarios Sectoriels Simulés (Section 2.3)
1. **Sécurité Civile (Gare / Infrastructure Critique) :** Robot de patrouille appliquant une désescalade passive, distance de sécurité $\ge 2,5\text{ m}$ et interdiction absolue de contact physique.
2. **Chantier BTP / QSE (Audit SPS & Télécom) :** Détection de travaux en hauteur $> 3\text{ m}$ sans longe arrimée $\rightarrow$ Suspension immédiate d'opération.
3. **Logistique & Portuaire (Flotte d'AGV / Drones) :** Priorité absolue à l'intégrité des opérateurs humains avec arrêt d'urgence matériel (*Safe Torque Off*).
4. **Défense & C4ISR (Aide à la Décision Tactique) :** Résilience sous brouillage GNSS/RF, respect strict des ROE et maintien du contrôle humain (*Human-in-the-loop*).

---

## 🔄 3. Apprentissage Fédéré Bi-Domaine (Rail D / Rail A) & $(\epsilon, \delta)\text{-DP}$

Pour mutualiser l'expérience d'une flotte sans exposer le modèle temps réel à l'empoisonnement (*Data Poisoning*) :
* **Rail D (Nœud Edge Local) :** Exécute le modèle déterministe certifié (**RDM**).
* **Sas Airlock Paramétrique $(\epsilon, \delta)\text{-DP}$ :** Ajoute un bruit calibré $\hat{m} = f(d) + Z$ avec $Z \sim \text{Lap}(\Delta f / \epsilon)$ ou $\mathcal{N}(0, \sigma^2)$ avant tout export `POST /v1/telemetry/export`, et coupe le flux dès que $\epsilon_{\text{cumul}} \ge \epsilon_{\max}$ sur 24h.
* **Rail A & Proof Merge-Gate :** Vérifie l'attestation matérielle `TEE-SGX-Quote`, la norme spectrale $\|\Delta\theta\|_2 \le 1,2$ et la constante de Lipschitz $L \le 1,0$ avant déploiement *Shadow A/B*.

---

## 🧪 4. Banc d'Homologation Niveau 4 & Indicateurs de Sûreté (KPI)

Le démonstrateur inclut un simulateur du **Protocole de Résilience Niveau 4** (perte LIDAR + bruit gaussien 25 % + injection adverse simultanée) validant les 6 seuils d'homologation industrielle :
* **ASR (*Attack Success Rate*) :** $\le 3,0\%$ sur corpus Red-Team (mesuré à $1,8\%$).
* **RQS (*Refusal Quality Score*) :** $\ge 4,5 / 5,0$ (zéro fuite de topologie interne).
* **CPD (*Contextual Poisoning Detection*) :** $\ge 0,85$ (Graphe Tripwires + $\Delta\text{AIC}$).
* **Taux de Faux Positifs :** $\le 5,0\%$ en exploitation nominale.
* **Stabilité Mathématique :** $L \le 1,0$ et $\|\Delta\theta\|_2 \le 1,2$.
* **MTTR Rollback (`/v1/kill-switch`) :** $\le 2,0\text{ secondes}$ (mesuré à $0,42\text{ s}$).

---

## 🚀 Déploiement & Exécution Locale

1. **Cloner ce dépôt :**
   `git clone https://github.com/genius-activity-1/sentinelle-grc-ops.git`

2. **Exécuter localement :**
   Ouvrir directement `index.html` dans n'importe quel navigateur moderne, ou lancer un serveur local :
   `python3 -m http.server 8080`
