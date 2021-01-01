# gta5vehmoding
<!-- Created by Rak
For more info:
http://www.gtamodding.com/wiki/Handling.meta

> UNITS <
Dimensions in metres
Mass in Kg
Velocity in Km/h
Acceleration/deceleration in ms^2
Multipliers: x1.0 is default
Angles in degrees

> FIELD DESCRIPTIONS <
handlingName					[14 characters max]		This is what links handling to a model through vehicles.meta (see handlingId in vehicles.meta). You can have multiple models use a single set of handling data
fMass
fInitialDragCoeff				[10 to 120]				Sets the drag coefficient on the rage physics archetype of the vehicle (proportional to velocity squared). Increase to simulate aerodynamic drag
fPercentSubmerged				Level submerged before vehicle becomes inoperable
vecCentreOfMassOffset			[minus 10.0 > x > 10.0]
vecInertiaMultiplier			[minus 10.0 > x > 10.0]

TRANSMISSION
fDriveBiasFront					1.0 = front wheel drive, 0.0 = rear wheel drive, 0.5 = 4x4
nInitialDriveGears				Number of gears (excluding reverse)
fInitialDriveForce				Power engine produces in top gear
fDriveInertia					Between 0 and 1. A lower drive inertia slows engine acceleration. If you want a vehicle with high torque but slow acceleration (e.g. a truck) lower the driver inertia but specify a high drive force
fClutchChangeRateScaleUpShift	Clutch speed multiplier on up shifts
fClutchChangeRateScaleDownShift	Clutch speed multiplier on down shifts
fInitialDriveMaxFlatVel			Max velocity in top gear (used when configuring gears)
fBrakeForce						Braking power for normal braking
fBrakeBiasFront					Front / rear brake ratio
fHandBrakeForce					Braking power for handbrake. Increase to lock wheels
fSteeringLock					Max wheel angle (outer wheel) at low speed. gets reduced at high speed, unless you are turning into a skid.

WHEEL TRACTION
fTractionCurveMax				(formerly fTractionMult)
fTractionCurveMin				(formerly fTractionLoss)
fTractionCurveLateral			(shape of lateral traction curve (peak traction position in degrees)
fTractionSpringDeltaMax			(max dist for traction spring)
fLowSpeedTractionLossMult		(how much traction is reduced at low speed, 0.0f means normal traction)
fCamberStiffnesss				used for bikes in vanilla ~ less = more 'skipping'/understeer?
fTractionBiasFront				traction distribution 0.99 = front wheels, 0.01 = rear wheels, 0.5 = equal. Don't use 1 or 0.
fTractionLossMult				(how much is traction affected by material grip differences from 1.0)

SUSPENSION
fSuspensionForce				(1 / (Force * NumWheels) = Lower limit for zero force at full extension
fSuspensionCompDamp				damping during strut compression. > = stiffer
fSuspensionReboundDamp			damping during strut rebound. > = stiffer
fSuspensionUpperLimit			visual limit... how far can wheels move up / down from orig position
fSuspensionLowerLimit			"..."
fSuspensionRaise				adjust from artist positioning
fSuspensionBiasFront			force damping scale front/back. if more wheels at back (e.g. trucks) need front suspension to be stronger
fAntiRollBarForce				the spring constant that is transmitted to the opposite wheel when under compression larger numbers are a larger force
fAntiRollBarBiasFront			the bias between front and rear for the antiroll bar(0 front, 1 rear)
fRollCentreHeightFront
fRollCentreHeightRear

DAMAGE
fCollisionDamageMult
fWeaponDamageMult
fDeformationDamageMult
fEngineDamageMult
fPetrolTankVolume				amount of petrol that will leak after shooting tank
fOilVolume						black smoke time before engine dies

MISC
fSeatOffsetDistX				entering vehicle position. Driver > passenger
fSeatOffsetDistY				"..." Trunk > hood
fSeatOffsetDistZ				"..." Undercarriage > roof
nMonetaryValue					Vehicle worth in $
strModelFlag					(model flags ~ see below)
strHandlingFlags				(handling flags ~ see below)
strDamageFlags					(door damage flags ~ see below)
AIHandling						Defines the AI handling parameters to inform the AI how to drive the car

MODEL FLAGS ~ written in HEX
	1st digit	1: IS_VAN						2: IS_BUS			4: IS_LOW				8: IS_BIG
	2nd digit	1: ABS_STD						2: ABS_OPTION		4: ABS_ALT_STD			8: ABS_ALT_OPTION
	3rd digit	1: NO_DOORS						2: TANDEM_SEATS		4: SIT_IN_BOAT			8: HAS_TRACKS
	4th digit	1: NO_EXHAUST					2: DOUBLE_EXHAUST	4: NO1FPS_LOOK_BEHIND	8: CAN_ENTER_IF_NO_DOOR
	5th digit	1: AXLE_F_TORSION	 			2: AXLE_F_SOLID		4: AXLE_F_MCPHERSON		8: ATTACH_PED_TO_BODYSHELL
	6th digit	1: AXLE_R_TORSION	 			2: AXLE_R_SOLID		4: AXLE_R_MCPHERSON		8: DONT_FORCE_GRND_CLEARANCE
	7th digit	1: DONT_RENDER_STEER 			2: NO_WHEEL_BURST	4: INDESTRUCTIBLE		8: DOUBLE_FRONT_WHEELS
	8th digit	1: RC							2: DOUBLE_RWHEELS	4: MF_NO_WHEEL_BREAK	8: IS_HATCHBACK

HANDLING FLAGS ~ written in HEX
	1st digit	1: SMOOTH_COMPRESN	2: REDUCED_MOD_MASS			4: N/A										8: N/A
	2nd digit	1: NO_HANDBRAKE		2: STEER_REARWHEELS 		4: HB_REARWHEEL_STEER						8: STEER_ALL_WHEELS
	3rd digit	1: FREEWHEEL_NO_GAS	2: NO_REVERSE				4: N/A										8: STEER NO WHEELS
	4th digit	1: CVT				2: ALT_EXT_WHEEL_BOUNDS_BEH	4: DONT_RAISE_BOUNDS_AT_SPEED				8: N/A
	5th digit	1: LESS_SNOW_SINK 	2: TYRES_CAN_CLIP			4: N/A										8: N/A
	6th digit	1: OFFROAD_ABILITY	2: OFFROAD_ABILITY2			4: HF_TYRES_RAISE_SIDE_IMPACT_THRESHOLD		8: N/A
	7th digit	1: ENABLE_LEAN		2: N/A						4: HEAVYARMOUR								8: ARMOURED
	8th digit	1: SELF_RIGHTING_IN_WATER	2: IMPROVED_RIGHTING_FORCE

DOOR DAMAGE FLAGS ~ indicates the doors that are nonbreakable, written in HEX
	1st digit	1: DRIVER_SIDE_FRONT_DOOR	2: DRIVER_SIDE_REAR_DOOR	4: DRIVER_PASSENGER_SIDE_FRONT_DOOR	5: DRIVER_PASSENGER_SIDE_REAR_DOOR
	2st digit	1: BONNET					2: BOOT						4: N/A								5: N/A
	3st digit	1: N/A						2: N/A						4: N/A								5: N/A
	4st digit	1: N/A						2: N/A						4: N/A								5: N/A
	5st digit	1: N/A						2: N/A						4: N/A								5: N/A
	6st digit	1: N/A						2: N/A						4: N/A								5: N/A
	7st digit	1: N/A						2: N/A						4: N/A								5: N/A
	8st digit	1: N/A						2: N/A						4: N/A								5: N/A

SUBHANDLING DATA
	CBoatHandlingData
		For Boats: (some car handling variables are used for alternate functions in boats)
		fRudderOffSetSubmerge	~ Vertical offset of propeller from bone when determining if submerged.
		fRudderOffSetForce		~ Vertical offset of propeller from bone when applying force.
		fLowLodAngOffset		~ The angular offset from vertical that this boat sits at on calm water; used to smooth transition to/from low LOD buoyancy mode.
	CBikeHandlingData
	CFlyingHandlingData
		AIR DYNAMICS
			fSideSlipMult	~	Side rudder force multiplier
			fFormLiftMult	~	Base lift factor that’s independent from wing’s attack angle
			fAttackLiftMult	~	Lift factor of the wing’s attack angle while rising
			fAttackDiveMult	~	Lift factor of the wing’s attack angle while diving
			fWindMult		~	Wind influence factor
		TURBULENCE
			fTurublenceMagnitudeMax		~ Maximum turbulence magnitude of Sinwave motion simulation
			fTurublenceForceMulti		~ Turbulence vertical force multiplier
			fTurublenceRollTorqueMulti	~ Turbulence y axis torque multiplier
			fTurublencePitchTorqueMulti	~ Turbulence x axis torque multiplier
		CONTROL NOISE
			fBodyDamageControlEffectMult		~ Control noise factor contributed from plane damage 
			fInputSensitivityForDifficulty		~ Control noise factor contributed from pilot driving skills
	CVehicleWeaponHandlingData
		uWeaponHash			~	Vehicle Weapon Name. 
			Available Weapons:
				VEHICLE_WEAPON_TANK
				VEHICLE_WEAPON_SPACE_ROCKET
				VEHICLE_WEAPON_PLANE_ROCKET
				VEHICLE_WEAPON_PLAYER_LASER
				VEHICLE_WEAPON_ENEMY_LASER
				VEHICLE_WEAPON_PLAYER_BULLET
				VEHICLE_WEAPON_PLAYER_BUZZARD
				VEHICLE_WEAPON_PLAYER_HUNTER
				VEHICLE_WEAPON_PLAYER_LAZER
				VEHICLE_WEAPON_SEARCHLIGHT
				VEHICLE_WEAPON_WATER_CANNON
				VEHICLE_WEAPON_RADAR
				VEHICLE_WEAPON_DUNE
	CSubmarineHandlingData
	CTrailerHandlingData
		Negative values for rotation limits indicate no constraint	
		fUprightSpringConstant	~	Exactly 0.0 will cause the upright spring to apply no force
		fAttachedMaxDistance	~	Less than or equal to 0.0 will default to the old spherical constraint
			Otherwise: fAttachedMaxDistance		= Attachment distance constraint max distance
				  and: fAttachedMaxPenetration	= Attachment distance constraint max penetration
		fPosConstraintMassRatio	~	indicates that we want the trailer to appear either heavier (val < 1.0) or lighter (val > 1.0) 
			relative to the towing vehicle without actually changing it's real mass
	CCarHandlingData
	CBaseSubHandlingData
		Train handling. Only used by the Metrotrain.
	CSeaPlaneHandlingData
		
		
OTHER
fWeaponDamageScaledToVehHealthMult
-->
