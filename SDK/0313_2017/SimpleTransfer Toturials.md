## Mr.LOOP SDK SimpleTransfer Guide ##
/* 
 * This toturial describes how to drive our device with our SDK.
 *
 * There are three states with hardware-driven: 
 * 1. Enable devices.
 * 2. Devices work.
 * 3. Disable devices.
 *
 * 
 * We would implement each state in main function of SampleTransfer.cpp sequentially:
 *
 * #Enable devices.
 * 1. Call ML_HiddenDebugMsg() to check if our library included and then disable error message output.
 * 2. Call ML_Init() to enable and open our device.
 * 3. Call ML_SetSpeed(int) to set up RF Speed threshold. Default value is 2.
 * 4. Call ML_SetMode(int) to recognize this peer is 1 (tx) or 2 (rx).
 *
 * #Devices work.
 * 5. Developers always need to allocate enough buffers to be copied whatever the peer is Tx or Rx.
 * 6. CheckPktTx/CheckPktRx used to examine RF signals if packets received exactly.
 *
 * #Disable devices
 * 7. Call ML_Close() to close devices before applications quit.
 *
 */
