
<!DOCTYPE html>
<html>
<body>

<canvas id="myCanvas" width="800" height="300" style="border:1px solid #d3d3d3;">
click counter:</canvas>

<script>

var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var count1=0;
var count2=0;
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black"; 
		ctx.moveTo(300,40);
		ctx.lineTo(450,40);
		ctx.stroke();
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black";  
		ctx.moveTo(300,20);
		ctx.lineTo(300,80);
		ctx.stroke();
		ctx.globalAlpha = 0.3;
		ctx.beginPath();
		ctx.rect(300,20,74,20);
		ctx.fillStyle = 'blue';
		ctx.fill();
		ctx.globalAlpha = 0.3;
		ctx.beginPath();
		ctx.rect(374,20,76,20);
		ctx.fillStyle = 'red';
		ctx.fill();
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black";  
		ctx.moveTo(450,20);
		ctx.lineTo(450,80);
		ctx.stroke();
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black";  
		ctx.moveTo(374,20);
		ctx.lineTo(374,80);
		ctx.stroke();
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black";  
		ctx.moveTo(300,20);
		ctx.lineTo(450,20);
		ctx.stroke();
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "black";  
		ctx.moveTo(300,80);
		ctx.lineTo(450,80);
		ctx.stroke();
		ctx.font = "40px Verdana";
		ctx.fillText(count1,310,75);
		ctx.font = "40px Verdana";
		ctx.fillText(count2,380,75);
		
function stroke_fn(a,b,c,d,flag)
{
	if(flag % 2 ==0)
	{
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "blue";  
		ctx.moveTo(a,b);
		ctx.lineTo(c,d);
		ctx.stroke();
	}
	else
	{
		ctx.globalAlpha = 1;
		ctx.beginPath();
		ctx.strokeStyle = "red";  
		ctx.moveTo(a,b);
		ctx.lineTo(c,d);
		ctx.stroke();
	}
		
}
function fill_fn(u,v,flag)
{
	if(flag % 2 ==0)
	{
		count1+=5;
		ctx.globalAlpha = 0.3;
		ctx.beginPath();
		ctx.rect(u,v,30,30);
		ctx.fillStyle = 'blue';
		ctx.fill();
		ctx.clearRect(305,43,65,35);
		ctx.font = "40px Verdana";
		ctx.fillText(count1,310,75);
		
	}
	else
	{
		count2+=5;
		ctx.globalAlpha = 0.3;
		ctx.beginPath();
		ctx.rect(u,v,30,30);
		ctx.fillStyle = 'red';
		ctx.fill();
		ctx.clearRect(377,43,70,35);
		ctx.font = "40px Verdana";
		ctx.fillText(count2,380,75);
	}
}
var i;
var j;
for(i=10;i<=190;i+=30)
{
	for(j=10;j<=190;j+=30)
	{
		ctx.beginPath();
		ctx.arc(i, j, 4, 0, 2 * Math.PI);
		ctx.stroke();
	}
}
var number = 1;
var k=false;
var l=false;
var ar = [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0];


c.addEventListener('click', on_canvas_click, false);
function on_canvas_click(ev) 
{		document.onclick = function()
		{
			number++;
			
    			var x = ev.clientX - c.offsetLeft;
         		var y = ev.clientY - c.offsetTop;
			
			
				if(number % 2 == 0)
				{
		
  					if((x>=5) && (x<15) &&(k===false))
					{
						
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
								stroke_fn(10,15,10,35,number);
								l=true;
								ar[0]++;
								if(ar[0]==4)
								{
									fill_fn(10,10,number);
									
								}		
							
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							
							stroke_fn(10,45,10,65,number);
							l=true;
							ar[6]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							} 
							
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							
							stroke_fn(10,75,10,95,number);
							l=true;
							ar[12]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							} 
							
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							
							stroke_fn(10,105,10,125,number);
							l=true;
							ar[18]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							} 
							
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							
							stroke_fn(10,135,10,155,number);
							l=true;
							ar[24]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							} 
							
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							
							stroke_fn(10,165,10,185,number);
							l=true;
							ar[30]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							} 
							
						}
						else 
						k=false;

					}
					else
					if((x>=35) && (x<45) && (k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							
							stroke_fn(40,15,40,35,number);
							l=true;
							ar[0]++;
							ar[1]++;
							if(ar[0]==4)
							{
								
								fill_fn(10,10,number);
							}
							
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							
							stroke_fn(40,45,40,65,number);
							l=true;
							ar[6]++;
							ar[7]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
						
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							
							stroke_fn(40,75,40,95,number);
							l=true;
							ar[12]++;
							ar[13]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							} 
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							
							stroke_fn(40,105,40,125,number);
							l=true;
							ar[18]++;
							ar[19]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							} 
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							
							stroke_fn(40,135,40,155,number);
							l=true;
							ar[24]++;
							ar[25]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							} 
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							
							
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							
							stroke_fn(40,165,40,185,number);
							l=true;
							ar[30]++;
							ar[31]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							} 
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else 
						k=false;
					}
					else
					if((x>=65) && (x<75) &&( k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							stroke_fn(70,15,70,35,number);
							l=true;
							ar[1]++;
							ar[2]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							stroke_fn(70,45,70,65,number);
							l=true;
							ar[7]++;
							ar[8]++;
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							stroke_fn(70,75,70,95,number);
							l=true;
							ar[13]++;
							ar[14]++;
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							} 
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							stroke_fn(70,105,70,125,number);
							l=true;
							ar[19]++;
							ar[20]++;
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							} 
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							
							stroke_fn(70,135,70,155,number);
							l=true;
							ar[25]++;
							ar[26]++;
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							} 
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							
							
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							
							stroke_fn(70,165,70,185,number);
							l=true;
							ar[31]++;
							ar[32]++;
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							} 
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						k=false;
					}
					else
					if((x>=95) && (x<105) &&( k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							stroke_fn(100,15,100,35,number);
							l=true;
							ar[2]++;
							ar[3]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							stroke_fn(100,45,100,65,number);
							l=true;
							ar[8]++;
							ar[9]++;
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							stroke_fn(100,75,100,95,number);
							l=true;
							ar[14]++;
							ar[15]++;
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}  
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							stroke_fn(100,105,100,125,number);
							l=true;
							ar[20]++;
							ar[21]++;
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							} 
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							stroke_fn(100,135,100,155,number);
							l=true;
							ar[26]++;
							ar[27]++;
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							} 
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							stroke_fn(100,165,100,185,number);
							l=true;
							ar[32]++;
							ar[33]++;
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							} 
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}	
						}
						else
						k=false;	
					}
					else
					if((x>=125) && (x<135) &&( k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							stroke_fn(130,15,130,35,number);
							l=true;
							ar[3]++;
							ar[4]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							stroke_fn(130,45,130,65,number);
							l=true;
							ar[9]++;
							ar[10]++;
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							stroke_fn(130,75,130,95,number);
							l=true;
							ar[15]++;
							ar[16]++;
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}  
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							stroke_fn(130,105,130,125,number);
							l=true;
							ar[21]++;
							ar[22]++;
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							} 
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							stroke_fn(130,135,130,155,number);
							l=true;
							ar[27]++;
							ar[28]++;
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							} 
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							stroke_fn(130,165,130,185,number);
							l=true;
							ar[33]++;
							ar[34]++;
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							} 
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}	
						}
						else
						k=false;	
					}
					else
					if((x>=155) && (x<165) &&( k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							stroke_fn(160,15,160,35,number);
							l=true;
							ar[4]++;
							ar[5]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							stroke_fn(160,45,160,65,number);
							l=true;
							ar[10]++;
							ar[11]++;
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							stroke_fn(160,75,160,95,number);
							l=true;
							ar[16]++;
							ar[17]++;
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}  
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							stroke_fn(160,105,160,125,number);
							l=true;
							ar[22]++;
							ar[23]++;
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							} 
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							stroke_fn(160,135,160,155,number);
							l=true;
							ar[28]++;
							ar[29]++;
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							} 
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							stroke_fn(160,165,160,185,number);
							l=true;
							ar[34]++;
							ar[35]++;
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							} 
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}	
						}
						else
						k=false;	
					}
					else
					if((x>=185) && (x<195) &&( k===false))
					{
						k=true;
						if((y>=15) && (y<35) && (l===false))
						{
							stroke_fn(190,15,190,35,number);
							l=true;
							ar[5]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===false))
						{
							stroke_fn(190,45,190,65,number);
							l=true;
							ar[11]++;
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===false))
						{
							stroke_fn(190,75,190,95,number);
							l=true;
							ar[17]++;
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===false))
						{
							stroke_fn(190,105,190,125,number);
							l=true;
							ar[23]++;
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===false))
						{
							stroke_fn(190,135,190,155,number);
							l=true;
							ar[29]++;
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===false))
						{
							stroke_fn(190,165,190,185,number);
							l=true;
							ar[35]++;
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}	
						}
						else
						k=false;	
					}
					else
					if((y>=5) && (y<15) && (k===false))
					{
						k=true;
						if((x>=15) && (x<35) &&(l===false))
						{
							stroke_fn(15,10,35,10,number);
							l=true;
							ar[0]++;
							if(ar[0]==4)
							{
								fill_fn(10,10,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65)&&(l===false))
						{
							
							stroke_fn(45,10,65,10,number);
							l=true;
							ar[1]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
						}
						else
						if((x>=75) && (x<95)&&(l===false))
						{
							
							stroke_fn(75,10,95,10,number);
							l=true;
							ar[2]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
						}
						else
						if((x>=105) && (x<125)&&(l===false))
						{
							
							stroke_fn(105,10,125,10,number);
							l=true;
							ar[3]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
						}
						else
						if((x>=135) && (x<155)&&(l===false))
						{
							
							stroke_fn(135,10,155,10,number);
							l=true;
							ar[4]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
						}
						else
						if((x>=165) && (x<185)&&(l===false))
						{
							
							stroke_fn(165,10,185,10,number);
							l=true;
							ar[5]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else k=false;

					}
					else
					if((y>=35) &&(y<45)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,40,35,40,number);
							l=true;
							ar[0]++;
							ar[6]++;
							if(ar[0]==4)
							{
								fill_fn(10,10,number);
							}
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
							stroke_fn(45,40,65,40,number);
							l=true;
							ar[1]++;
							ar[7]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
							stroke_fn(75,40,95,40,number);
							l=true;
							ar[2]++;
							ar[8]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
						}
						else
						if((x>=105) && (x<125) &&(l===false))
						{
							stroke_fn(105,40,125,40,number);
							l=true;
							ar[3]++;
							ar[9]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
						}
						else
						if((x>=135) && (x<155) &&(l===false))
						{
							stroke_fn(135,40,155,40,number);
							l=true;
							ar[4]++;
							ar[10]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
						}
						else
						if((x>165) && (x<185) &&(l===false))
						{
							stroke_fn(165,40,185,40,number);
							l=true;
							ar[5]++;
							ar[11]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else 
						k=false;
						
					}
					else
					if((y>=65)&&(y<75)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,70,35,70,number);
							l=true;
							ar[6]++;
							ar[12]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
						
							stroke_fn(45,70,65,70,number);
							l=true;	
							ar[7]++;
							ar[13]++;
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
						
							stroke_fn(75,70,95,70,number);
							l=true;	
							ar[8]++;
							ar[14]++;
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===false))
						{
						
							stroke_fn(105,70,125,70,number);
							l=true;	
							ar[9]++;
							ar[15]++;
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
							
						}
						else
						if((x>135) && (x<155) &&(l===false))
						{
						
							stroke_fn(135,70,155,70,number);
							l=true;	
							ar[10]++;
							ar[16]++;
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
							
						}
						else
						if((x>165) && (x<185) &&(l===false))
						{
						
							stroke_fn(165,70,185,70,number);
							l=true;	
							ar[11]++;
							ar[17]++;
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
							
						}
						else
						k=false;

					}
					else
					if((y>=95)&&(y<105)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,100,35,100,number);
							l=true;
							ar[12]++;
							ar[18]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							}
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
						
							stroke_fn(45,100,65,100,number);
							l=true;	
							ar[13]++;
							ar[19]++;
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
						
							stroke_fn(75,100,95,100,number);
							l=true;	
							ar[14]++;
							ar[20]++;
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===false))
						{
						
							stroke_fn(105,100,125,100,number);
							l=true;	
							ar[15]++;
							ar[21]++;
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===false))
						{
						
							stroke_fn(135,100,155,100,number);
							l=true;	
							ar[16]++;
							ar[22]++;
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===false))
						{
						
							stroke_fn(165,100,185,100,number);
							l=true;	
							ar[17]++;
							ar[23]++;
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
							
						}
						else
						k=false;

					}
					else
					if((y>=125)&&(y<135)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,130,35,130,number);
							l=true;
							ar[18]++;
							ar[24]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							}
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
						
							stroke_fn(45,130,65,130,number);
							l=true;	
							ar[19]++;
							ar[25]++;
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
						
							stroke_fn(75,130,95,130,number);
							l=true;	
							ar[20]++;
							ar[26]++;
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===false))
						{
						
							stroke_fn(105,130,125,130,number);
							l=true;	
							ar[21]++;
							ar[27]++;
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===false))
						{
						
							stroke_fn(135,130,155,130,number);
							l=true;	
							ar[22]++;
							ar[28]++;
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===false))
						{
						
							stroke_fn(165,130,185,130,number);
							l=true;	
							ar[23]++;
							ar[29]++;
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
							
						}
						else
						k=false;

					}
					else
					if((y>=155)&&(y<165)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,160,35,160,number);
							l=true;
							ar[24]++;
							ar[30]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							}
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
						
							stroke_fn(45,160,65,160,number);
							l=true;	
							ar[25]++;
							ar[31]++;
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
						
							stroke_fn(75,160,95,160,number);
							l=true;	
							ar[26]++;
							ar[32]++;
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===false))
						{
						
							stroke_fn(105,160,125,160,number);
							l=true;	
							ar[27]++;
							ar[33]++;
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===false))
						{
						
							stroke_fn(135,160,155,160,number);
							l=true;	
							ar[28]++;
							ar[34]++;
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===false))
						{
						
							stroke_fn(165,160,185,160,number);
							l=true;	
							ar[29]++;
							ar[35]++;
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}
							
						}
						else
						k=false;

					}
					else
					if((y>=185)&&(y<195)&&(k===false))
					{
						k=true;
						if((x>=15) && (x<35)&&(l===false))
						{
							
							stroke_fn(15,190,35,190,number);
							l=true;
							ar[30]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===false))
						{
						
							stroke_fn(45,190,65,190,number);
							l=true;	
							ar[31]++;
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===false))
						{
						
							stroke_fn(75,190,95,190,number);
							l=true;	
							ar[32]++;
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						if((x>105) && (x<125) &&(l===false))
						{
						
							stroke_fn(105,190,125,190,number);
							l=true;	
							ar[33]++;
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===false))
						{
						
							stroke_fn(135,190,155,190,number);
							l=true;	
							ar[34]++;
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===false))
						{
							stroke_fn(165,190,185,190,number);
							l=true;	
							ar[35]++;
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}
							
						}
						else
						k=false;

					}
				}
			    else
				{
					if((x>=5) && (x<15) &&(k===true))
					{
						k=false;				
						
						if((y>=15) &&(y<35)&&(l===true))
						{
								stroke_fn(10,15,10,35,number);
								l=false;
								ar[0]++;
								if(ar[0]==4)
								{
									fill_fn(10,10,number);
								}
						}
						else
						if((y>=45)&&(y<65)&&(l===true))
						{
							stroke_fn(10,45,10,65,number);
							l=false;
							ar[6]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							} 
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							
							stroke_fn(10,75,10,95,number);
							l=false;
							ar[12]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							} 
							
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							
							stroke_fn(10,105,10,125,number);
							l=false;
							ar[18]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							} 
							
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							
							stroke_fn(10,135,10,155,number);
							l=false;
							ar[24]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							} 
							
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							stroke_fn(10,165,10,185,number);
							l=false;
							ar[30]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							} 
						}
						else
						k=true;

					}
					else
					if((x>=35) &&(x<45) &&(k===true))
					{
						k=false;
						
						if((y>=15) &&(y<35)&&(l===true))
						{
							
							stroke_fn(40,15,40,35,number);
							l=false;
							ar[0]++;
							ar[1]++;
							if(ar[0]==4)
							{
								fill_fn(10,10,number);
							}
							
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							
						}else
						if((y>=45)&&(y<65)&&(l===true))
						{
							stroke_fn(40,45,40,65,number);
							l=false;
							ar[6]++;
							ar[7]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
						
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							
							stroke_fn(40,75,40,95,number);
							l=false;
							ar[12]++;
							ar[13]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							} 
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							
							stroke_fn(40,105,40,125,number);
							l=false;
							ar[18]++;
							ar[19]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							} 
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							
							stroke_fn(40,135,40,155,number);
							l=false;
							ar[24]++;
							ar[25]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							} 
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							
							
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							
							stroke_fn(40,165,40,185,number);
							l=false;
							ar[30]++;
							ar[31]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							} 
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else
						k=true;
			
					}
					else
					if((x>=65) &&(x<75) &&(k===true))
					{
						
						k=false;
						if((y>=15) &&(y<35)&&(l===true))
						{
							
							stroke_fn(70,15,70,35,number);
						    l=false;
							ar[1]++;
							ar[2]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
							
						}
						else
						if((y>=45)&&(y<65)&&(l===true))
						{
							
							stroke_fn(70,45,70,65,number);
							l=false;
							ar[7]++;
							ar[8]++;
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
							
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							
							stroke_fn(70,75,70,95,number);
							l=false;
							ar[13]++;
							ar[14]++;
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							} 
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							
							stroke_fn(70,105,70,125,number);
							l=false;
							ar[19]++;
							ar[20]++;
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							} 
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							
							stroke_fn(70,135,70,155,number);
							l=false;
							ar[25]++;
							ar[26]++;
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							} 
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							
							
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							
							stroke_fn(70,165,70,185,number);
							l=false;
							ar[31]++;
							ar[32]++;
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							} 
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						k=true;
					}
					else
					if((x>=95) && (x<105) &&( k===true))
					{
						k=false;
						if((y>=15) && (y<35) && (l===true))
						{
							stroke_fn(100,15,100,35,number);
							l=false;
							ar[2]++;
							ar[3]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===true))
						{
							stroke_fn(100,45,100,65,number);
							l=false;
							ar[8]++;
							ar[9]++;
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							stroke_fn(100,75,100,95,number);
							l=false;
							ar[14]++;
							ar[15]++;
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}  
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							stroke_fn(100,105,100,125,number);
							l=false;
							ar[20]++;
							ar[21]++;
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							} 
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							stroke_fn(100,135,100,155,number);
							l=false;
							ar[26]++;
							ar[27]++;
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							} 
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							stroke_fn(100,165,100,185,number);
							l=false;
							ar[32]++;
							ar[33]++;
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							} 
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}	
						}
						else
						k=true;	
					}
					else
					if((x>=125) && (x<135) &&( k===true))
					{
						k=false;
						if((y>=15) && (y<35) && (l===true))
						{
							stroke_fn(130,15,130,35,number);
							l=false;
							ar[3]++;
							ar[4]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===true))
						{
							stroke_fn(130,45,130,65,number);
							l=false;
							ar[9]++;
							ar[10]++;
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							stroke_fn(130,75,130,95,number);
							l=false;
							ar[15]++;
							ar[16]++;
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}  
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							stroke_fn(130,105,130,125,number);
							l=false;
							ar[21]++;
							ar[22]++;
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							} 
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							stroke_fn(130,135,130,155,number);
							l=false;
							ar[27]++;
							ar[28]++;
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							} 
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							stroke_fn(130,165,130,185,number);
							l=false;
							ar[33]++;
							ar[34]++;
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							} 
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}	
						}
						else
						k=true;	
					}
					else
					if((x>=155) && (x<165) &&( k===true))
					{
						k=false;
						if((y>=15) && (y<35) && (l===true))
						{
							stroke_fn(160,15,160,35,number);
							l=false;
							ar[4]++;
							ar[5]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===true))
						{
							stroke_fn(160,45,160,65,number);
							l=false;
							ar[10]++;
							ar[11]++;
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							stroke_fn(160,75,160,95,number);
							l=false;
							ar[16]++;
							ar[17]++;
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}  
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							stroke_fn(160,105,160,125,number);
							l=false;
							ar[22]++;
							ar[23]++;
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							} 
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							stroke_fn(160,135,160,155,number);
							l=false;
							ar[28]++;
							ar[29]++;
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							} 
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							stroke_fn(160,165,160,185,number);
							l=false;
							ar[34]++;
							ar[35]++;
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							} 
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}	
						}
						else
						k=true;	
					}
					else
					if((x>=185) && (x<195) &&( k===true))
					{
						k=false;
						if((y>=15) && (y<35) && (l===true))
						{
							stroke_fn(190,15,190,35,number);
							l=false;
							ar[5]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else
						if((y>=45) && (y<65) && (l===true))
						{
							stroke_fn(190,45,190,65,number);
							l=false;
							ar[11]++;
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else
						if((y>=75) && (y<95) && (l===true))
						{
							stroke_fn(190,75,190,95,number);
							l=false;
							ar[17]++;
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
						}
						else
						if((y>=105) && (y<125) && (l===true))
						{
							stroke_fn(190,105,190,125,number);
							l=false;
							ar[23]++;
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
						}
						else
						if((y>=135) && (y<155) && (l===true))
						{
							stroke_fn(190,135,190,155,number);
							l=false;
							ar[29]++;
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
						}
						else
						if((y>=165) && (y<185) && (l===true))
						{
							stroke_fn(190,165,190,185,number);
							l=false;
							ar[35]++;
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}	
						}
						else
						k=true;	
					}
					else
					if((y>=5) && (y<15) && (k===true))
					{
						k=false;
						if((x>=15) && (x<35) &&(l===true))
						{
							stroke_fn(15,10,35,10,number);
							l=false;
							ar[0]++;
							if(ar[0]==4)
							{
								fill_fn(10,10,number);
							}
						}
						else
						if((x>=45) && (x<65)&&(l===true))
						{
							stroke_fn(45,10,65,10,number);
							l=false;
							ar[1]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
						}
						else
						if((x>=75) && (x<95)&&(l===true))
						{
							
							stroke_fn(75,10,95,10,number);
							l=false;
							ar[2]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
						}
						else
						if((x>=105) && (x<125)&&(l===true))
						{
							
							stroke_fn(105,10,125,10,number);
							l=false;
							ar[3]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
						}
						else
						if((x>=135) && (x<155)&&(l===true))
						{
							
							stroke_fn(135,10,155,10,number);
							l=false;
							ar[4]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
						}
						else
						if((x>=165) && (x<185)&&(l===true))
						{
							
							stroke_fn(165,10,185,10,number);
							l=false;
							ar[5]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
						}
						else
						k=true;

					}
					else
					if((y>=35) &&(y<45)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,40,35,40,number);
							l=false;
							ar[0]++;
							ar[6]++;
							if(ar[0]==4)
							{
								fill_fn(10,10,number);
							}
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
							stroke_fn(45,40,65,40,number);
							l=false;
							ar[1]++;
							ar[7]++;
							if(ar[1]==4)
							{
								fill_fn(40,10,number);
							}
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
							stroke_fn(75,40,95,40,number);
							l=false;
							ar[2]++;
							ar[8]++;
							if(ar[2]==4)
							{
								fill_fn(70,10,number);
							}
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
						}
						else
						if((x>=105) && (x<125) &&(l===true))
						{
							stroke_fn(105,40,125,40,number);
							l=false;
							ar[3]++;
							ar[9]++;
							if(ar[3]==4)
							{
								fill_fn(100,10,number);
							}
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
						}
						else
						if((x>=135) && (x<155) &&(l===true))
						{
							stroke_fn(135,40,155,40,number);
							l=false;
							ar[4]++;
							ar[10]++;
							if(ar[4]==4)
							{
								fill_fn(130,10,number);
							}
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
						}
						else
						if((x>165) && (x<185) &&(l===true))
						{
							stroke_fn(165,40,185,40,number);
							l=false;
							ar[5]++;
							ar[11]++;
							if(ar[5]==4)
							{
								fill_fn(160,10,number);
							}
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
						}
						else 
						k=true;
						
					}
					else
					if((y>=65)&&(y<75)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,70,35,70,number);
							l=false;
							ar[6]++;
							ar[12]++;
							if(ar[6]==4)
							{
								fill_fn(10,40,number);
							}
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
						
							stroke_fn(45,70,65,70,number);
							l=false;	
							ar[7]++;
							ar[13]++;
							if(ar[7]==4)
							{
								fill_fn(40,40,number);
							}
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
						
							stroke_fn(75,70,95,70,number);
							l=false;	
							ar[8]++;
							ar[14]++;
							if(ar[8]==4)
							{
								fill_fn(70,40,number);
							}
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===true))
						{
						
							stroke_fn(105,70,125,70,number);
							l=false;	
							ar[9]++;
							ar[15]++;
							if(ar[9]==4)
							{
								fill_fn(100,40,number);
							}
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
							
						}
						else
						if((x>135) && (x<155) &&(l===true))
						{
						
							stroke_fn(135,70,155,70,number);
							l=false;	
							ar[10]++;
							ar[16]++;
							if(ar[10]==4)
							{
								fill_fn(130,40,number);
							}
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
							
						}
						else
						if((x>165) && (x<185) &&(l===true))
						{
						
							stroke_fn(165,70,185,70,number);
							l=false;	
							ar[11]++;
							ar[17]++;
							if(ar[11]==4)
							{
								fill_fn(160,40,number);
							}
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
							
						}
						else
						k=true;

					}
					else
					if((y>=95)&&(y<105)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,100,35,100,number);
							l=false;
							ar[12]++;
							ar[18]++;
							if(ar[12]==4)
							{
								fill_fn(10,70,number);
							}
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
						
							stroke_fn(45,100,65,100,number);
							l=false;	
							ar[13]++;
							ar[19]++;
							if(ar[13]==4)
							{
								fill_fn(40,70,number);
							}
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
						
							stroke_fn(75,100,95,100,number);
							l=false;	
							ar[14]++;
							ar[20]++;
							if(ar[14]==4)
							{
								fill_fn(70,70,number);
							}
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===true))
						{
						
							stroke_fn(105,100,125,100,number);
							l=false;	
							ar[15]++;
							ar[21]++;
							if(ar[15]==4)
							{
								fill_fn(100,70,number);
							}
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===true))
						{
						
							stroke_fn(135,100,155,100,number);
							l=false;	
							ar[16]++;
							ar[22]++;
							if(ar[16]==4)
							{
								fill_fn(130,70,number);
							}
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===true))
						{
						
							stroke_fn(165,100,185,100,number);
							l=false;	
							ar[17]++;
							ar[23]++;
							if(ar[17]==4)
							{
								fill_fn(160,70,number);
							}
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
							
						}
						else
						k=true;

					}
					else
					if((y>=125)&&(y<135)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,130,35,130,number);
							l=false;
							ar[18]++;
							ar[24]++;
							if(ar[18]==4)
							{
								fill_fn(10,100,number);
							}
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
						
							stroke_fn(45,130,65,130,number);
							l=false;	
							ar[19]++;
							ar[25]++;
							if(ar[19]==4)
							{
								fill_fn(40,100,number);
							}
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
						
							stroke_fn(75,130,95,130,number);
							l=false;	
							ar[20]++;
							ar[26]++;
							if(ar[20]==4)
							{
								fill_fn(70,100,number);
							}
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===true))
						{
						
							stroke_fn(105,130,125,130,number);
							l=false;	
							ar[21]++;
							ar[27]++;
							if(ar[21]==4)
							{
								fill_fn(100,100,number);
							}
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===true))
						{
						
							stroke_fn(135,130,155,130,number);
							l=false;	
							ar[22]++;
							ar[28]++;
							if(ar[22]==4)
							{
								fill_fn(130,100,number);
							}
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===true))
						{
						
							stroke_fn(165,130,185,130,number);
							l=false;	
							ar[23]++;
							ar[29]++;
							if(ar[23]==4)
							{
								fill_fn(160,100,number);
							}
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
							
						}
						else
						k=true;

					}
					else
					if((y>=155)&&(y<165)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,160,35,160,number);
							l=false;
							ar[24]++;
							ar[30]++;
							if(ar[24]==4)
							{
								fill_fn(10,130,number);
							}
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
						
							stroke_fn(45,160,65,160,number);
							l=false;	
							ar[25]++;
							ar[31]++;
							if(ar[25]==4)
							{
								fill_fn(40,130,number);
							}
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
						
							stroke_fn(75,160,95,160,number);
							l=false;	
							ar[26]++;
							ar[32]++;
							if(ar[26]==4)
							{
								fill_fn(70,130,number);
							}
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						if((x>=105) && (x<125) &&(l===true))
						{
						
							stroke_fn(105,160,125,160,number);
							l=false;	
							ar[27]++;
							ar[33]++;
							if(ar[27]==4)
							{
								fill_fn(100,130,number);
							}
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===true))
						{
						
							stroke_fn(135,160,155,160,number);
							l=false;	
							ar[28]++;
							ar[34]++;
							if(ar[28]==4)
							{
								fill_fn(130,130,number);
							}
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===true))
						{
						
							stroke_fn(165,160,185,160,number);
							l=false;	
							ar[29]++;
							ar[35]++;
							if(ar[29]==4)
							{
								fill_fn(160,130,number);
							}
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}
							
						}
						else
						k=true;

					}
					else
					if((y>=185)&&(y<195)&&(k===true))
					{
						k=false;
						if((x>=15) && (x<35)&&(l===true))
						{
							
							stroke_fn(15,190,35,190,number);
							l=false;
							ar[30]++;
							if(ar[30]==4)
							{
								fill_fn(10,160,number);
							}
							
							
						}
						else
						if((x>=45) && (x<65) &&(l===true))
						{
						
							stroke_fn(45,190,65,190,number);
							l=false;	
							ar[31]++;
							if(ar[31]==4)
							{
								fill_fn(40,160,number);
							}
							
						}
						else
						if((x>=75) && (x<95) &&(l===true))
						{
						
							stroke_fn(75,190,95,190,number);
							l=false;	
							ar[32]++;
							if(ar[32]==4)
							{
								fill_fn(70,160,number);
							}
							
						}
						else
						if((x>105) && (x<125) &&(l===true))
						{
						
							stroke_fn(105,190,125,190,number);
							l=false;	
							ar[33]++;
							if(ar[33]==4)
							{
								fill_fn(100,160,number);
							}
							
						}
						else
						if((x>=135) && (x<155) &&(l===true))
						{
						
							stroke_fn(135,190,155,190,number);
							l=false;	
							ar[34]++;
							if(ar[34]==4)
							{
								fill_fn(130,160,number);
							}
							
						}
						else
						if((x>=165) && (x<185) &&(l===true))
						{
							stroke_fn(165,190,185,190,number);
							l=false;	
							ar[35]++;
							if(ar[35]==4)
							{
								fill_fn(160,160,number);
							}
							
						}
						else
						k=true;
					}
				}
		}
}
</script>

</body>
</html>

