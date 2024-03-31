# Huawei Cloud Resource

## ECS   
### Virtual manchine   
   Region: ภูมิภาคทีต้องการให้ ECS resouce อยุ่ เลือกตาม target user เพื่อให้เกิด low latency และ access resouce ที่รวดเร็ว เช่นกลุ่มผู้ใช้งานอยู่ในไทยก็เลือกเป็น AP-Bangkok 
   
   Billing Mode: 
   - Yearly/Montly: เป็น Commit usage กรณีที่ลบ Instance ก่อนถึงกำหนดปีหรือเดือนยังได้รับเงินคืน(ไม่เหมือน Cloud เจ้าอื่นๆ)
   - Pay-per-use: ใช้เท่าไหร่จ่ายเท่านั้นคิดเป็น /ชั่วโมง
   - Spot pricing: คิดเงินตามการใช้งานจริงเป็นรายชั่วโมง ราคาจะไม่คงที่ขึ้นอยู่กับความนิยมในแต่ละ Flavor(รุ่น) คำนวณ cost ยาก และจะโดน terminate เมื่อไหร่ก็ได้ มี 2 แบบ
      1. Spot price คือ การกำหนดราคาสูงสุดที่รับได้โดยเงื่อนไขคือถ้าเกินราคาที่ตั้งไว้จะเกิดการ terminate VMs ทันที
		1.1 Automatic กำหนดราคาที่รับได้ให้เท่ากับราคาตลาด(market price) ของราคา Pay-per-use
		1.2 manual กำหนดราคาที่รับได้เอง เช่น 0.11$/hour
      2. Spot block คือ กำหนดเป็นช่วงเวลาที่ VMs instance จะอยู่(สูงสุดได้ 6 ชั่วโมง) ถ้าเกินจากนั้นจะเกิดการ terminate VMs ทันที
   
   AZ: Availability zones คือ กลุ่มของ Data center ที่ถูกออกแบบให้แยกออกจากกันในแง่ของความเสี่ยงในการล้มเหลว ทั้งในเรื่องแหล่งสาธารณูปโภค (น้ำ, ไฟ, ฯลฯ) ความเสี่ยงด้านภัยธรรมชาติ ในแต่ละ Region จะต้องมีอย่างน้อย 2 Availability Zones ให้บริการ เช่น Region AP-Bangkok จะมี 3 Availability Zones คือ NTT นิคมอุตสาหกรรมอมตะซิตี้ ชลบุรี (AZ1), TRUE IDC บางนา(AZ2), ระยอง(AZ3) https://developer.huaweicloud.com/intl/en-us/endpoint   

   Instance Selection:  
   - CPU Architecture : เลือก X86
   -    
## EIP   
### Public IP


DC-บางนา(AZ1) และ DR-อมตะ(AZ2)