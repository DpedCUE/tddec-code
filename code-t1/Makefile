#Set this to @ to keep the makefile quiet
SILENCE = @

#---- Outputs ----#
COMPONENT_NAME = t1
TARGET_LIB = \
	lib/lib$(COMPONENT_NAME).a
	
TEST_TARGET = \
	$(COMPONENT_NAME)_tests

#--- Inputs ----#
PROJECT_HOME_DIR = .
CPP_PLATFORM = Gcc

CPPUTEST_USE_EXTENSIONS = Y
CPPUTEST_WARNINGFLAGS += -Wno-long-long
CPPUTEST_WARNINGFLAGS +=-Wno-address
CPPUTEST_WARNINGFLAGS += -Wno-c++14-compat
CPPUTEST_WARNINGFLAGS += -Wall -Wswitch-default -Werror
#CPPUTEST_WARNINGFLAGS += -Wno-missing-prototypes
CPPUTEST_WARNINGFLAGS += -Wno-format-nonliteral -Wno-sign-conversion -Wno-pedantic
CPPUTEST_WARNINGFLAGS += -Wno-shadow -Wno-missing-field-initializers -Wno-unused-parameter
#CPPUTEST_CFLAGS = -std=c89
CPPUTEST_CFLAGS += -Wall -Wstrict-prototypes -pedantic -Wno-c++14-compat
LD_LIBRARIES = -lpthread

SRC_DIRS = \
	src/*\
	src/MyOS/Acme\

TEST_SRC_DIRS = \
	tests \
	tests/MyOS \
	tests/util \
	tests/devices \
	tests/HomeAutomation\
	tests/IO \
	mocks/IO \
	mocks
	
INCLUDE_DIRS =\
  .\
  $(CPPUTEST_HOME)/include/\
  include/*\
  mocks/IO \
  mocks

  
include $(CPPUTEST_HOME)/build/MakefileWorker.mk
