# 👋 Koffi Innocents Kouassi — Finance durable & Data (ESG/Climat)
 
🎓 **Master 2 — Finance durable / Finance internationale & soutenable**  
Je développe des livrables à l’interface **finance + données + durabilité** : analyse climat, automatisation, reporting ESG et visualisation orientée décision.
 
➡️ **Objectif actuel : stage de fin d’études** (ESG / Sustainable Finance / Data & Reporting / RSE)
 
 
 ## 🔗 Liens rapides
 **LinkedIn** : https://www.linkedin.com/in/koffi-innocents-kouassi/
 **CV (PDF)** : *à ajouter*
 **Email** : innocentskkouassi@gmail.com
 
 
## 💼 Positionnement
Je me positionne sur des missions où il faut :
Structurer et fiabiliser des données ESG/climat
Produire des analyses claires pour des décisions d’investissement/reporting
Transformer des besoins métier en livrables concrets (fichiers, dashboards, notes d’analyse)

 

## 🧰 Compétences
 **ESG / Climat** : ITR, scoring carbone, lecture de méthodologies, analyse sectorielle
 **Data** : nettoyage, matching, contrôles qualité, structuration de jeux de données
 **Outils** : Excel avancé, VBA, Python, R, visualisation, documentation
 **Reporting** : logique CSRD/RSE, construction d’indicateurs, synthèse opérationnelle
 
 
## 🚀 Projets (à venir)
Les projets seront ajoutés progressivement, avec pour chacun :
1. **Contexte & objectif métier**
2. **Données & méthodologie**
3. **Résultats clés (KPI / insights)**
4. **Limites & pistes d’amélioration**
5. **Documentation d’exécution** (reproduire l’analyse pas à pas)
 #!/usr/bin/env bash
définir -euo pipefail

si [ " $# " -lt 2 ]; alors
  echo "Utilisation : $0 <numéro> <nom_projet>" 
  echo "Exemple : $0 1 \"Analyse Rendus Portefeuilles\"" 
  sortie 1
fi

NUMÉRO_DE_PROJET= " $1 "
changement
NOM_DU_PROJET= "$*"

slugify () {
  echo " $1 " \
 
    | tr '[:upper:]' '[:lower:]' \
  
    | sed -E 's/[^a-z0-9]+/-/g; s/^-+//; s/-+$//'
}

PROJECT_SLUG= " $(slugify " $PROJECT_NAME " ) "
PROJECT_DIR= "projets/ ${PROJECT_NUMBER} - ${PROJECT_SLUG} "

si [ -d " $PROJECT_DIR " ]; alors
  echo "Le dossier $PROJECT_DIR existe déjà." 
  sortie 1
fi

mkdir -p " $PROJECT_DIR " /{src,excel,reports,data,outputs}

créer " $PROJECT_DIR /excel/.gitkeep" " $PROJECT_DIR /data/.gitkeep" " $PROJECT_DIR /outputs/.gitkeep"   

cat > " $PROJECT_DIR /PROJECT.md" << EOT
# ${PROJECT_NUMBER}) ${PROJECT_NAME}

## Contexte & objectif métier
- À compléter.

## Données et méthodologie
- Script R : \`src/main.R\`
- Fichier Excel : \`excel/\`
- Rapport : `reports/rapport.pdf`
- Méthodologie : à compléter.

## Résultats clés (KPI / insights)
- KPI 1 : à compléter.
- KPI 2 : à compléter.
- Insight principal : à compléter.

## Limites & pistes d'amélioration
- Limite : à compléter.
- Amélioration : à compléter.

## Documentation d'exécution
1. Installer R et les packages nécessaires.
2. Placez les sources dans \`excel/\` ou \`data/\`.
3. Exécuter \`Rscript src/main.R\`.
4. Consulter les sorties dans \`outputs/\` et le rapport dans \`reports/\`.
EOT

cat > " $PROJECT_DIR /src/main.R" << 'EOT'
# Script de démarrage du projet
message( "Projet prêt : ajoutez ici votre pipeline R" )
EOT

echo "✅ Projet initialisé dans : $PROJECT_DIR " 
echo "Étapes suivantes :" 
echo " 1) Copiez votre script R dans $PROJECT_DIR /src/" 
echo " 2) Copiez vos fichiers Excel dans $PROJECT_DIR /excel/" 
echo " 3) Copiez votre rapport dans $PROJECT_DIR /reports/" 
echo " 4) Mettre à jour $PROJECT_DIR /PROJECT.md"
 
## 📌 Roadmap du portfolio
 Ajouter les projets un par un avec documentation complète
 Standardiser un template de repo commun (structure, conventions, README)
 Ajouter des exemples de données anonymisées quand c’est possible
 
 
 ## 📫 Contact
Pour échanger sur un stage ou un projet **ESG & data** : **innocentskkouassi@gmail.com**
 
EOF
)
