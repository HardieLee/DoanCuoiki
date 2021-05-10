# DoanCuoiki

###### Nhập thông tin khách hàng:
while True:
    mks = int(input("Nhập mã số khách hàng: "))
    name = input("Mời Nhập tên: ") # nhập tên khách hàng 
    diachi = str(input("Nhập địa chỉ khách hàng: "))
    while True:
            sdt = input("Nhập Số Điện Thoại: ") # nhập số điện thoại
            if (len(sdt) > 10 or len(sdt) < 10):#nếu độ dài của n > 9 hoặc < 9
                print("---Vui lòng nhập lại---") # yêu cầu nhập lại
            else:
                print(f"Số Điện Thoại:{sdt}") # xuất ra số điện thoại
                break # kết thúc vòng lập while
    n = name.split(' ') # tạo khoảng cách cho từng phần của tên
    for i in range(len(n)): # cho i chạy trong độ dài của n
        if(not (n[i].isalpha()) or (n[i].isdigit())): # điều kiện không phải là số hoặc kí tự đặc biệt 
            print("Hãy nhập lại!!!!!") # yêu cầu nhập lại
            break # kết thúc vòng lặp 
    else: 
        print("Họ và tên khách  hàng: ", ' '.join(n))
        break #kết thúc vòng lập while
print("==> Mã số khách hàng: ",mks)
print("==> Địa chỉ khách hàng: ",diachi)
print("==> Số điện thoại khách hàng: ",sdt)
#----------------------------------------------*HIEUPC*---------------------------------------------------
#số kw đã tiêu thụ:
tieu_thu = int
csc = int(input("--- Mời nhập chỉ số cũ: "))
while csc<0:
    print("-Lưu ý: Số nhập vào phải là số nguyên và lớn hơn không!-")
    print("---vui lòng nhập lại!---")
    csc = int(input("--- Nhập chỉ số cũ: "))
else:
    csm = int(input("--- Nhập chỉ số mới: "))
    if csm<0:
        print("Vui lòng nhập lại số nguyên lớn hơn 0!!!!")  
        csm = int(input("--- Nhập chỉ số mới: "))
    else:    
        tieuthu = abs(csm-csc)
        print("==>",name,"tiêu thụ khoảng",format(tieuthu,","),"kw")
#-------------------------------------------------*HIEUPC*------------------------------------------------
#số tiền tạm tính:
I= 1500; II= 1800; III= 2000; IV= 2500; V= 3500
tamtinh = int
if (tieuthu<=30):
    print("==>Số kw tiêu thụ là: ",format(tieuthu,","),"kw thuộc định mức I")
    tamtinh= tieuthu*I
    print("==>Số tiền tạm tính: ",format(tamtinh,","),"đồng")
else:
    if (30<tieuthu<=50):
        print("==>Số kw tiêu thụ là: ",format(tieuthu,","),"kw thuộc định mức II")
        tamtinh= tieuthu*II
        print("==>Số tiền phải trả: ",format(tamtinh,","),"đồng")
    else:
        if (50<tieuthu<=100):
            print("==>Số kw tiêu thụ là: ",format(tieuthu,","),"kw thuộc định mức III")
            tamtinh= tieuthu*III
            print("==>Số tiền phải trả: ",format(tamtinh,","),"đồng")
        else:
            if (100<tieuthu<=150):
                print("==>Số kw tiêu thụ là: ",format(tieuthu,","),"kw thuộc định mức IV")
                tamtinh= tieuthu*IV
                print("==>Số tiền phải trả: ",format(tamtinh,","),"đồng")
            else:
                print("==>Số kw tiêu thụ là: ",format(tieuthu,","),"kw thuộc định mức V")
                tamtinh= tieuthu*V
                print("==>Số tiền phải trả: ",format(tamtinh,","),"đồng")                                                             
#---------------------------------------------*HIEUPC*-------------------------------------------------                                
#số tiền thêm trả kèm theo phụ phí(nếu có):
if tamtinh > 300000:
    phaitra = tamtinh+tamtinh*0.3
    print("==>Số tiền phải trả khi có phụ phí là: ",format(phaitra,","),"đồng")  
else:
    print("==>Số tiền phải trả khi có phụ phí là:",format(tamtinh,","),"đồng")
    if tamtinh > 500000:
        phaitra = tamtinh+tamtinh*0.8
        print("==>Số tiền phải trả khi có phụ phí là:",format(phaitra,","),"đồng")
    else:
        if tamtinh > 1000000:
            phaitra = tamtinh+tamtinh*1.1
            print("==>Số tiền phải trả khi có phụ phí là:",format(phaitra,","),"đồng")
