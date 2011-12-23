import os

env = Environment(ENV = os.environ)

source = Split("""bank.cpp file.cpp engine.cpp mixer.cpp resource.cpp parts.cpp vm.cpp
serializer.cpp sfxplayer.cpp staticres.cpp util.cpp video.cpp main.cpp
sysImplementation.cpp""")

env.ParseConfig('sdl-config --cflags --libs')
env.Append(CPPDEFINES = 'SYS_LITTLE_ENDIAN')
env.Append(LIBS = ['z'])
env.VariantDir('build', '.')
env.Program('game', ['build/%s' % file for file in source])
