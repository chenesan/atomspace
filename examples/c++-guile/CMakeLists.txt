
ADD_EXECUTABLE(PrimitiveExample
	PrimitiveExample.cc
)

TARGET_LINK_LIBRARIES(PrimitiveExample
	smob
	atomspace
	clearbox
)

ADD_LIBRARY (example SHARED
	ExampleSCM.cc
)

TARGET_LINK_LIBRARIES(example
	smob
	atomspace
)

# This is what the install should look like.
# INSTALL (TARGETS example DESTINATION "lib${LIB_DIR_SUFFIX}/opencog")
# INSTALL (FILES opencog/example.scm DESTINATION "${DATADIR}/scm/opencog")
