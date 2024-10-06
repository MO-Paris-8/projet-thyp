zenuml
title Processus de Gestion des Donnees des abonnement SDP

Client->PageAccueil.show() {
    PageAccueil->Utilisateur: Remplir le formulaire {
        if(Formulaire soumis?) {
            GoogleSheets.send(data) {
                GoogleSheets->DataPubliee: Donnees accessibles
                DataPubliee->PageData.show() {
                    if(Ligne cliquee?) {
                        PageData->Popup.show() {
                            Popup->Utilisateur: Afficher details supplementaires
                            @return
                            Popup->PageData: Fermer popup
                        }
                    }
                }
            }
        } else {
            PageAccueil->Utilisateur: Afficher message d'erreur
            @return
        }
    }
}
                }
            }
        } else {
            PageAccueil->Utilisateur: Afficher message d'erreur
            @return
        }
    }
}
