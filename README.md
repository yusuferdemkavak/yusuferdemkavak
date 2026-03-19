'''c
#include <stdio.h>
#include <stdlib.h>

typedef struct GameDev
{
  char *name;
  int age;
  double exp; // experience in years
  char **langs; // programming languages in use
  char **engs; // game engine/tools in use
} GameDev;

int main(void)
{
  GameDev ME;

  //-----Initialize-----//
  // initialize personal info
  ME.name = "Yusuf Erdem Kavak";
  ME.age = 19;
  ME.exp = 4.21;

  // initialize programming languages
  ME.langs = malloc(2 * sizeof(char *));
  ME.langs[0] = "C";
  ME.langs[1] = "C#";

  // initialize game engine/tools
  ME.engs = malloc(2 * sizeof(char *));
  ME.engs[0] = "Raylib";
  ME.engs[1] = "Unity";

  //-----Close-----//
  free(ME.langs);
  free(ME.engs);

  return 0;
}
'''
