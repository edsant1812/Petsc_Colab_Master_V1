#!/bin/bash
.SILENT:
.DEFAULT_GOAL := all
HOME_DIR=${HOME}
GIT_DIR=${HOME_DIR}/Git
PETSC_DIR=${GIT_DIR}/petsc
PETSC_ARCH=arch-linux-c-opt
MPIEXEC=${PETSC_DIR}/${PETSC_ARCH}/bin/mpiexec
include ${PETSC_DIR}/lib/petsc/conf/variables
include ${PETSC_DIR}/lib/petsc/conf/rules

all: CompileCode

CompileCode: YourCode.o # rename with your file name
	-${CLINKER} -o YourCode YourCode.o ${PETSC_LIB}
	${RM} YourCode.o