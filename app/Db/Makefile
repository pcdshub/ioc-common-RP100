TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

#----------------------------------------------------
#  Optimization of db files using dbst (DEFAULT: NO)
#DB_OPT = YES

#----------------------------------------------------
# Create and install (or just install)
# databases, templates, substitutions like this
DB_INSTALLS += $(IOCADMIN)/db/iocSoft.db
DB_INSTALLS += $(AUTOSAVE)/db/save_restoreStatus.db
DB_INSTALLS += $(ASYN)/db/asynRecord.db
DB += rp100.db

#----------------------------------------------------
# Create and install (or just install)
# Archive files, templates, substitutions like this
#
ARCHIVE += rp100.archive

#----------------------------------------------------
# Create and install (or just install)
# Autosave request files, templates, substitutions like this
#
REQ += rp100.req

# Nothing to build for autosave, just install from $AUTOSAVE/db
DB_INSTALLS += $(AUTOSAVE)/db/save_restoreStatus.db

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE
