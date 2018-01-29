# SMSC-GW-logs
# This directory contains configuration data of SMSC to SMSC SS7 connection
# The connection diagram is as follows
# SS7Simulator <-> SMSCGW <-> SMSCGW <-> SS7Simulator
# Current status of this connection is, Connection is established
# SRI-Request is going upto SS7Simulator on server side (Right most) but with error
# Error is given below

22:48:13,973 INFO  [HrSriServerSbb] (SLEE-EventRouterExecutor-3-thread-1) 
Home routing: HrSriServerSbb: Received SEND_ROUTING_INFO_FOR_SM_REQUEST = SendRoutingInfoForSMRequestWrapper [wrapped=SendRoutingInfoForSMRequest [DialogId=1, msisdn=ISDNAddressString[AddressNature=international_number, NumberingPlan=ISDN, Address=1234], sm_RP_PRI, serviceCentreAddress=ISDNAddressString[AddressNature=international_number, NumberingPlan=ISDN, Address=22220]]] Dialog=MAPDialogSmsWrapper [wrappedDialog=MAPDialog: LocalDialogId=1 RemoteDialogId=3 MAPDialogState=INITIAL_RECEIVED MAPApplicationContext=MAPApplicationContext [Name=shortMsgGatewayContext, Version=version3, Oid=0, 4, 0, 0, 1, 0, 20, 3, ] TCAPDialogState=InitialReceived]
22:48:14,011 WARN  [HomeRoutingManagement] (SLEE-EventRouterExecutor-3-thread-1) Found no entry in CcMccmncCollection for msisdn: 1234
22:48:14,034 INFO  [HrSriClientSbb] (SLEE-EventRouterExecutor-3-thread-1) 
Home routing: HrSriClientSbb: Sending: SendRoutingInfoForSMRequest: isdn=ISDNAddressString[AddressNature=international_number, NumberingPlan=ISDN, Address=1234], serviceCenterAddress=AddressString[AddressNature=international_number, NumberingPlan=ISDN, Address=22220], sm_RP_PRI=true
22:48:14,228 WARN  [SccpRoutingControl] (pool-27-thread-1) Received SccpMessage for Translation but no matching Rule found for local routing
SccpMessage=Sccp Msg [Type=UDT networkId=50 sls=1 incomingOpc=4 incomingDpc=3 outgoingDpc=-1 CallingAddress(pc=4,ssn=8,AI=83,gt=GlobalTitle0100Impl [digits=1234, natureOfAddress=INTERNATIONAL, numberingPlan=ISDN_TELEPHONY, translationType=1, encodingScheme=BCDEvenEncodingScheme[type=BCD_EVEN, code=2]]) CalledParty(pc=0,ssn=8,AI=18,gt=GlobalTitle0100Impl [digits=22220, natureOfAddress=INTERNATIONAL, numberingPlan=ISDN_TELEPHONY, translationType=0, encodingScheme=BCDOddEncodingScheme[type=BCD_ODD, code=1]]) DataLen=80]
22:48:44,040 ERROR [HrSriClientSbb] (SLEE-EventRouterExecutor-2-thread-1) 
Home routing: Rx :  onInvokeTimeoutInvokeTimeout [invokeId=0, mapDialogWrapper=MAPDialogSmsWrapper [wrappedDialog=MAPDialog: LocalDialogId=2 RemoteDialogId=null MAPDialogState=INITIAL_SENT MAPApplicationContext=MAPApplicationContext [Name=shortMsgGatewayContext, Version=version3, Oid=0, 4, 0, 0, 1, 0, 20, 3, ] TCAPDialogState=InitialSent]]
22:49:13,841 WARN  [HrSriServerSbb] (SLEE-EventRouterExecutor-3-thread-1) 
Home routing: Rx :  onDialogTimeoutDialogTimeout [MAPDialogSmsWrapper [wrappedDialog=MAPDialog: LocalDialogId=1 RemoteDialogId=3 MAPDialogState=INITIAL_RECEIVED MAPApplicationContext=MAPApplicationContext [Name=shortMsgGatewayContext, Version=version3, Oid=0, 4, 0, 0, 1, 0, 20, 3, ] TCAPDialogState=InitialReceived]]
22:49:14,119 WARN  [HrSriClientSbb] (SLEE-EventRouterExecutor-2-thread-1) 
Home routing: Rx :  onDialogTimeoutDialogTimeout [MAPDialogSmsWrapper [wrappedDialog=MAPDialog: LocalDialogId=2 RemoteDialogId=null MAPDialogState=INITIAL_SENT MAPApplicationContext=MAPApplicationContext [Name=shortMsgGatewayContext, Version=version3, Oid=0, 4, 0, 0, 1, 0, 20, 3, ] TCAPDialogState=InitialSent]]
22:49:14,120 ERROR [HrSriServerSbb] (SLEE-EventRouterExecutor-2-thread-1) Home routing: can not get MAPDialog for sending SRI negative Response
