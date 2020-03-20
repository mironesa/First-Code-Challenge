# First-Code-Challenge
// Created on Thu March 19 2020
int l_motor = 0 ;
int r_motor = 2 ; 
int speed = 50 ;
int pause = 1000 ;
int l_bump = 8 ;
int r_bump = 9 ;

void foward () {
		motor(l_motor,speed) ; // go foward
		motor(r_motor,speed) ; 
} 

void r_turn () {
		motor(l_motor,speed); // right turn
		motor(r_motor,speed) ;
		msleep (pause) ;
}

int main () {
	printf("Hello, World!\n");
	return 0 ;

		while(digital(r_bump) ==1) {
		foward () ;
		} // approach wall
		
		while(digital(l_bump) ==1) {
		r_turn () ;
		} // face the wall
		ao() ;
		msleep(pause) ;
		
		return 0 ;
	}
