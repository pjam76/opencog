ADD_SUBDIRECTORY (file)

# The hypertable code never worked, and according to bug #567,
# it doesn't compile either.
# IF (HYPERTABLE_FOUND AND HAVE_EXPAT)
#    ADD_SUBDIRECTORY (hypertable)
# ENDIF (HYPERTABLE_FOUND AND HAVE_EXPAT)

IF (ODBC_FOUND)
	ADD_SUBDIRECTORY (sql)
ENDIF (ODBC_FOUND)

IF (HAVE_ZMQ)
    ADD_SUBDIRECTORY (zmq)
ENDIF (HAVE_ZMQ)

# I give up. This doesn't work, and I can't debug it.
# IF (HAVE_XML)
# 	ADD_SUBDIRECTORY (xml)
# ENDIF (HAVE_XML)

