TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build an ioc application
# Use PROD_IOC_RTEMS for RTEMS only
# Use PROD_IOC_Linux for Linux only
PROD_IOC = rp100

# rp100.dbd will be created and installed
DBD += rp100.dbd

# rp100.dbd will be made up from these files:
rp100_DBD += base.dbd
rp100_DBD += iocAdmin.dbd
rp100_DBD += asSupport.dbd
rp100_DBD += asyn.dbd
rp100_DBD += drvAsynSerialPort.dbd
rp100_DBD += drvAsynIPPort.dbd
rp100_DBD += stream.dbd

# <name>_registerRecordDeviceDriver.cpp will be created from <name>.dbd
rp100_SRCS += rp100_registerRecordDeviceDriver.cpp
rp100_SRCS_DEFAULT += rp100Main.cpp

# Add locally compiled object code
#rp100_SRCS += dbSubExample.c

rp100_LIBS += devIocStats
rp100_LIBS += autosave
rp100_LIBS += asyn
rp100_LIBS += stream
rp100_LIBS += $(EPICS_BASE_IOC_LIBS)

ifdef PCRE
LIB_LIBS += pcre2
else
ifneq ($(words $(PCRE_LIB) $(PCRE_INCLUDE)),0)
PROD_SYS_LIBS_DEFAULT += pcre2
PROD_SYS_LIBS_WIN32 += $(PCRE_LIB)\\pcre
SHRLIB_DEPLIB_DIRS += $(PCRE_LIB)
USR_LDFLAGS+=-L$(PCRE_LIB)
endif
endif

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE
