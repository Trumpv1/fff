function click() local function fiximage(id) return string.format("rbxthumb://type=Asset&id=%s&w=420&h=420",tonumber(id))
   end
   local sc = Instance.new("ScreenGui",game.CoreGui) sc.DisplayOrder = 10000 sc.IgnoreGuiInset = true local img = Instance.new("ImageLabel",sc) img.Size = UDim2.new(1,0,1,0) img.Image = fiximage(7221675410) img.ScaleType = "Fit"
   img.BackgroundColor3 = Color3.fromRGB(0,0,0)
   local auegh = Instance.new("Sound",game)
   auegh.Volume = 3
   auegh.SoundId = "rbxassetid://7221658223"
   auegh:Play()
   auegh.Ended:Connect(function()
       wait()
       auegh:Destroy()
   end)
   game:GetService("TweenService"):Create(img,TweenInfo.new(3),{BackgroundTransparency = 1,ImageTransparency = 1}):Play()
   delay(3,function()
       sc:Destroy()
   end)
end

while wait() do
   if math.random(1,2) == 1 then
       click()
   end
end
