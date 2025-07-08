# Minecraft Network Protocol Docs 7/2/25
For r21_u10, Network Protocol Version 827

## Packet Changes
StartGamePacket
* Added mTickDeathSystemsEnabled (bool) - Used to indicate whether the new tick death systems are enabled.

Camera Instruction:
* Added optional Field of View instruction object to the packet. This is related to changes in the camera_command.
* Still need to Make sure Fov instruction has a proper structure and svg. Also Enum
  * Float - Field of View
  * EasingType Enum (Unsigned Byte) - FOV Ease Type
  * bool - Field of View Clear

CorrectPlayerMovePredictionPacket
* Renamed rotation to vehicle rotation and removed conditional writes of rotation and vehicleAngularVelocity from CorrectPlayerMovePredictionPacket

CameraAimAssistPacket
* Added mShowDebugRender (bool) ["Show Debug Render]


## Enum Changes

ActorDataIDs:
  Added DEPRECATED_CARRY_BLOCK_RUNTIME_ID (23) []
  Removed CARRY_BLOCK_RUNTIME_ID

ActorFlags:
  Added ROTATION_AXIS_ALIGNED (120) []
  Removed BODY_ROTATION_AXIS_ALIGNED

ActorType:
  Added CopperGolem (148 | PathfinderMob) []

Connection::DisconnectFailReason:
  Added INTERNAL_UserLeaveGameAttempted (14) []
  Added TESTONLY_CantConnect (22) []
  Added DEPRECATED_ClientSettingsIncompatibleWithServer (24) []
  Added INTERNAL_NoFailOccurred (30) []
  Added DEPRECATED_NoPremiumPlatform (36) []
  Added DEPRECATED_WorldCorruption (39) []
  Added DEPRECATED_DisconnectPacket (62) []
  Added DEPRECATED_ConnectionLost (66) []
  Added DEPRECATED_ZombieConnection (67) []
  Added DEPRECATED_ReasonNotSet (69) []
  Added DEPRECATED_RealmsSessionNotFound (89) []
  Added INTERNAL_RequestServerShutdown (106) []
  Added DEPRECATED_NoVenue (109) []
  Added NetherNetDataChannelClosed (122) []
  Removed UserLeaveGameAttempted
  Removed CantConnect
  Removed ClientSettingsIncompatibleWithServer
  Removed NoFailOccurred
  Removed NoPremiumPlatform
  Removed WorldCorruption
  Removed DisconnectPacket_DEPRECATED
  Removed ConnectionLost_DEPRECATED
  Removed ZombieConnection
  Removed ReasonNotSet_DEPRECATED
  Removed RealmsSessionNotFound_DEPRECATED
  Removed RequestServerShutdown
  Removed NoVenue

MolangVersion:
  Added CarryingBlockQueryAllActors (13) []
  Displaced NumValidVersions

SharedTypes::Legacy::LevelSoundEvent:
  Added EquipCopper (561) []
  Added RecordLavaChicken (562) []
  Displaced Undefined

# Need to check
ServerAuthMovementMode writeEnum or writeVarEnum not found!
ServerAuthMovementMode declaration not found. Has it been removed?

SimpleEventPacket::Subtype writeEnum or writeVarEnum not found!
SimpleEventPacket::Subtype declaration not found. Has it been removed?


SetTitlePacket::TitleType writeEnum or writeVarEnum not found!
SetTitlePacket::TitleType declaration not found. Has it been removed?