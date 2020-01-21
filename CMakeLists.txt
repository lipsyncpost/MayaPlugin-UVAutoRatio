#-
# ==========================================================================
# Copyright (c) 2018 Autodesk, Inc.
# All rights reserved.
# 
# These coded instructions, statements, and computer programs contain
# unpublished proprietary information written by Autodesk, Inc., and are
# protected by Federal copyright law. They may not be disclosed to third
# parties or copied or duplicated in any form, in whole or in part, without
# the prior written consent of Autodesk, Inc.
# ==========================================================================
#+


cmake_minimum_required(VERSION 2.8)

# include the project setting file
include($ENV{DEVKIT_LOCATION}/cmake/pluginEntry.cmake)

# specify project name
set(PROJECT_NAME UVAutoRatioPro$ENV{MAYA_VERSION})


# set SOURCE_FILES
set(SOURCE_FILES
   UVAutoRatio/GetSurfaceUVArea.cpp
   UVAutoRatio/GetSurfaceUVArea.h
   UVAutoRatio/GetUVShellSelectionStrings.cpp
   UVAutoRatio/GetUVShellSelectionStrings.h
   UVAutoRatio/main.cpp
   UVAutoRatio/MayaPCH.cpp
   UVAutoRatio/MayaPCH.h
   UVAutoRatio/MayaPlugin.cpp
   UVAutoRatio/MayaPlugin.h
   UVAutoRatio/MayaUtility.cpp
   UVAutoRatio/MayaUtility.h
   UVAutoRatio/MeshProcessor.cpp
   UVAutoRatio/Processor.cpp
   UVAutoRatio/ShellProcessor.cpp
   UVAutoRatio/ShellProcessor.h
   UVAutoRatio/Timer.cpp
   UVAutoRatio/Timer.h
   UVAutoRatio/Utility.cpp
   UVAutoRatio/Utility.h
   UVAutoRatio/UVAutoRatioPlugin.cpp
   UVAutoRatio/UVAutoRatioPlugin.h
   UVAutoRatio/UVAutoRatioPro.cpp
   UVAutoRatio/UVAutoRatioPro.h
   UVAutoRatio/UVAutoRatioPro_Setup.cpp
   UVAutoRatio/UVSpringLayout.cpp
   UVAutoRatio/UVSpringLayout.h
   UVAutoRatio/minmax.h
)

# set linking libraries
set(LIBRARIES
     OpenMaya Foundation OpenMayaAnim OpenMayaFX OpenMayaRender OpenMayaUI
)

# Build plugin
build_plugin()