if game:GetService("RunService"):IsClient() then error("Script must be server-side in order to work; use h/ and not hl/") end
local Player,Mouse,mouse,UserInputService,ContextActionService = owner
do
	print("FE Compatibility code by Mokiros")
	script.Parent = Player.Character

	--RemoteEvent for communicating
	local Event = Instance.new("RemoteEvent")
	Event.Name = "UserInput_Event"

	--Fake event to make stuff like Mouse.KeyDown work
	local function fakeEvent()
		local t = {_fakeEvent=true,Connect=function(self,f)self.Function=f end}
		t.connect = t.Connect
		return t
	end

	--Creating fake input objects with fake variables
    local m = {Target=nil,Hit=CFrame.new(),KeyUp=fakeEvent(),KeyDown=fakeEvent(),Button1Up=fakeEvent(),Button1Down=fakeEvent()}
	local UIS = {InputBegan=fakeEvent(),InputEnded=fakeEvent()}
	local CAS = {Actions={},BindAction=function(self,name,fun,touch,...)
		CAS.Actions[name] = fun and {Name=name,Function=fun,Keys={...}} or nil
	end}
	--Merged 2 functions into one by checking amount of arguments
	CAS.UnbindAction = CAS.BindAction

	--This function will trigger the events that have been :Connect()'ed
	local function te(self,ev,...)
		local t = m[ev]
		if t and t._fakeEvent and t.Function then
			t.Function(...)
		end
	end
	m.TrigEvent = te
	UIS.TrigEvent = te

	Event.OnServerEvent:Connect(function(plr,io)
	    if plr~=Player then return end
		if io.isMouse then
			m.Target = io.Target
			m.Hit = io.Hit
		else
			local b = io.UserInputState == Enum.UserInputState.Begin
			if io.UserInputType == Enum.UserInputType.MouseButton1 then
				return m:TrigEvent(b and "Button1Down" or "Button1Up")
			end
			for _,t in pairs(CAS.Actions) do
				for _,k in pairs(t.Keys) do
					if k==io.KeyCode then
						t.Function(t.Name,io.UserInputState,io)
					end
				end
			end
			m:TrigEvent(b and "KeyDown" or "KeyUp",io.KeyCode.Name:lower())
			UIS:TrigEvent(b and "InputBegan" or "InputEnded",io,false)
	    end
	end)
	Event.Parent = NLS([==[
	local Player = game:GetService("Players").LocalPlayer
	local Event = script:WaitForChild("UserInput_Event")

	local UIS = game:GetService("UserInputService")
	local input = function(io,a)
		if a then return end
		--Since InputObject is a client-side instance, we create and pass table instead
		Event:FireServer({KeyCode=io.KeyCode,UserInputType=io.UserInputType,UserInputState=io.UserInputState})
	end
	UIS.InputBegan:Connect(input)
	UIS.InputEnded:Connect(input)

	local Mouse = Player:GetMouse()
	local h,t
	--Give the server mouse data 30 times every second, but only if the values changed
	--If player is not moving their mouse, client won't fire events
	while wait(1/30) do
		if h~=Mouse.Hit or t~=Mouse.Target then
			h,t=Mouse.Hit,Mouse.Target
			Event:FireServer({isMouse=true,Target=t,Hit=h})
		end
	end]==],Player.Character)
	Mouse,mouse,UserInputService,ContextActionService = m,m,UIS,CAS
end
-----------------------
--[[ Name : Inked Monster ]]--
-------------------------------------------------------
--A script By makhail07

--Discord Creterisk#2958 

--NOTE THIS SCRIPT WAS PURELY MADE FROM MY FUCKING IMAGINATION
--IF IT HAPPENS TO LOOK LIKE ANOTHER SCRIPT
--DONT CALL IT A FUCKING BOOTLEG THANK YOU AND ENJOY THE SCRIPT
--YOU FUCKING SKIDS,
--For Those who log/decompile this, If you sell or trade this,
--and I find out who you are, i will take massive action.

-------------------------------------------------------

local FavIDs = {
	340106355, --Nefl Crystals
	927529620, --Dimension
	876981900, --Fantasy
	398987889, --Ordinary Days
	1117396305, --Oh wait, it's you.
	885996042, --Action Winter Journey
	919231299, --Sprawling Idiot Effigy
	743466274, --Good Day Sunshine
	727411183, --Knife Fight
	1402748531, --The Earth Is Counting On You!
	595230126 --Robot Language
	}



--The reality of my life isn't real but a Universe -makhail07
wait(0.2)
local plr = owner
print('Local User is '..plr.Name)
print('Inked Monster Loaded')
print('Wat')
local char = plr.Character
local hum = char.Humanoid
local hed = char.Head
local root = char.HumanoidRootPart
local rootj = root.RootJoint
local tors = char.Torso
local ra = char["Right Arm"]
local la = char["Left Arm"]
local rl = char["Right Leg"]
local ll = char["Left Leg"]
local neck = tors["Neck"]
local RootCF = CFrame.fromEulerAnglesXYZ(-1.57, 0, 3.14)
local RHCF = CFrame.fromEulerAnglesXYZ(0, 1.6, 0)
local LHCF = CFrame.fromEulerAnglesXYZ(0, -1.6, 0)
local maincolor = BrickColor.new("Institutional white")
-------------------------------------------------------
--Start Whitelist and Invincibility--
-------------------------------------------------------	
ff = Instance.new("ForceField",char)
ff.Visible = false
hum.Name = "Base"
hum.MaxHealth = 1.0E298
hum.Health = 1.0E298
game:GetService("RunService"):BindToRenderStep("Bbae", 0, function()
  if hum.Health > 0.1 and hum.Health < 1.0E298 then
    hum.MaxHealth = 1.0E298
    hum.Health = 1.0E298
  end
end)
-------------------------------------------------------
--End Whitelist and Invincibility--
-------------------------------------------------------	

-------------------------------------------------------
--Start Good Stuff--
-------------------------------------------------------
cam = game.Workspace.CurrentCamera
CF = CFrame.new
angles = CFrame.Angles
attack = false
Euler = CFrame.fromEulerAnglesXYZ
Rad = math.rad
IT = Instance.new
BrickC = BrickColor.new
Cos = math.cos
Acos = math.acos
Sin = math.sin
Asin = math.asin
Abs = math.abs
Mrandom = math.random
Floor = math.floor
-------------------------------------------------------
--End Good Stuff--
-------------------------------------------------------
necko = CF(0, 1, 0, -1, -0, -0, 0, 0, 1, 0, 1, 0)
RSH, LSH = nil, nil 
RW = Instance.new("Weld") 
LW = Instance.new("Weld")
RH = tors["Right Hip"]
LH = tors["Left Hip"]
RSH = tors["Right Shoulder"] 
LSH = tors["Left Shoulder"] 
RSH.Parent = nil 
LSH.Parent = nil 
RW.Name = "RW"
RW.Part0 = tors 
RW.C0 = CF(1.5, 0.5, 0)
RW.C1 = CF(0, 0.5, 0) 
RW.Part1 = ra
RW.Parent = tors 
LW.Name = "LW"
LW.Part0 = tors 
LW.C0 = CF(-1.5, 0.5, 0)
LW.C1 = CF(0, 0.5, 0) 
LW.Part1 = la
LW.Parent = tors
Effects = {}
-------------------------------------------------------
--Start HeartBeat--
-------------------------------------------------------
ArtificialHB = Instance.new("BindableEvent", script)
ArtificialHB.Name = "Heartbeat"
script:WaitForChild("Heartbeat")

frame = 1 / 60
tf = 0
allowframeloss = false
tossremainder = false


lastframe = tick()
script.Heartbeat:Fire()


game:GetService("RunService").Heartbeat:connect(function(s, p)
	tf = tf + s
	if tf >= frame then
		if allowframeloss then
			script.Heartbeat:Fire()
			lastframe = tick()
		else
			for i = 1, math.floor(tf / frame) do
				script.Heartbeat:Fire()
			end
			lastframe = tick()
		end
		if tossremainder then
			tf = 0
		else
			tf = tf - frame * math.floor(tf / frame)
		end
	end
end)
-------------------------------------------------------
--End HeartBeat--
-------------------------------------------------------

-------------------------------------------------------
--Start Important Functions--
-------------------------------------------------------
function swait(num)
	if num == 0 or num == nil then
		game:service("RunService").Stepped:wait(0)
	else
		for i = 0, num do
			game:service("RunService").Stepped:wait(0)
		end
	end
end
function thread(f)
	coroutine.resume(coroutine.create(f))
end
function clerp(a, b, t)
	local qa = {
		QuaternionFromCFrame(a)
	}
	local qb = {
		QuaternionFromCFrame(b)
	}
	local ax, ay, az = a.x, a.y, a.z
	local bx, by, bz = b.x, b.y, b.z
	local _t = 1 - t
	return QuaternionToCFrame(_t * ax + t * bx, _t * ay + t * by, _t * az + t * bz, QuaternionSlerp(qa, qb, t))
end
function QuaternionFromCFrame(cf)
	local mx, my, mz, m00, m01, m02, m10, m11, m12, m20, m21, m22 = cf:components()
	local trace = m00 + m11 + m22
	if trace > 0 then
		local s = math.sqrt(1 + trace)
		local recip = 0.5 / s
		return (m21 - m12) * recip, (m02 - m20) * recip, (m10 - m01) * recip, s * 0.5
	else
		local i = 0
		if m00 < m11 then
			i = 1
		end
		if m22 > (i == 0 and m00 or m11) then
			i = 2
		end
		if i == 0 then
			local s = math.sqrt(m00 - m11 - m22 + 1)
			local recip = 0.5 / s
			return 0.5 * s, (m10 + m01) * recip, (m20 + m02) * recip, (m21 - m12) * recip
		elseif i == 1 then
			local s = math.sqrt(m11 - m22 - m00 + 1)
			local recip = 0.5 / s
			return (m01 + m10) * recip, 0.5 * s, (m21 + m12) * recip, (m02 - m20) * recip
		elseif i == 2 then
			local s = math.sqrt(m22 - m00 - m11 + 1)
			local recip = 0.5 / s
			return (m02 + m20) * recip, (m12 + m21) * recip, 0.5 * s, (m10 - m01) * recip
		end
	end
end
function QuaternionToCFrame(px, py, pz, x, y, z, w)
	local xs, ys, zs = x + x, y + y, z + z
	local wx, wy, wz = w * xs, w * ys, w * zs
	local xx = x * xs
	local xy = x * ys
	local xz = x * zs
	local yy = y * ys
	local yz = y * zs
	local zz = z * zs
	return CFrame.new(px, py, pz, 1 - (yy + zz), xy - wz, xz + wy, xy + wz, 1 - (xx + zz), yz - wx, xz - wy, yz + wx, 1 - (xx + yy))
end
function QuaternionSlerp(a, b, t)
	local cosTheta = a[1] * b[1] + a[2] * b[2] + a[3] * b[3] + a[4] * b[4]
	local startInterp, finishInterp
	if cosTheta >= 1.0E-4 then
		if 1 - cosTheta > 1.0E-4 then
			local theta = math.acos(cosTheta)
			local invSinTheta = 1 / Sin(theta)
			startInterp = Sin((1 - t) * theta) * invSinTheta
			finishInterp = Sin(t * theta) * invSinTheta
		else
			startInterp = 1 - t
			finishInterp = t
		end
	elseif 1 + cosTheta > 1.0E-4 then
		local theta = math.acos(-cosTheta)
		local invSinTheta = 1 / Sin(theta)
		startInterp = Sin((t - 1) * theta) * invSinTheta
		finishInterp = Sin(t * theta) * invSinTheta
	else
		startInterp = t - 1
		finishInterp = t
	end
	return a[1] * startInterp + b[1] * finishInterp, a[2] * startInterp + b[2] * finishInterp, a[3] * startInterp + b[3] * finishInterp, a[4] * startInterp + b[4] * finishInterp
end
function rayCast(Position, Direction, Range, Ignore)
	return game:service("Workspace"):FindPartOnRay(Ray.new(Position, Direction.unit * (Range or 999.999)), Ignore)
end
local RbxUtility = LoadLibrary("RbxUtility")
local Create = RbxUtility.Create

-------------------------------------------------------
--Start Damage Function--
-------------------------------------------------------
function Damage(Part, hit, minim, maxim, knockback, Type, Property, Delay, HitSound, HitPitch)
	if hit.Parent == nil then
		return
	end
	local h = hit.Parent:FindFirstChildOfClass("Humanoid")
	for _, v in pairs(hit.Parent:children()) do
		if v:IsA("Humanoid") then
			h = v
		end
	end
         if h ~= nil and hit.Parent.Name ~= char.Name and hit.Parent:FindFirstChild("UpperTorso") ~= nil then
	
         hit.Parent:FindFirstChild("Head"):BreakJoints()
         end

	if h ~= nil and hit.Parent.Name ~= char.Name and hit.Parent:FindFirstChild("Torso") ~= nil then
		if hit.Parent:findFirstChild("DebounceHit") ~= nil then
			if hit.Parent.DebounceHit.Value == true then
				return
			end
		end
         if insta == true then
         hit.Parent:FindFirstChild("Head"):BreakJoints()
         end
		local c = Create("ObjectValue"){
			Name = "creator",
			Value = game:service("Players").LocalPlayer,
			Parent = h,
		}
		game:GetService("Debris"):AddItem(c, .5)
		if HitSound ~= nil and HitPitch ~= nil then
			CFuncs.Sound.Create(HitSound, hit, 1, HitPitch) 
		end
		local Damage = math.random(minim, maxim)
		local blocked = false
		local block = hit.Parent:findFirstChild("Block")
		if block ~= nil then
			if block.className == "IntValue" then
				if block.Value > 0 then
					blocked = true
					block.Value = block.Value - 1
					print(block.Value)
				end
			end
		end
		if blocked == false then
			h.Health = h.Health - Damage
			ShowDamage((Part.CFrame * CFrame.new(0, 0, (Part.Size.Z / 2)).p + Vector3.new(0, 1.5, 0)), -Damage, 1.5, tors.BrickColor.Color)
		else
			h.Health = h.Health - (Damage / 2)
			ShowDamage((Part.CFrame * CFrame.new(0, 0, (Part.Size.Z / 2)).p + Vector3.new(0, 1.5, 0)), -Damage, 1.5, tors.BrickColor.Color)
		end
		if Type == "Knockdown" then
			local hum = hit.Parent.Humanoid
			hum.PlatformStand = true
			coroutine.resume(coroutine.create(function(HHumanoid)
				swait(1)
				HHumanoid.PlatformStand = false
			end), hum)
			local angle = (hit.Position - (Property.Position + Vector3.new(0, 0, 0))).unit
			local bodvol = Create("BodyVelocity"){
				velocity = angle * knockback,
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			local rl = Create("BodyAngularVelocity"){
				P = 3000,
				maxTorque = Vector3.new(500000, 500000, 500000) * 50000000000000,
				angularvelocity = Vector3.new(math.random(-10, 10), math.random(-10, 10), math.random(-10, 10)),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodvol, .5)
			game:GetService("Debris"):AddItem(rl, .5)
		elseif Type == "Normal" then
			local vp = Create("BodyVelocity"){
				P = 500,
				maxForce = Vector3.new(math.huge, 0, math.huge),
				velocity = Property.CFrame.lookVector * knockback + Property.Velocity / 1.05,
			}
			if knockback > 0 then
				vp.Parent = hit.Parent.Torso
			end
			game:GetService("Debris"):AddItem(vp, .5)
		elseif Type == "Up" then
			local bodyVelocity = Create("BodyVelocity"){
				velocity = Vector3.new(0, 20, 0),
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodyVelocity, .5)
		elseif Type == "DarkUp" then
			coroutine.resume(coroutine.create(function()
				for i = 0, 1, 0.1 do
					swait()
					Effects.Block.Create(BrickColor.new("Black"), hit.Parent.Torso.CFrame, 5, 5, 5, 1, 1, 1, .08, 1)
				end
			end))
			local bodyVelocity = Create("BodyVelocity"){
				velocity = Vector3.new(0, 20, 0),
				P = 5000,
				maxForce = Vector3.new(8e+003, 8e+003, 8e+003),
				Parent = hit,
			}
			game:GetService("Debris"):AddItem(bodyVelocity, 1)
		elseif Type == "Snare" then
			local bp = Create("BodyPosition"){
				P = 2000,
				D = 100,
				maxForce = Vector3.new(math.huge, math.huge, math.huge),
				position = hit.Parent.Torso.Position,
				Parent = hit.Parent.Torso,
			}
			game:GetService("Debris"):AddItem(bp, 1)
		elseif Type == "Freeze" then
			local BodPos = Create("BodyPosition"){
				P = 50000,
				D = 1000,
				maxForce = Vector3.new(math.huge, math.huge, math.huge),
				position = hit.Parent.Torso.Position,
				Parent = hit.Parent.Torso,
			}
			local BodGy = Create("BodyGyro") {
				maxTorque = Vector3.new(4e+005, 4e+005, 4e+005) * math.huge ,
				P = 20e+003,
				Parent = hit.Parent.Torso,
				cframe = hit.Parent.Torso.CFrame,
			}
			hit.Parent.Torso.Anchored = true
			coroutine.resume(coroutine.create(function(Part) 
				swait(1.5)
				Part.Anchored = false
			end), hit.Parent.Torso)
			game:GetService("Debris"):AddItem(BodPos, 3)
			game:GetService("Debris"):AddItem(BodGy, 3)
		end
		local debounce = Create("BoolValue"){
			Name = "DebounceHit",
			Parent = hit.Parent,
			Value = true,
		}
		game:GetService("Debris"):AddItem(debounce, Delay)
		c = Create("ObjectValue"){
			Name = "creator",
			Value = Player,
			Parent = h,
		}
		game:GetService("Debris"):AddItem(c, .5)
	end
end
-------------------------------------------------------
--End Damage Function--
-------------------------------------------------------

-------------------------------------------------------
--Start Damage Function Customization--
-------------------------------------------------------
function ShowDamage(Pos, Text, Time, Color)
	local Rate = (1 / 30)
	local Pos = (Pos or Vector3.new(0, 0, 0))
	local Text = (Text or "")
	local Time = (Time or 2)
	local Color = (Color or Color3.new(1, 0, 1))
	local EffectPart = CFuncs.Part.Create(workspace, "SmoothPlastic", 0, 1, BrickColor.new(Color), "Effect", Vector3.new(0, 0, 0))
	EffectPart.Anchored = true
	local BillboardGui = Create("BillboardGui"){
		Size = UDim2.new(3, 0, 3, 0),
		Adornee = EffectPart,
		Parent = EffectPart,
	}
	local TextLabel = Create("TextLabel"){
		BackgroundTransparency = 1,
		Size = UDim2.new(1, 0, 1, 0),
		Text = Text,
		Font = "Bodoni",
		TextColor3 = Color,
		TextScaled = true,
		TextStrokeColor3 = Color3.fromRGB(0,0,0),
		Parent = BillboardGui,
	}
	game.Debris:AddItem(EffectPart, (Time))
	EffectPart.Parent = game:GetService("Workspace")
	delay(0, function()
		local Frames = (Time / Rate)
		for Frame = 1, Frames do
			wait(Rate)
			local Percent = (Frame / Frames)
			EffectPart.CFrame = CFrame.new(Pos) + Vector3.new(0, Percent, 0)
			TextLabel.TextTransparency = Percent
		end
		if EffectPart and EffectPart.Parent then
			EffectPart:Destroy()
		end
	end)
end
-------------------------------------------------------
--End Damage Function Customization--
-------------------------------------------------------

function MagniDamage(Part, magni, mindam, maxdam, knock, Type)
  for _, c in pairs(workspace:children()) do
    local hum = c:findFirstChild("Humanoid")
    if hum ~= nil then
      local head = c:findFirstChild("Head")
      if head ~= nil then
        local targ = head.Position - Part.Position
        local mag = targ.magnitude
        if magni >= mag and c.Name ~= plr.Name then
          Damage(head, head, mindam, maxdam, knock, Type, root, 0.1, "http://www.roblox.com/asset/?id=0", 1.2)
        end
      end
    end
  end
end


CFuncs = {
	Part = {
		Create = function(Parent, Material, Reflectance, Transparency, BColor, Name, Size)
			local Part = Create("Part")({
				Parent = Parent,
				Reflectance = Reflectance,
				Transparency = Transparency,
				CanCollide = false,
				Locked = true,
				BrickColor = BrickColor.new(tostring(BColor)),
				Name = Name,
				Size = Size,
				Material = Material
			})
			RemoveOutlines(Part)
			return Part
		end
	},
	Mesh = {
		Create = function(Mesh, Part, MeshType, MeshId, OffSet, Scale)
			local Msh = Create(Mesh)({
				Parent = Part,
				Offset = OffSet,
				Scale = Scale
			})
			if Mesh == "SpecialMesh" then
				Msh.MeshType = MeshType
				Msh.MeshId = MeshId
			end
			return Msh
		end
	},
	Mesh = {
		Create = function(Mesh, Part, MeshType, MeshId, OffSet, Scale)
			local Msh = Create(Mesh)({
				Parent = Part,
				Offset = OffSet,
				Scale = Scale
			})
			if Mesh == "SpecialMesh" then
				Msh.MeshType = MeshType
				Msh.MeshId = MeshId
			end
			return Msh
		end
	},
	Weld = {
		Create = function(Parent, Part0, Part1, C0, C1)
			local Weld = Create("Weld")({
				Parent = Parent,
				Part0 = Part0,
				Part1 = Part1,
				C0 = C0,
				C1 = C1
			})
			return Weld
		end
	},
	Sound = {
		Create = function(id, par, vol, pit)
			coroutine.resume(coroutine.create(function()
				local S = Create("Sound")({
					Volume = vol,
					Pitch = pit or 1,
					SoundId = id,
					Parent = par or workspace
				})
				wait()
				S:play()
				game:GetService("Debris"):AddItem(S, 6)
			end))
		end
	},
	ParticleEmitter = {
		Create = function(Parent, Color1, Color2, LightEmission, Size, Texture, Transparency, ZOffset, Accel, Drag, LockedToPart, VelocityInheritance, EmissionDirection, Enabled, LifeTime, Rate, Rotation, RotSpeed, Speed, VelocitySpread)
			local fp = Create("ParticleEmitter")({
				Parent = Parent,
				Color = ColorSequence.new(Color1, Color2),
				LightEmission = LightEmission,
				Size = Size,
				Texture = Texture,
				Transparency = Transparency,
				ZOffset = ZOffset,
				Acceleration = Accel,
				Drag = Drag,
				LockedToPart = LockedToPart,
				VelocityInheritance = VelocityInheritance,
				EmissionDirection = EmissionDirection,
				Enabled = Enabled,
				Lifetime = LifeTime,
				Rate = Rate,
				Rotation = Rotation,
				RotSpeed = RotSpeed,
				Speed = Speed,
				VelocitySpread = VelocitySpread
			})
			return fp
		end
	}
}
function RemoveOutlines(part)
	part.TopSurface, part.BottomSurface, part.LeftSurface, part.RightSurface, part.FrontSurface, part.BackSurface = 10, 10, 10, 10, 10, 10
end
function CreatePart1(FormFactor, Parent, Material, Reflectance, Transparency, BColor, Name, Size)
	local Part = Create("Part")({
		formFactor = FormFactor,
		Parent = Parent,
		Reflectance = Reflectance,
		Transparency = Transparency,
		CanCollide = false,
		Locked = true,
		BrickColor = BrickColor.new(tostring(BColor)),
		Name = Name,
		Size = Size,
		Material = Material
	})
	RemoveOutlines(Part)
	return Part
end
function CreatePart(FORMFACTOR, PARENT, MATERIAL, REFLECTANCE, TRANSPARENCY, BRICKCOLOR, NAME, SIZE, ANCHOR)
	local NEWPART = IT("Part")
	NEWPART.formFactor = FORMFACTOR
	NEWPART.Reflectance = REFLECTANCE
	NEWPART.Transparency = TRANSPARENCY
	NEWPART.CanCollide = false
	NEWPART.Locked = true
	NEWPART.Anchored = true
	if ANCHOR == false then
		NEWPART.Anchored = false
	end
	NEWPART.BrickColor = BrickC(tostring(BRICKCOLOR))
	NEWPART.Name = NAME
	NEWPART.Size = SIZE
	NEWPART.Position = tors.Position
	NEWPART.Material = MATERIAL
	NEWPART:BreakJoints()
	NEWPART.Parent = PARENT
	return NEWPART
end
function CreateMesh(Mesh, Part, MeshType, MeshId, OffSet, Scale)
	local Msh = Create(Mesh)({
		Parent = Part,
		Offset = OffSet,
		Scale = Scale
	})
	if Mesh == "SpecialMesh" then
		Msh.MeshType = MeshType
		Msh.MeshId = MeshId
	end
	return Msh
end
function CreateWeld(Parent, Part0, Part1, C0, C1)
	local Weld = Create("Weld")({
		Parent = Parent,
		Part0 = Part0,
		Part1 = Part1,
		C0 = C0,
		C1 = C1
	})
	return Weld
end


-------------------------------------------------------
--Start Effect Function--
-------------------------------------------------------
EffectModel = Instance.new("Model", char)
Effects = {
  Block = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay, Type)
      local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("BlockMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      if Type == 1 or Type == nil then
        table.insert(Effects, {
          prt,
          "Block1",
          delay,
          x3,
          y3,
          z3,
          msh
        })
      elseif Type == 2 then
        table.insert(Effects, {
          prt,
          "Block2",
          delay,
          x3,
          y3,
          z3,
          msh
        })
      else
        table.insert(Effects, {
          prt,
          "Block3",
          delay,
          x3,
          y3,
          z3,
          msh
        })
      end
    end
  },
  Sphere = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "Sphere", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3,
        y3,
        z3,
        msh
      })
    end
  },
  Cylinder = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("CylinderMesh", prt, "", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3,
        y3,
        z3,
        msh
      })
    end
  },
  Wave = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://20329976", Vector3.new(0, 0, 0), Vector3.new(x1 / 60, y1 / 60, z1 / 60))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3 / 60,
        y3 / 60,
        z3 / 60,
        msh
      })
    end
  },
  Ring = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://3270017", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3,
        y3,
        z3,
        msh
      })
    end
  },
  Break = {
    Create = function(brickcolor, cframe, x1, y1, z1)
      local prt = CFuncs.Part.Create(EffectModel, "Neon", 0, 0, brickcolor, "Effect", Vector3.new(0.5, 0.5, 0.5))
      prt.Anchored = true
      prt.CFrame = cframe * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "Sphere", "", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      local num = math.random(10, 50) / 1000
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Shatter",
        num,
        prt.CFrame,
        math.random() - math.random(),
        0,
        math.random(50, 100) / 100
      })
    end
  },
Spiral = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://1051557", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3,
        y3,
        z3,
        msh
      })
    end
  },
Push = {
    Create = function(brickcolor, cframe, x1, y1, z1, x3, y3, z3, delay)
      local prt = CFuncs.Part.Create(EffectModel, "SmoothPlastic", 0, 0, brickcolor, "Effect", Vector3.new())
      prt.Anchored = true
      prt.CFrame = cframe
      local msh = CFuncs.Mesh.Create("SpecialMesh", prt, "FileMesh", "rbxassetid://437347603", Vector3.new(0, 0, 0), Vector3.new(x1, y1, z1))
      game:GetService("Debris"):AddItem(prt, 10)
      table.insert(Effects, {
        prt,
        "Cylinder",
        delay,
        x3,
        y3,
        z3,
        msh
      })
    end
  }
}
function part(formfactor ,parent, reflectance, transparency, brickcolor, name, size)
	local fp = IT("Part")
	fp.formFactor = formfactor 
	fp.Parent = parent
	fp.Reflectance = reflectance
	fp.Transparency = transparency
	fp.CanCollide = false 
	fp.Locked = true
	fp.BrickColor = brickcolor
	fp.Name = name
	fp.Size = size
	fp.Position = tors.Position 
	RemoveOutlines(fp)
	fp.Material = "SmoothPlastic"
	fp:BreakJoints()
	return fp 
end 
 
function mesh(Mesh,part,meshtype,meshid,offset,scale)
	local mesh = IT(Mesh) 
	mesh.Parent = part
	if Mesh == "SpecialMesh" then
		mesh.MeshType = meshtype
	if meshid ~= "nil" then
		mesh.MeshId = "http://www.roblox.com/asset/?id="..meshid
		end
	end
	mesh.Offset = offset
	mesh.Scale = scale
	return mesh
end

function Magic(bonuspeed, type, pos, scale, value, color, MType)
	local type = type
	local rng = Instance.new("Part", char)
	rng.Anchored = true
	rng.BrickColor = color
	rng.CanCollide = false
	rng.FormFactor = 3
	rng.Name = "Ring"
	rng.Material = "Neon"
	rng.Size = Vector3.new(1, 1, 1)
	rng.Transparency = 0
	rng.TopSurface = 0
	rng.BottomSurface = 0
	rng.CFrame = pos
	local rngm = Instance.new("SpecialMesh", rng)
	rngm.MeshType = MType
	rngm.Scale = scale
	local scaler2 = 1
	if type == "Add" then
		scaler2 = 1 * value
	elseif type == "Divide" then
		scaler2 = 1 / value
	end
	coroutine.resume(coroutine.create(function()
		for i = 0, 10 / bonuspeed, 0.1 do
			swait()
			if type == "Add" then
				scaler2 = scaler2 - 0.01 * value / bonuspeed
			elseif type == "Divide" then
				scaler2 = scaler2 - 0.01 / value * bonuspeed
			end
			rng.Transparency = rng.Transparency + 0.01 * bonuspeed
			rngm.Scale = rngm.Scale + Vector3.new(scaler2 * bonuspeed, scaler2 * bonuspeed, scaler2 * bonuspeed)
		end
		rng:Destroy()
	end))
end

function Eviscerate(dude)
	if dude.Name ~= char then
		local bgf = IT("BodyGyro", dude.Head)
		bgf.CFrame = bgf.CFrame * CFrame.fromEulerAnglesXYZ(Rad(-90), 0, 0)
		local val = IT("BoolValue", dude)
		val.Name = "IsHit"
		local ds = coroutine.wrap(function()
			dude:WaitForChild("Head"):BreakJoints()
			wait(0.5)
			target = nil
			coroutine.resume(coroutine.create(function()
				for i, v in pairs(dude:GetChildren()) do
					if v:IsA("Accessory") then
						v:Destroy()
					end
					if v:IsA("Humanoid") then
						v:Destroy()
					end
					if v:IsA("CharacterMesh") then
						v:Destroy()
					end
					if v:IsA("Model") then
						v:Destroy()
					end
					if v:IsA("Part") or v:IsA("MeshPart") then
						for x, o in pairs(v:GetChildren()) do
							if o:IsA("Decal") then
								o:Destroy()
							end
						end
						coroutine.resume(coroutine.create(function()
							v.Material = "Neon"
							v.CanCollide = false
							local PartEmmit1 = IT("ParticleEmitter", v)
							PartEmmit1.LightEmission = 1
							PartEmmit1.Texture = "rbxassetid://284205403"
							PartEmmit1.Color = ColorSequence.new(maincolor.Color)
							PartEmmit1.Rate = 150
							PartEmmit1.Lifetime = NumberRange.new(1)
							PartEmmit1.Size = NumberSequence.new({
								NumberSequenceKeypoint.new(0, 0.75, 0),
								NumberSequenceKeypoint.new(1, 0, 0)
							})
							PartEmmit1.Transparency = NumberSequence.new({
								NumberSequenceKeypoint.new(0, 0, 0),
								NumberSequenceKeypoint.new(1, 1, 0)
							})
							PartEmmit1.Speed = NumberRange.new(0, 0)
							PartEmmit1.VelocitySpread = 30000
							PartEmmit1.Rotation = NumberRange.new(-500, 500)
							PartEmmit1.RotSpeed = NumberRange.new(-500, 500)
							local BodPoss = IT("BodyPosition", v)
							BodPoss.P = 3000
							BodPoss.D = 1000
							BodPoss.maxForce = Vector3.new(50000000000, 50000000000, 50000000000)
							BodPoss.position = v.Position + Vector3.new(Mrandom(-15, 15), Mrandom(-15, 15), Mrandom(-15, 15))
							v.Color = maincolor.Color
							coroutine.resume(coroutine.create(function()
								for i = 0, 49 do
									swait(1)
									v.Transparency = v.Transparency + 0.08
								end
								wait(0.5)
								PartEmmit1.Enabled = false
								wait(3)
								v:Destroy()
								dude:Destroy()
							end))
						end))
					end
				end
			end))
		end)
		ds()
	end
end

function FindNearestHead(Position, Distance, SinglePlayer)
	if SinglePlayer then
		return Distance > (SinglePlayer.Torso.CFrame.p - Position).magnitude
	end
	local List = {}
	for i, v in pairs(workspace:GetChildren()) do
		if v:IsA("Model") and v:findFirstChild("Head") and v ~= char and Distance >= (v.Head.Position - Position).magnitude then
			table.insert(List, v)
		end
	end
	return List
end

function Aura(bonuspeed, FastSpeed, type, pos, x1, y1, z1, value, color, outerpos, MType)
	local type = type
	local rng = Instance.new("Part", char)
	rng.Anchored = true
	rng.BrickColor = color
	rng.CanCollide = false
	rng.FormFactor = 3
	rng.Name = "Ring"
	rng.Material = "Neon"
	rng.Size = Vector3.new(1, 1, 1)
	rng.Transparency = 0
	rng.TopSurface = 0
	rng.BottomSurface = 0
	rng.CFrame = pos
	rng.CFrame = rng.CFrame + rng.CFrame.lookVector * outerpos
	local rngm = Instance.new("SpecialMesh", rng)
	rngm.MeshType = MType
	rngm.Scale = Vector3.new(x1, y1, z1)
	local scaler2 = 1
	local speeder = FastSpeed
	if type == "Add" then
		scaler2 = 1 * value
	elseif type == "Divide" then
		scaler2 = 1 / value
	end
	coroutine.resume(coroutine.create(function()
		for i = 0, 10 / bonuspeed, 0.1 do
			swait()
			if type == "Add" then
				scaler2 = scaler2 - 0.01 * value / bonuspeed
			elseif type == "Divide" then
				scaler2 = scaler2 - 0.01 / value * bonuspeed
			end
			speeder = speeder - 0.01 * FastSpeed * bonuspeed
			rng.CFrame = rng.CFrame + rng.CFrame.lookVector * speeder * bonuspeed
			rng.Transparency = rng.Transparency + 0.01 * bonuspeed
			rngm.Scale = rngm.Scale + Vector3.new(scaler2 * bonuspeed, scaler2 * bonuspeed, 0)
		end
		rng:Destroy()
	end))
end

function SoulSteal(dude)
if dude.Name ~= char then
local bgf = IT("BodyGyro", dude.Head)
bgf.CFrame = bgf.CFrame * CFrame.fromEulerAnglesXYZ(Rad(-90), 0, 0)
local val = IT("BoolValue", dude)
val.Name = "IsHit"
local torso = (dude:FindFirstChild'Head' or dude:FindFirstChild'Torso' or dude:FindFirstChild'UpperTorso' or dude:FindFirstChild'LowerTorso' or dude:FindFirstChild'HumanoidRootPart')
local soulst = coroutine.wrap(function()
local soul = Instance.new("Part",dude)
soul.Size = Vector3.new(1,1,1)
soul.CanCollide = false
soul.Anchored = false
soul.Position = torso.Position
soul.Transparency = 1
local PartEmmit1 = IT("ParticleEmitter", soul)
PartEmmit1.LightEmission = 1
PartEmmit1.Texture = "rbxassetid://569507414"
PartEmmit1.Color = ColorSequence.new(maincolor.Color)
PartEmmit1.Rate = 250
PartEmmit1.Lifetime = NumberRange.new(1.6)
PartEmmit1.Size = NumberSequence.new({
	NumberSequenceKeypoint.new(0, 1, 0),
	NumberSequenceKeypoint.new(1, 0, 0)
})
PartEmmit1.Transparency = NumberSequence.new({
	NumberSequenceKeypoint.new(0, 0, 0),
	NumberSequenceKeypoint.new(1, 1, 0)
})
PartEmmit1.Speed = NumberRange.new(0, 0)
PartEmmit1.VelocitySpread = 30000
PartEmmit1.Rotation = NumberRange.new(-360, 360)
PartEmmit1.RotSpeed = NumberRange.new(-360, 360)
local BodPoss = IT("BodyPosition", soul)
BodPoss.P = 3000
BodPoss.D = 1000
BodPoss.maxForce = Vector3.new(50000000000, 50000000000, 50000000000)
BodPoss.position = torso.Position + Vector3.new(Mrandom(-15, 15), Mrandom(-15, 15), Mrandom(-15, 15))
wait(1.6)
soul.Touched:connect(function(hit)
	if hit.Parent == char then
	soul:Destroy()
	end
end)
wait(1.2)
while soul do
	swait()
	PartEmmit1.Color = ColorSequence.new(maincolor.Color)
	BodPoss.Position = tors.Position
end
end)
	soulst()
	end
end
function FaceMouse()
local	Cam = workspace.CurrentCamera
	return {
		CFrame.new(char.Torso.Position, Vector3.new(mouse.Hit.p.x, char.Torso.Position.y, mouse.Hit.p.z)),
		Vector3.new(mouse.Hit.p.x, mouse.Hit.p.y, mouse.Hit.p.z)
	}
end
-------------------------------------------------------
--End Effect Function--
-------------------------------------------------------
function Cso(ID, PARENT, VOLUME, PITCH)
	local NSound = nil
	coroutine.resume(coroutine.create(function()
		NSound = IT("Sound", PARENT)
		NSound.Volume = VOLUME
		NSound.Pitch = PITCH
		NSound.SoundId = "http://www.roblox.com/asset/?id="..ID
		swait()
		NSound:play()
		game:GetService("Debris"):AddItem(NSound, 10)
	end))
	return NSound
end
function CameraEnshaking(Length, Intensity)
	coroutine.resume(coroutine.create(function()
		local intensity = 1 * Intensity
		local rotM = 0.01 * Intensity
		for i = 0, Length, 0.1 do
			swait()
			intensity = intensity - 0.05 * Intensity / Length
			rotM = rotM - 5.0E-4 * Intensity / Length
			hum.CameraOffset = Vector3.new(Rad(Mrandom(-intensity, intensity)), Rad(Mrandom(-intensity, intensity)), Rad(Mrandom(-intensity, intensity)))
			cam.CFrame = cam.CFrame * CF(Rad(Mrandom(-intensity, intensity)), Rad(Mrandom(-intensity, intensity)), Rad(Mrandom(-intensity, intensity))) * Euler(Rad(Mrandom(-intensity, intensity)) * rotM, Rad(Mrandom(-intensity, intensity)) * rotM, Rad(Mrandom(-intensity, intensity)) * rotM)
		end
		hum.CameraOffset = Vector3.new(0, 0, 0)
	end))
end

local Particle = IT("ParticleEmitter",nil)
Particle.Enabled = false
--Particle.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0,1),NumberSequenceKeypoint.new(0.3,0.95),NumberSequenceKeypoint.new(1,1)})
Particle.LightEmission = 0.5
Particle.Rate = 150
Particle.ZOffset = 1
Particle.Rotation = NumberRange.new(-180, 180)
Particle.RotSpeed = NumberRange.new(-180, 180)
Particle.Texture = "http://www.roblox.com/asset/?id=284205403"
Particle.Color = ColorSequence.new(Color3.new(0,0,0),Color3.new(0,0,0))

function ParticleEmitter(Table)
	local PRTCL = Particle:Clone()
	local Speed = Table.Speed or 5
	local Drag = Table.Drag or 0
	local Size1 = Table.Size1 or 1
	local Size2 = Table.Size2 or 5
	local Lifetime1 = Table.Lifetime1 or 1
	local Lifetime2 = Table.Lifetime2 or 1.5
	local Parent = Table.Parent or tors
	local Emit = Table.Emit or 100
	local Offset = Table.Offset or 360
	local Acel = Table.Acel or Vector3.new(0,-50,0)
	local Enabled = Table.Enabled or false
	PRTCL.Parent = Parent
	PRTCL.Size = NumberSequence.new(Size1,Size2)
	PRTCL.Lifetime = NumberRange.new(Lifetime1,Lifetime2)
	PRTCL.Speed = NumberRange.new(Speed)
	PRTCL.VelocitySpread = Offset
	PRTCL.Drag = Drag
	PRTCL.Acceleration = Acel
	if Enabled == false then
		PRTCL:Emit(Emit)
		game:GetService("Debris"):AddItem(PRTCL,Lifetime2)
	else
		PRTCL.Enabled = true
	end
	return PRTCL
end
local PRT = ParticleEmitter({Speed = 0.3, Drag = 3, Size1 = 1.1, Size2 = 0.3, Lifetime1 = 0.2, Lifetime2 = 1, Parent = rl, Emit = 900, Offset = 360, Enabled = true})
--PRT.LockedToPart = true
local PRT = ParticleEmitter({Speed = 0.3, Drag = 3, Size1 = 1.1, Size2 = 0.3, Lifetime1 = 0.2, Lifetime2 = 1, Parent = ll, Emit = 900, Offset = 360, Enabled = true})
--PRT.LockedToPart = true
local PRT = ParticleEmitter({Speed = 0.3, Drag = 3, Size1 = 1.1, Size2 = 0.3, Lifetime1 = 0.3, Lifetime2 = 1.5, Parent = tors, Emit = 900, Offset = 360, Enabled = true})
--PRT.LockedToPart = true
local PRT = ParticleEmitter({Speed = 0.3, Drag = 3, Size1 = 1.1, Size2 = 0.3, Lifetime1 = 0.2, Lifetime2 = 1, Parent = ra, Emit = 900, Offset = 360, Enabled = true})
--PRT.LockedToPart = true
local PRT = ParticleEmitter({Speed = 0.3, Drag = 3, Size1 = 1.1, Size2 = 0.3, Lifetime1 = 0.2, Lifetime2 = 1, Parent = la, Emit = 900, Offset = 360, Enabled = true})
--PRT.LockedToPart = true
function CreateWeldOrSnapOrMotor(TYPE, PARENT, PART0, PART1, C0, C1)
	local NEWWELD = IT(TYPE)
	NEWWELD.Part0 = PART0
	NEWWELD.Part1 = PART1
	NEWWELD.C0 = C0
	NEWWELD.C1 = C1
	NEWWELD.Parent = PARENT
	return NEWWELD
end

function MakeForm(PART,TYPE)
	local MSH = nil
	if TYPE == "Cyl" then
		MSH = IT("CylinderMesh",PART)
	elseif TYPE == "Ball" then
		MSH = IT("SpecialMesh",PART)
		MSH.MeshType = "Sphere"
	elseif TYPE == "Wedge" then
		MSH = IT("SpecialMesh",PART)
		MSH.MeshType = "Wedge"
	elseif TYPE == "Block" then
		MSH = IT("SpecialMesh",PART)
		MSH.MeshType = "Brick"
	end
	return MSH
end

function Raycast(POSITION, DIRECTION, RANGE, IGNOREDECENDANTS)
	return workspace:FindPartOnRay(Ray.new(POSITION, DIRECTION.unit * RANGE), IGNOREDECENDANTS)
end

function Sink(position,radius)
	for i,v in ipairs(workspace:GetChildren()) do
	if v:FindFirstChild("Hit2By"..plr.Name) == nil then
		local body = v:GetChildren()
			for part = 1, #body do
				if(v:FindFirstChild("Hit2By"..plr.Name) == nil and (body[part].ClassName == "Part" or body[part].ClassName == "MeshPart") and v ~= char) then
					if(body[part].Position - position).Magnitude < radius then
						if v.ClassName == "Model" then
							v:FindFirstChildOfClass("Humanoid").Name = "Humanoid"
							if v:FindFirstChild("Humanoid") then
								local defence = Instance.new("BoolValue",v)
								defence.Name = ("Hit2By"..plr.Name)
								if v.Humanoid.Health ~= 0 then
									local TORS = v:FindFirstChild("HumanoidRootPart") or v:FindFirstChild("Torso") or v:FindFirstChild("UpperTorso")
									if TORS ~= nil then
										local HITFLOOR2, HITPOS2 = Raycast(TORS.Position, (CF(TORS.Position, TORS.Position + Vector3.new(0, -1, 0))).lookVector, 25 * TORS.Size.Y/2, v)
										coroutine.resume(coroutine.create(function()
											if HITFLOOR2 ~= nil then
												TORS.Anchored = true
												local Hole2 = CreatePart(3, EffectModel, "Neon", 0, 0, "Really black", "Hole", Vector3.new(TORS.Size.X*4,0,TORS.Size.X*4))
												Hole2.Color = Color3.new(0,0,0)
												local MESH = MakeForm(Hole2,"Cyl")
												MESH.Scale = Vector3.new(0,1,0)
												Hole2.CFrame = CF(HITPOS2)
												for i = 1, 10 do
													swait()
													MESH.Scale = MESH.Scale + Vector3.new(0.1,0,0.1)
												end
												--Cso("160440683", v:FindFirstChild("Head"), 10, .8)
												Cso("154955269", v:FindFirstChild("Head"), 10, 1)
												repeat
													swait()
													TORS.CFrame = TORS.CFrame * CF(0,-0.1,0)
													--MESH.Scale = MESH.Scale + Vector3.new(0,1.6,0)
												until TORS.Position.Y<position.Y-4
												v:remove()
												for i = 1, 10 do
													swait()
													MESH.Scale = MESH.Scale - Vector3.new(0.1,0,0.1)
												end
												Hole2:remove()
											end
										end))
									end
								end
							end
						end
						--body[part].Velocity = CFrame.new(position,body[part].Position).lookVector*5*maxstrength
					end
				end
			end
		end	
	end
end
function Trail(Part)
	local TRAIL = Part:Clone()
	TRAIL.CanCollide = false
	TRAIL.Anchored = true
	TRAIL.Parent = EffectModel
	TRAIL.Name = "Trail"
	local TRANS = Part.Transparency
	coroutine.resume(coroutine.create(function()
		for i = 1, 20 do
			swait()
			TRAIL.Transparency = TRAIL.Transparency + ((1-TRANS)/20)
		end
		TRAIL:remove()
	end))
end
function getRegion(point,range,ignore)
    return workspace:FindPartsInRegion3WithIgnoreList(Region3.new(point-Vector3.new(1,1,1)*range/2,point+Vector3.new(1,1,1)*range/2),ignore,100)
end

function GetTorso(char)
	return char:FindFirstChild'Torso' or char:FindFirstChild'UpperTorso' or char:FindFirstChild'LowerTorso' or char:FindFirstChild'HumanoidRootPart'
end

local M = {C=math.cos,R=math.rad,S=math.sin,P=math.pi,RNG=math.random,MRS=math.randomseed,H=math.huge,RRNG = function(min,max,div) return math.rad(math.random(min,max)/(div or 1)) end}

NewInstance = function(instance,parent,properties)
	local inst = Instance.new(instance)
	inst.Parent = parent
	if(properties)then
		for i,v in next, properties do
			pcall(function() inst[i] = v end)
		end
	end
	return inst;
end

function Part(parent,color,material,size,cframe,anchored,cancollide)
	local part = Instance.new("Part")
	part[typeof(color) == 'BrickColor' and 'BrickColor' or 'Color'] = color or Color3.new(0,0,0)
	part.Material = material or Enum.Material.SmoothPlastic
	part.TopSurface,part.BottomSurface=10,10
	part.Size = size or Vector3.new(1,1,1)
	part.CFrame = cframe or CF(0,0,0)
	part.Anchored = anchored or true
	part.CanCollide = cancollide or false
	part.Parent = parent or char
	return part
end
-------------------------------------------------------
--End Important Functions--
-------------------------------------------------------


-------------------------------------------------------
--Start Customization--
-------------------------------------------------------
local Player_Size = 1
if Player_Size ~= 1 then
root.Size = root.Size * Player_Size
tors.Size = tors.Size * Player_Size
hed.Size = hed.Size * Player_Size
ra.Size = ra.Size * Player_Size
la.Size = la.Size * Player_Size
rl.Size = rl.Size * Player_Size
ll.Size = ll.Size * Player_Size
----------------------------------------------------------------------------------
rootj.Parent = root
neck.Parent = tors
RW.Parent = tors
LW.Parent = tors
RH.Parent = tors
LH.Parent = tors
----------------------------------------------------------------------------------
rootj.C0 = RootCF * CF(0 * Player_Size, 0 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(0), Rad(0))
rootj.C1 = RootCF * CF(0 * Player_Size, 0 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(0), Rad(0))
neck.C0 = necko * CF(0 * Player_Size, 0 * Player_Size, 0 + ((1 * Player_Size) - 1)) * angles(Rad(0), Rad(0), Rad(0))
neck.C1 = CF(0 * Player_Size, -0.5 * Player_Size, 0 * Player_Size) * angles(Rad(-90), Rad(0), Rad(180))
RW.C0 = CF(1.5 * Player_Size, 0.5 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(0), Rad(0)) --* RIGHTSHOULDERC0
LW.C0 = CF(-1.5 * Player_Size, 0.5 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(0), Rad(0)) --* LEFTSHOULDERC0
----------------------------------------------------------------------------------
RH.C0 = CF(1 * Player_Size, -1 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(90), Rad(0)) * angles(Rad(0), Rad(0), Rad(0))
LH.C0 = CF(-1 * Player_Size, -1 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(-90), Rad(0)) * angles(Rad(0), Rad(0), Rad(0))
RH.C1 = CF(0.5 * Player_Size, 1 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(90), Rad(0)) * angles(Rad(0), Rad(0), Rad(0))
LH.C1 = CF(-0.5 * Player_Size, 1 * Player_Size, 0 * Player_Size) * angles(Rad(0), Rad(-90), Rad(0)) * angles(Rad(0), Rad(0), Rad(0))
--hat.Parent = Character
end
----------------------------------------------------------------------------------
local SONG = 660140936
local SONG2 = 0
local Music = Instance.new("Sound",tors)
Music.Volume = 2.5
Music.Looped = true
Music.Pitch = 1 --Pitcher
----------------------------------------------------------------------------------
local equipped = false
local idle = 0
local change = 1
local val = 0
local toim = 0
local idleanim = 0.4
local sine = 0
local Sit = 1
local Mode = "Normal"
----------------------------------------------------------------------------------
hum.WalkSpeed = 16
hum.JumpPower = 57
--hum.Animator.Parent = nil
----------------------------------------------------------------------------------
local Hole = CreatePart(3, EffectModel, "Neon", 0, 0, "Really black", "Hole", Vector3.new(5,0,5))
local MESH = MakeForm(Hole,"Cyl")
local ROBLOXIDLEANIMATION = IT("Animation")
ROBLOXIDLEANIMATION.Name = "Roblox Idle Animation"
ROBLOXIDLEANIMATION.AnimationId = "http://www.roblox.com/asset/?id=180435571"
local ANIMATOR = hum.Animator
local ANIMATE = char.Animate
-------------------------------------------------------
--End Customization--
-------------------------------------------------------


-------------------------------------------------------
--Start Attacks N Stuff--
-------------------------------------------------------
function InkyWarp()
	attack = true
	attack = true
	hum.WalkSpeed = 0
	root.Anchored = true
	for i = 0, 4, 0.1 do
		swait()
		rootj.C0 = clerp(rootj.C0, RootCF * CF(0 - 0.04 * Sin(sine / 24) * Player_Size, 0 + 0.04 * Sin(sine / 12) * Player_Size, 0 + 0.05 * Player_Size * Cos(sine / 12)) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(0 - 2.5 * Sin(sine / 24)), Rad(0)), 0.15)
		tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(25 - 6.5 * Cos(sine / 12)), Rad(0), Rad(20 * Cos(sine / 12))), 0.3)
		RH.C0 = clerp(RH.C0, CF(1 * Player_Size, -1 * Player_Size + 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(84), Rad(0)) * angles(Rad(-6 - 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		LH.C0 = clerp(LH.C0, CF(-1 * Player_Size, -1 * Player_Size - 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(-84), Rad(0)) * angles(Rad(-6 + 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(-6 + 4.5 * Sin(sine / 12)), Rad(25 + 2.5 * Sin(sine / 12)), Rad(25 + 4.5 * Sin(sine / 12))), 0.1)
		LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(7 + 4.5 * Sin(sine / 12)), Rad(0 + 2.5 * Sin(sine / 12)), Rad(-13 - 4.5 * Sin(sine / 12))), 0.1)
	end
	for i = 0, 2, 0.1 do
		swait()
		rootj.C0 = clerp(rootj.C0, RootCF * CF(0 - 0.04 * Sin(sine / 24) * Player_Size, 0 + 0.04 * Sin(sine / 12) * Player_Size, -15 + 0.05 * Player_Size * Cos(sine / 12)) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(0 - 2.5 * Sin(sine / 24)), Rad(0)), 0.15)
		tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(25 - 6.5 * Cos(sine / 12)), Rad(0), Rad(20 * Cos(sine / 12))), 0.3)
		RH.C0 = clerp(RH.C0, CF(1 * Player_Size, -1 * Player_Size + 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(84), Rad(0)) * angles(Rad(-6 - 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		LH.C0 = clerp(LH.C0, CF(-1 * Player_Size, -1 * Player_Size - 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(-84), Rad(0)) * angles(Rad(-6 + 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(-6 + 4.5 * Sin(sine / 12)), Rad(25 + 2.5 * Sin(sine / 12)), Rad(25 + 4.5 * Sin(sine / 12))), 0.1)
		LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(7 + 4.5 * Sin(sine / 12)), Rad(0 + 2.5 * Sin(sine / 12)), Rad(-13 - 4.5 * Sin(sine / 12))), 0.1)
	end
	for i = 1, 50 do
		swait()
		Trail(Hole)
		MESH.Scale = MESH.Scale - Vector3.new(0.02,0,0.02)
	end
	local ORIGINPOS = root.Position
	root.CFrame = CF(Vector3.new(mouse.Hit.p.X,root.Position.Y,mouse.Hit.p.Z),ORIGINPOS)
	Cso("154955269", tors, 10, .8)
	for i = 1, 50 do
		swait()
		MESH.Scale = MESH.Scale + Vector3.new(0.02,0,0.02)
	end
	for i = 0, 4, 0.1 do
		swait()
		rootj.C0 = clerp(rootj.C0, RootCF * CF(0 - 0.04 * Sin(sine / 24) * Player_Size, 0 + 0.04 * Sin(sine / 12) * Player_Size, 0 + 0.05 * Player_Size * Cos(sine / 12)) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(0 - 2.5 * Sin(sine / 24)), Rad(0)), 0.15)
		tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(25 - 6.5 * Cos(sine / 12)), Rad(0), Rad(20 * Cos(sine / 12))), 0.3)
		RH.C0 = clerp(RH.C0, CF(1 * Player_Size, -1 * Player_Size + 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(84), Rad(0)) * angles(Rad(-6 - 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		LH.C0 = clerp(LH.C0, CF(-1 * Player_Size, -1 * Player_Size - 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(-84), Rad(0)) * angles(Rad(-6 + 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
		RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(-6 + 4.5 * Sin(sine / 12)), Rad(25 + 2.5 * Sin(sine / 12)), Rad(25 + 4.5 * Sin(sine / 12))), 0.1)
		LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(7 + 4.5 * Sin(sine / 12)), Rad(0 + 2.5 * Sin(sine / 12)), Rad(-13 - 4.5 * Sin(sine / 12))), 0.1)
	end
	attack = false
	hum.WalkSpeed = 16
	root.Anchored = false
end

-------------------------------------------------------
--End Attacks N Stuff--
-------------------------------------------------------
mouse.KeyDown:connect(function(key)
	if attack == false then
		if key == 'z' then
			InkyWarp()
		elseif key == 'p' and Mode == "Normal" then
			Mode = "Chase"
			SONG = 1634663187
			hum.WalkSpeed = 28
		elseif key == 'p' and Mode == "Chase" then
			Mode = "Normal"
			SONG = 660140936
			hum.WalkSpeed = 16
		end
	end
end)

 






-------------------------------------------------------
--Start Animations--
-------------------------------------------------------
print("By Makhail07")
coroutine.resume(coroutine.create(function()
	while wait() do
	if hitfloor ~= nil then
		Hole.CFrame = CF(posfloor)
	end
	Sink(Hole.Position, Hole.Size.X/2.2 * MESH.Scale.X)
	Hole.Color = Color3.new(0,0,0)
	Trail(Hole)
	end
end))
while true do
	swait()
	sine = sine + change
	ANIMATE.Parent = nil
	local IDLEANIMATION = hum:LoadAnimation(ROBLOXIDLEANIMATION)
	IDLEANIMATION:Play()
	local torvel = (root.Velocity * Vector3.new(1, 0, 1)).magnitude
	local velderp = root.Velocity.y
	hitfloor, posfloor = rayCast(root.Position, CFrame.new(root.Position, root.Position - Vector3.new(0, 1, 0)).lookVector, 4 * Player_Size, char)
	if equipped == true or equipped == false then
		if attack == false then
			idle = idle + 1
		else
			idle = 0
		end
		if 1 < root.Velocity.y and hitfloor == nil then
			Anim = "Jump"
			if attack == false then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0* Player_Size, 0* Player_Size, -0.1 + 0.1 * Cos(sine / 20)* Player_Size) * angles(Rad(-16), Rad(0), Rad(0)), 0.15)
				neck.C0 = clerp(neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(0 - 2.5 * Sin(sine / 30)), Rad(0), Rad(0)), 0.3)
				RH.C0 = clerp(RH.C0, CF(1* Player_Size, -0.9 - 0.1 * Cos(sine / 20)* Player_Size, 0* Player_Size) * RHCF * angles(Rad(-6.5), Rad(0), Rad(0)), 0.15)
				LH.C0 = clerp(LH.C0, CF(-1* Player_Size, -.9 - 0.1 * Cos(sine / 20), -.5* Player_Size) * LHCF * angles(Rad(-6.5), Rad(0), Rad(0)), 0.15)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.5 + 0.02 * Sin(sine / 20)* Player_Size, 0* Player_Size) * angles(Rad(25), Rad(-.6), Rad(13 + 4.5 * Sin(sine / 20))), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.5 + 0.02 * Sin(sine / 20)* Player_Size, 0* Player_Size) * angles(Rad(25), Rad(-.6), Rad(-13 - 4.5 * Sin(sine / 20))), 0.1)
			end
		elseif -1 > root.Velocity.y and hitfloor == nil then
			Anim = "Fall"
			if attack == false then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0* Player_Size, 0* Player_Size, -0.1 + 0.1 * Cos(sine / 20)* Player_Size) * angles(Rad(15), Rad(0), Rad(0)), 0.15)
				neck.C0 = clerp(neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(10 - 2.5 * Sin(sine / 30)), Rad(0), Rad(0)), 0.3)
				RH.C0 = clerp(RH.C0, CF(1* Player_Size, -1 - 0.1 * Cos(sine / 20)* Player_Size, 0* Player_Size) * RHCF * angles(Rad(-9.5), Rad(0), Rad(20)), 0.15)
				LH.C0 = clerp(LH.C0, CF(-1* Player_Size, -.4 - 0.1 * Cos(sine / 20)* Player_Size, -.5* Player_Size) * LHCF * angles(Rad(-9.5), Rad(0), Rad(20)), 0.15)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.5 + 0.02 * Sin(sine / 20)* Player_Size, 0* Player_Size) * angles(Rad(65), Rad(-.6), Rad(75 + 4.5 * Sin(sine / 20))), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.5 + 0.02 * Sin(sine / 20)* Player_Size, 0* Player_Size) * angles(Rad(55), Rad(-.6), Rad(-75 - 4.5 * Sin(sine / 20))), 0.1)
			end
		elseif torvel < 1 and hitfloor ~= nil then
			Anim = "Idle"
			change = 1
			if attack == false then
				if Mode == "Normal" then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0 - 0.04 * Sin(sine / 24) * Player_Size, 0 + 0.04 * Sin(sine / 12) * Player_Size, 0 + 0.05 * Player_Size * Cos(sine / 12)) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(0 - 2.5 * Sin(sine / 24)), Rad(0)), 0.15)
				tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(25 - 6.5 * Cos(sine / 12)), Rad(0), Rad(20 * Cos(sine / 12))), 0.3)
				RH.C0 = clerp(RH.C0, CF(1 * Player_Size, -1 * Player_Size + 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(84), Rad(0)) * angles(Rad(-6 - 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
				LH.C0 = clerp(LH.C0, CF(-1 * Player_Size, -1 * Player_Size - 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(-84), Rad(0)) * angles(Rad(-6 + 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(-6 + 4.5 * Sin(sine / 12)), Rad(25 + 2.5 * Sin(sine / 12)), Rad(25 + 4.5 * Sin(sine / 12))), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(7 + 4.5 * Sin(sine / 12)), Rad(0 + 2.5 * Sin(sine / 12)), Rad(-13 - 4.5 * Sin(sine / 12))), 0.1)
			elseif Mode == "Chase" then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0 - 0.04 * Sin(sine / 24) * Player_Size, 0 + 0.04 * Sin(sine / 12) * Player_Size, 0 + 0.05 * Player_Size * Cos(sine / 12)) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(0 - 2.5 * Sin(sine / 24)), Rad(0)), 0.15)
				tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(-6.5 * Cos(sine / 12)), Rad(10), Rad(0)), 0.3)
				RH.C0 = clerp(RH.C0, CF(1 * Player_Size, -1 * Player_Size + 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(84), Rad(0)) * angles(Rad(-6 - 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
				LH.C0 = clerp(LH.C0, CF(-1 * Player_Size, -1 * Player_Size - 0.06 * Sin(sine / 24) - 0.05 * Player_Size * Cos(sine / 12), -0.01 * Player_Size) * angles(Rad(0 - 2.5 * Sin(sine / 12)), Rad(-84), Rad(0)) * angles(Rad(-6 + 2.5 * Sin(sine / 24)), Rad(0), Rad(0)), 0.15)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(-6 + 4.5 * Sin(sine / 12)), Rad(25 + 2.5 * Sin(sine / 12)), Rad(5)), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.35 + 0.15 * Cos(sine / 12)* Player_Size, 0* Player_Size) * angles(Rad(7 + 4.5 * Sin(sine / 12)), Rad(0 + 2.5 * Sin(sine / 12)), Rad(-5)), 0.1)
				end
			end
		elseif (tors.Velocity).magnitude < 200 and hitfloor ~= nil then
			Anim = "Walk"
			change = 1.1
			if attack == false then
				if Mode == "Normal" then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0* Player_Size, 0* Player_Size, -0.175 + 0.13 * Cos(sine / 3.5) + -Sin(sine / 3.5) / 7* Player_Size) * angles(Rad(3 - 2.5 * Cos(sine / 3.5)), Rad(0) - root.RotVelocity.Y / 75, Rad(10 * Cos(sine / 7))), 0.15)
				tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(0), Rad(0), Rad(0) - hed.RotVelocity.Y / 15), 0.3)
				RH.C0 = clerp(RH.C0, CF(1* Player_Size, -0.8 - 0.5 * Cos(sine / 7) / 2* Player_Size, 0.6 * Cos(sine / 7) / 2* Player_Size)  * angles(Rad(-10 - 25 * Cos(sine / 7)) - rl.RotVelocity.Y / 75 + -Sin(sine / 7) / 2.5, Rad(90 - 15 * Cos(sine / 7)), Rad(0)) * angles(Rad(0 + 2 * Cos(sine / 7)), Rad(0), Rad(0)), 0.3)
         		LH.C0 = clerp(LH.C0, CF(-1* Player_Size, -0.8 + 0.5 * Cos(sine / 7) / 2* Player_Size, -0.6 * Cos(sine / 7) / 2* Player_Size) * angles(Rad(-10 + 25 * Cos(sine / 7)) + ll.RotVelocity.Y / 75 + Sin(sine / 7) / 2.5, Rad(-90 - 15 * Cos(sine / 7)), Rad(0)) * angles(Rad(0 - 2 * Cos(sine / 7)), Rad(0), Rad(0)), 0.3)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.5 + 0.05 * Sin(sine / 7)* Player_Size, 0* Player_Size) * angles(Rad(57)  * Cos(sine / 7) , Rad(10 * Cos(sine / 7)), Rad(10) - ra.RotVelocity.Y / 75), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.5 + 0.05 * Sin(sine / 7)* Player_Size, 0* Player_Size) * angles(Rad(-57)  * Cos(sine / 7) , Rad(10 * Cos(sine / 7)) ,	Rad(-10) + la.RotVelocity.Y / 75), 0.1)
			elseif Mode == "Chase" then
				rootj.C0 = clerp(rootj.C0, RootCF * CF(0* Player_Size, 0* Player_Size, -0.175 + 0.13 * Cos(sine / 3.5) + -Sin(sine / 3.5) / 7* Player_Size) * angles(Rad(3 - 2.5 * Cos(sine / 3.5)), Rad(0) - root.RotVelocity.Y / 75, Rad(17 + 8 * Cos(sine / 7))), 0.15)
				tors.Neck.C0 = clerp(tors.Neck.C0, necko* CF(0, 0, 0 + ((1* Player_Size) - 1)) * angles(Rad(0), Rad(0), Rad(-17) - hed.RotVelocity.Y / 15), 0.3)
				RH.C0 = clerp(RH.C0, CF(1* Player_Size, -0.8 - 0.5 * Cos(sine / 7) / 2* Player_Size, 0.6 * Cos(sine / 7) / 2* Player_Size)  * angles(Rad(-15 - 5 * Cos(sine / 7)) - rl.RotVelocity.Y / 75 + -Sin(sine / 7) / 2.5, Rad(90 - 15 * Cos(sine / 7)), Rad(0)) * angles(Rad(0 + 2 * Cos(sine / 7)), Rad(0), Rad(0)), 0.3)
         		LH.C0 = clerp(LH.C0, CF(-1* Player_Size, -0.8 + 0.5 * Cos(sine / 7) / 2* Player_Size, -0.6 * Cos(sine / 7) / 2* Player_Size) * angles(Rad(-15 + 5 * Cos(sine / 7)) + ll.RotVelocity.Y / 75 + Sin(sine / 7) / 2.5, Rad(-90 - 15 * Cos(sine / 7)), Rad(0)) * angles(Rad(0 - 2 * Cos(sine / 7)), Rad(0), Rad(0)), 0.3)
				RW.C0 = clerp(RW.C0, CF(1.5* Player_Size, 0.5 + 0.05 * Sin(sine / 7)* Player_Size, 0* Player_Size) * angles(Rad(90)  , Rad(10 * Cos(sine / 7)), Rad(28) - ra.RotVelocity.Y / 75), 0.1)
				LW.C0 = clerp(LW.C0, CF(-1.5* Player_Size, 0.5 + 0.05 * Sin(sine / 7)* Player_Size, 0* Player_Size) * angles(Rad(-57)  * Cos(sine / 7) , Rad(10 * Cos(sine / 7)) ,	Rad(-10) + la.RotVelocity.Y / 75), 0.1)
				end
			end
		end
	end
	for _, c in pairs(char:GetDescendants()) do
		if c.ClassName == "Part" and c.Name ~= "Eye" and c.Parent ~= Effects and c.Parent.Parent ~= Effects then
			c.Material = "Neon"
			c.Color = Color3.new(0,0,0)
			if c:FindFirstChildOfClass("SpecialMesh") then
				c:FindFirstChildOfClass("SpecialMesh").TextureId = ""
			end
			if c == hed then
				if c:FindFirstChild("face") then
					c.face:remove()
				end
			end
		elseif c.ClassName == "Part" and c.Name == "Eye" then
			c.Color = Color3.new(1,0,0)
			c.Material = "Neon"
		elseif c.ClassName == "CharacterMesh" or c.Name == "Body Colors" then
			c:remove()
		elseif (c.ClassName == "Shirt" or c.ClassName == "Pants") and c.Name ~= "Cloth" then
			c:remove()
		end
	end
	Music.SoundId = "rbxassetid://"..SONG
	Music.Looped = true
	Music.Pitch = 1
	Music.Volume = 5
	Music.Parent = tors
	Music:Resume()
	if 0 < #Effects then
		for e = 1, #Effects do
			if Effects[e] ~= nil then
				local Thing = Effects[e]
				if Thing ~= nil then
					local Part = Thing[1]
					local Mode = Thing[2]
					local Delay = Thing[3]
					local IncX = Thing[4]
					local IncY = Thing[5]
					local IncZ = Thing[6]
					if 1 >= Thing[1].Transparency then
						if Thing[2] == "Block1" then
							Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50))
							local Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Block2" then
							Thing[1].CFrame = Thing[1].CFrame + Vector3.new(0, 0, 0)
							local Mesh = Thing[7]
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Block3" then
							Thing[1].CFrame = Thing[1].CFrame * CFrame.fromEulerAnglesXYZ(math.random(-50, 50), math.random(-50, 50), math.random(-50, 50)) + Vector3.new(0, 0.15, 0)
							local Mesh = Thing[7]
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Cylinder" then
							local Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Blood" then
							local Mesh = Thing[7]
							Thing[1].CFrame = Thing[1].CFrame * Vector3.new(0, 0.5, 0)
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[4], Thing[5], Thing[6])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Elec" then
							local Mesh = Thing[1].Mesh
							Mesh.Scale = Mesh.Scale + Vector3.new(Thing[7], Thing[8], Thing[9])
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Disappear" then
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
						elseif Thing[2] == "Shatter" then
							Thing[1].Transparency = Thing[1].Transparency + Thing[3]
							Thing[4] = Thing[4] * CFrame.new(0, Thing[7], 0)
							Thing[1].CFrame = Thing[4] * CFrame.fromEulerAnglesXYZ(Thing[6], 0, 0)
							Thing[6] = Thing[6] + Thing[5]
						end
					else
						Part.Parent = nil
						table.remove(Effects, e)
					end
				end
			end
		end
	end
end
-------------------------------------------------------
--End Animations And Script--
-------------------------------------------------------
