cmake_minimum_required(VERSION 3.15)

set(CMAKE_EXPORT_COMPILE_COMMANDS true)

project(zlib LANGUAGES C)

set(CMAKE_C_STANDARD 99)

add_library(z STATIC
	adler32.c
	compress.c
	crc32.c
	gzio.c
	uncompr.c
	deflate.c
	trees.c
	zutil.c
	inflate.c
	infback.c
	inftrees.c
	inffast.c
)
target_compile_options(z PUBLIC -Wall -O3)
