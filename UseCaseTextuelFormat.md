#USE CASE ( Format Textuel )

skinparam usecase{

	BackgroundColor DeepSkyBlue

	BorderColor DeepSkyBlue

	BackgroundColor<< Main >>  blue

	BorderColor<< Main >> blue

	ArrowColor DeepSkyBlue

	ActorBorderColor GreenYellow

	ActorFontName GreenYellow

	ActorBackgroundColor<< Human >> GreenYellow

}
actor Utilisateur_anonyme
actor Utilisateur_en_attente_de_confirmation
actor Utilisateur_confirmé


Utilisateur_confirmé --> (Se connecter)
rectangle Entraînement {
  (Se connecter) --> (Créer une séance)
  (Créer une séance) --> (Ajouter un exercice à la séance)
  (Créer une séance) --> (Enlever un exercice à la séance)
  (Créer une séance) --> (Consulter les exercices de la séance)
}
rectangle Performance {
  (Se connecter) --> (Consulter ses performances)
  (Consulter ses performances) --> (Comparer ses performances)
  (Consulter ses performances) --> (Comparer ses performances avec les autres utilisateurs)
}
rectangle Informations_complémentaires {
  (Se connecter) --> (Renseigner son poids)
  (Se connecter) --> (Renseigner son nombre d'heure de sommeil)
}

rectangle Inscription {
  Utilisateur_anonyme --> (S'inscrire)
  Utilisateur_en_attente_de_confirmation --> (Confirmer son inscription)
}

###End Of UseCaseTextuelFormat
