find_all_sources(. utils_SRCS)

list(REMOVE_ITEM utils_SRCS ./WindowsShortcut.cpp)
list(REMOVE_ITEM utils_SRCS ./EdenVideoArtUpdater.cpp)
if(TARGET_WIN32)
  list(REMOVE_ITEM utils_SRCS ./GLUtils.cpp)
  list(REMOVE_ITEM utils_SRCS ./LCDFactory.cpp)
endif(TARGET_WIN32)
add_sources(${utils_SRCS})
