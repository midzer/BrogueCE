# Emscripten

## Build

```
emmake make
```

## Link

```
emcc -O3 -flto -fno-rtti -fno-exceptions src/*/*.o -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS=png -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@funcs.txt -sINITIAL_MEMORY=128mb -sSTACK_SIZE=1048576 -sENVIRONMENT=web --preload-file bin/assets/@assets/ --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
