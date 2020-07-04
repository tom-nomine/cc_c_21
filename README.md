# cc_c_21
#include <stdio.h>

#include "game.h"

int main()
{
    t_game * g = game_init();

    game_loop(g);

    print_player_coins(g->player); // Afficher le nombre de jetons du joueur
    
broker_new_hand(g); // Le croupier pioche
player_new_hand(g); // Le joueur pioce
print_player_hand(g->player); // Afficher la main du joueur
broker_place_bet(g); // Le croupier mise
player_place_bet(g); // Le joueur mise
sum_player_hand(g->player); /* Le joueur choisi la valeur de ses Valets
 et cette function "return" le score du joueur */

    print_turn_results(t_game * g, int p_hand); /* Afficher le score du croupier et du joueur
 (le score du joueur doit être donné par la
 variable p_hand) */

    return 0;
}

void game_loop(t_game * g)
{
}