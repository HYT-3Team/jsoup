# Options JVM sélectionnées et justification:

## -XX:+UseG1GC

Ce flag a le but d'activer le ramassage-miettes *Garbage-First* (G1). Ceci pourrait réduire les pauses de collecte des ordures et améliorer la performance.
Ceci est adapté aux scénarios où jsoup pourrait traiter des documents XML ou HTML plus volumineux.

## -XX:+UnlockDiagnosticVMOptions

Ce flag a le but de débloquer les options de diagnostic pour une meilleure observabilité. Ceci pourrait fournir des informations plus approfondies sur le
comportement de la JVM, ce qui est utile pour analyser les performances de jsoup, et identifier les zones de problèmes.

## -XX:+ShowCodeDetailsInExceptionMessages

Ce flag a le but d'ajouter l'emplacement du bytecode dans les traces de pile pour faciliter le débogage. En faisant ceci, ça améliore la qualité du code et
aide les développeurs à tracer les problèmes plus efficacement dans les composants de parsing et dans le nettoyage de jsoup. 

## -XX:+AlwaysPreTouch

Ce flag a le but de garantir une allocation de pages mémoire dès le départ. Ceci améliore potentiellement le temps de réponse en évitant les retards d'allocation mémoire.

## -XX:+ExtendedDTraceProbes

Ce flag active les sondes DTrace supplémentaires plus détaillés pour observer l'activité de la JVM, ce qui nous permet de profiler les performances de jsoup
sous charge ou lors des opérations de parsing chargés.


P.S. Pas de lolcommits malheureusement, je code sur mon PC et je n'ai pas de webcam. :(
