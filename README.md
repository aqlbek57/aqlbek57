def foydalanuvchi_info(ism, familiya, tugilgan_yili, email_manzili='', tel_raqami=''):
    if email_manzili and tel_raqami:
        foydalanuvchi = f"{ism} {familiya} {tugilgan_yili} {email_manzili} {tel_raqami}"
    else:
        foydalanuvchi = f"{ism} {familiya} {tugilgan_yili}"
    return foydalanuvchi.title()
foydalanuvchi1 = foydalanuvchi_info('abbos', 'usmonov' , '2005-yil', 'abbosusmonov5707@gmail.com', '906108009')
foydalanuvchi2 = foydalanuvchi_info('isfandiyor', 'risqimboyev' , '2005-yil', ) #telefon va electron manzili kiritilmadi
print(f"Foydalanuvchi haqida ma'lumotlar: {foydalanuvchi1} va {foydalanuvchi2}")
print("Saytimizda foydalanuvchilarni ma'lumotlari ro'yxatini shaklantiramiz.")
malumotlar =[]
while True:
    print(end='')
    ism=input("Ismingiz kiriting!!! \n")
    familiya = input("Familiyangiz kiriting!!! \n")
    tugilgan_yil = input("Tug'ilgan yilingiz kiriting!!! \n")
    e_manzil = input("Electron manzilingizni kiriting!!! \n")
    tel_nomer = input("Telefon raqamingizni kiriting!!! \n")
    malumotlar.append(foydalanuvchi_info(ism, familiya, tugilgan_yil, e_manzil, tel_nomer))
    javob = input("Izoh yozib qoldirishni hohlaysizmi? (ha/yoq):")
    if javob == 'yoq':
        break
 
 
