function onTick()
	
	ThisD=math.floor(input.getNumber(13))
	Dest=math.floor(input.getNumber(14))
	distance=input.getNumber(15)
	N1=input.getNumber(29)
	N2=input.getNumber(30)
	N3=input.getNumber(31)
	N4=input.getNumber(32)
	NX=input.getNumber(16)
	NY=input.getNumber(17)
	
		
	if(Dest==2)then
	
		tgt1=math.floor(input.getNumber(5))
		tgt2=math.floor(input.getNumber(6))
		tgt3=math.floor(input.getNumber(7))
		tgt4=math.floor(input.getNumber(8))
	else
		if(Dest==1)then 
			tgt1=math.floor(input.getNumber(1))
			tgt2=math.floor(input.getNumber(2))
			tgt3=math.floor(input.getNumber(3))
			tgt4=math.floor(input.getNumber(4))	
		end
	end
	if(Dest==0)then
		tgt1=0
		tgt2=0
		tgt3=0
		tgt4=0
		
	end
	if(ThisD==tgt1 and N1==Dest)then
		K1=1
	end
	if(ThisD==tgt2 and N2==Dest)then
		K1=2
	end
	if(ThisD==tgt3 and N3==Dest)then
		K1=3
	end
	if(ThisD==tgt4 and N4==Dest)then
		K1=4
	end
	Foutput=0
	outputD=0
	if(ThisD==0 or Dest==0)then else 
		Foutput=K1

	 end
			TX=input.getNumber(20+Foutput)
		TY=input.getNumber(24+Foutput)
		FCD=math.sqrt( (NX-TX)^2 + (NY-TY)^2 )
	outputD=FCD
	output.setNumber(1,outputD)
	output.setNumber(10,Foutput)
end
