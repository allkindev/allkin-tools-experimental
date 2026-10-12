# Creator

L'agent qui fabrique des outils pour Allkin. Tu lui décris ce que tu veux ; il te pose ses
questions dans un **formulaire**, écrit l'outil, le service ou la compétence selon le standard
Allkin, le **contrôle** et le met au point avec toi. Creator n'a pas de page à lui : c'est un
agent, dans la liste des agents, à qui l'on parle.

## À quoi ça sert

- **Créer un outil** : un programme qui tourne en continu, une page, un morceau de l'interface
  d'Allkin, un agent dédié — ou plusieurs à la fois.
- **Créer un service** : apprendre à Allkin comment joindre une API externe, pour que tes agents
  l'appellent avec ta clé.
- **Créer une compétence** : un savoir-faire qu'un agent charge à la demande.

Tout ce que Creator écrit respecte le **standard Allkin**, livré avec l'outil
(`standard/PLUGIN-STANDARD.md`, `standard/SERVICE-STANDARD.md`, `standard/SKILL-STANDARD.md`),
et il le vérifie lui-même après chaque modification.

## Mise en route

1. Installe Creator, puis accorde ses trois droits sur sa page. L'agent **Creator** et ton dépôt
   local sont créés à ce moment-là.
2. Ouvre la conversation de l'agent Creator (il est dans la liste des agents, en rose comme tout
   agent d'un outil) et dis-lui ce que tu veux.
3. Il te pose ses questions en une fois, dans un formulaire ; réponds, il écrit les fichiers,
   les contrôle, et termine en te disant quoi faire : installer, accorder un droit, recharger
   la page, démarrer le service.
4. Pour installer ce qu'il a écrit : page **Outils**, ton dépôt « Creator » y est une source ;
   **Installer**, puis les droits sur la page de l'outil. Un service se branche depuis la page
   **Services** ; une compétence depuis la page **Compétences**.

## Mettre au point

Quand un outil ne fait pas ce qu'il faut, dis-le à Creator : il lit le journal du service
(`read_tool_log`), relance le contrôle (`check_project`), corrige, augmente la version, et te
dit quoi refaire. Donne-lui l'erreur exacte que tu vois, c'est ce qui l'aide le plus.

## Où sont tes fichiers

Dans le dossier de travail de l'agent : `~/.allkin/plugin-data/creator/workspace/`, avec un
dossier `plugins/`, un dossier `services/` et un dossier `skills/`. Ce dossier est un **dépôt
local** : il apparaît dans la fenêtre *Dépôts* des pages Outils, Services et Compétences, et tes
créations y sont listées avec l'étiquette « Creator ».

Ce dossier **n'est pas supprimé** quand tu désinstalles Creator. Pour publier une création,
copie son dossier dans ton dépôt d'outils.

## Les droits demandés

| Droit | Pourquoi |
|-------|----------|
| Agent dédié | L'agent Creator, qui écrit les fichiers. Il n'a aucun accès à la machine en dehors de son dossier de travail |
| Dépôt | Faire du dossier de travail une source d'outils, de services et de compétences pour cet Allkin |
| Réseau | Laisser l'agent lire la documentation en ligne des API |

## Si ça ne marche pas

- **L'agent Creator n'apparaît pas** : un droit n'est pas accordé. Ouvre la page de l'outil.
- **Installer n'apporte rien** : la version n'a pas changé. Demande à Creator de l'augmenter.
- **L'interface de l'outil n'apparaît pas** : accorde ses droits sur sa page, puis recharge.
- **L'agent ne répond pas** : vérifie ton fournisseur IA dans les Paramètres d'Allkin.
