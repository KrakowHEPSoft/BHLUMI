####################################################
LOCAL_LIB   =  400.a 
LIB_OBJECTS =  bhlumi.o bhlum4.o lumlog.o oldbis.o bhllog.o \
               model.o modl2a.o modl2b.o m2agzi.o repi.o
####################################################
############## What has to be built ################
all:	$(LOCAL_LIB) 
####################################################
F77 = gfortran
LD = $(F77)
AR = ar
RANLIB = ranlib
FFLAGS  =  -fno-automatic -ffixed-line-length-132 -fbackslash -C -O
########### collection of ibm  flags ###########
#FFLAGS  =  -O   -C -qextchk  -bloadmap:lmap
#FFLAGS  =  -C -qextchk -qinitauto=FF -bloadmap:lmap -qflttrap=overflow:underflow:zerodivide:invalid:enable
# LDFLAGS =  -O   -C -qextchk  -bloadmap:lmap
# LDFLAGS =  -C -qextchk -qinitauto=FF -bloadmap:lmap -qflttrap=overflow:underflow:zerodivide:invalid:enable
####################################################
.f.o:
	$(F77) $(FFLAGS) -c $<
####################################################
$(LOCAL_LIB): $(LIB_OBJECTS)
	$(AR) rv  $(LOCAL_LIB) $(LIB_OBJECTS)
####################################################
clean:
	rm -f *.o; rm -f *.a; rm -f *~ 
####################################################



