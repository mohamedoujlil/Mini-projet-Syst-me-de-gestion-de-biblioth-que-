# Mini-projet-Syst-me-de-gestion-de-biblioth-que-
Système de gestion de bibliothèque utilisant les structures de données (listes, piles, files, et arbres) et les fichier
INTRODUCTION 
Les listes chaînées sont des structures de données fondamentales en informatique, largement utilisées pour stocker et manipuler des collections d'éléments de manière dynamique. Elles offrent une alternative flexible et efficace aux tableaux statiques, permettant l'insertion, la suppression et la modification des éléments de manière efficace.
Ce projet a pour objectif de trouver un livre s’il est disponible à l’aide des listes chaînées. Nous allons concevoir une classe de liste chaînée en utilisant un ensemble de nœuds liés entre eux pour stocker les données. Chaque nœud contient à la fois une valeur « BOOK » et une référence vers le nœud suivant dans la liste.

INCLUSION DE BEBLEOTHEQUE

#include <stdlib.h>
#include <stdio.h>
#include <string.h>



INSTRECTIONS DU PROGRAMME

struct Book {
    char title[100];
    char author[100];
    char isbn[20];
    int is_available;
};
struct Node {
struct Book book;
struct Node* next;
};
struct Node* create_book(struct Book book) {
struct Node* node = (struct Node*)malloc(sizeof(struct Node));
node->book = book;
node->next = NULL;
return node;
}

int main() {  
struct Book book1 = {       
.title = "The Hitchhiker's Guide to the Galaxy",
.author = "Douglas Adams",      
.isbn = "9780345391803",        
.is_available = 1
};

struct Book book2 = {
.title = "The Lord of the Rings",
.author = "J.R.R. Tolkien",
.isbn = "9780544003415",
.is_available = 0   
};

struct Book book3 = {
.title = "1984",      
.author = "George Orwell",
.isbn = "9780451524935",
.is_available = 1
};

struct Node* head = create_book(book1);
head->next = create_book(book2);
head->next->next = create_book(book3);
struct Node* current = head;
while (current != NULL) {
printf("%s by %s (ISBN: %s), available: %s\n",
current->book.title,
current->book.author,
current->book.isbn,
current->book.is_available ? "yes" : "no"
);

current = current->next;
}

return 0; 
}


CONCLISION


En conclusion, la saisie du nom d'un livre dans un programme et la vérification de son existence sont désormais à portée de main grâce aux avancées technologiques. L'utilisation de programmes et d'applications dédiés facilite grandement la recherche de livres et offre une expérience plus efficace.
Que vous soyez un lecteur passionné, un chercheur ou simplement curieux, ces programmes vous permettent d'accéder rapidement et facilement à une mine d'informations sur les livres du monde entier. Ils vous évitent de perdre du temps à fouiller des bibliothèques physiques ou à naviguer sur Internet à la recherche de renseignements.
Grâce à ces programmes, vous pouvez non seulement vérifier si un livre existe, mais aussi obtenir des détails précieux tels que l'auteur, la date de publication, le résumé et même des critiques. Cela vous aide à prendre des décisions éclairées sur vos lectures et à découvrir de nouveaux titres qui pourraient susciter votre intérêt
Et les mêmes étapes on peut appliquer pour créer un autre projet qui contient des magazines ou des journaux.


















