GlisyUniform
============

## Installation

```sh
$ clib install glisy/uniform --save
```

## Usage

```c
#include <glisy/uniform.h>
#include <glisy/color.h>
#include <glisy/math.h>

int
main (void) {
  GlisyColor color;
  GlisyUniform uColor;

  glisyColorInit(&color, "blue", 0);
  glisyUniformInit(&uColor, "uColor", GLISY_UNIFORM_VECTOR, 3);
  glisyUniformSet(&uColor, &vec3(color.r, color.g, color.b), sizeof(vec3));
  glisyUniformBind(&uColor, 0); // current bound program

  return 0;
}
```

## License

MIT
