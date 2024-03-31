# Huawei Cloud Resource

## ECS   
### Virtual manchine   
   Region: เลือก AP-Bangkok  
   Billing Mode: 
   - Yearly/Montly: เป็น Commit usage กรณีที่ลบ Instance ก่อนถึงกำหนดปีหรือเดือนยังได้รับเงินคืน(ไม่เหมือน Cloud เจ้าอื่นๆ)
   - Pay-per-use: ใช้เท่าไหร่จ่ายเท่านั้นคิดเป็น /ชั่วโมง
   - Spot pricing: คิดเงินตามการใช้งานจริงเป็นรายชั่วโมง ราคาจะไม่คงที่ขึ้นอยู่กับความนิยมในแต่ละ Flavor(รุ่น) คำนวณ cost ยาก และจะโดน terminate เมื่อไหร่ก็ได้ มี 2 แบบ
      1. Spot price คือ การกำหนดราคาสูงสุดที่รับได้โดยเงื่อนไขคือถ้าเกินราคาที่ตั้งไว้จะเกิดการ terminate VMs ทันที
		1.1 Automatic กำหนดราคาที่รับได้ให้เท่ากับราคาตลาด(market price) ของราคา Pay-per-use
		1.2 manual กำหนดราคาที่รับได้เอง เช่น 0.11$/hour
      2. Spot block คือ กำหนดเป็นช่วงเวลาที่ VMs instance จะอยู่(สูงสุดได้ 6 ชั่วโมง) ถ้าเกินจากนั้นจะเกิดการ terminate VMs ทันที

   Instance Selection:  
   - CPU Architecture : เลือก X86
   -    
## EIP   
### Public IP
