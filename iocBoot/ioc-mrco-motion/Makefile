IOC_TOP=/cds/group/pcds/epics/ioc/common/ads-ioc/R0.6.2
IOC_INSTANCE_PATH := $(shell pwd)

# Set PRODUCTION_IOC to 1 to move from a testing to a production IOC:
PRODUCTION_IOC := 1

PROJECT_NAME := plc-mrco-motion
PROJECT_PATH := ../../lcls-plc-mrco-motion/lcls-plc-mrco-motion.tsproj
PLC = mrco_motion

PYTMC_OPTS :=
PREFIX = PLC:MRCO:MOTION

# With two $$, as in $$(IOC) below, this will be expanded in the
# environment of st.cmd:
DB_PARAMETERS := 'PREFIX=$(PREFIX):,IOCNAME=$$(IOC),IOC=$$(IOC)'

# If you know the netconfig name of the PLC, enter it here.  If specified, this
# will be used in place of the auto-detected IP address from the PLC project:
PLC_HOSTNAME :=
# You may also specify the AMS Net ID of the PLC, but it's usually OK to
# leave this blank as it can be found in the project:
PLC_AMS_NET_ID :=

include $(IOC_TOP)/iocBoot/templates/Makefile.base

