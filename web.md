# Easy Web 

![323642908-9661bc22-0bbf-45ca-82dd-138f6b0f9a45](https://github.com/neo-M3tinez/BlackHat-Asia-CTF/assets/174318737/97f7f8fe-3e22-43bb-aba7-f5259f431791)


- với bài này chúng ta đã có gợi ý từ đề bài là flag hidden in web

=> đầu tiên ta sẽ check src của web sau khi lướt 1 hồi thì ta thấy có flag nằm ở comment cuối src code

![323644108-e45c32e8-725d-4ecc-b325-e997ecb5e5f3](https://github.com/neo-M3tinez/BlackHat-Asia-CTF/assets/174318737/719ce5b0-c6da-4dbc-92f8-e4115563a3ab)


=> flag : flag{hidden_in_plain_sight}

# Old But Gold 

- bài này ta có thông tin về launch1.cgi ở phần f12 sau khi search ta biết được đây là lỗ hổng shellshock

gửi request đến url với đường link /cgi-bin/launch1.cgi

![323677624-0a783507-43ab-492a-965d-d738fddd1eef](https://github.com/neo-M3tinez/BlackHat-Asia-CTF/assets/174318737/373b2faa-0b28-4d6a-b0f8-7b2e9a29aba6)


payload của shellshock

```
User-Agent:() { :; }; echo ; echo ; /bin/cat /etc/passwd
```

![323686106-d3f89108-32d0-4e01-86d2-8f8509066a39](https://github.com/neo-M3tinez/BlackHat-Asia-CTF/assets/174318737/d3ec2290-3479-4715-aa62-d05a5c79aa65)



tương tự ta có thể chèn 1 đoạn command reverse shell vào trong đó thì sẽ rev đến local 

dùng netcat với local port and ip 

### tìm cách reverse shell vào web đó qua payload

có thể dùng commix hoặc nc 

![323817202-afe0d27b-a844-4573-850e-8df4f0d9f7f8](https://github.com/neo-M3tinez/BlackHat-Asia-CTF/assets/174318737/c30c4cfd-e293-4466-a552-e2f9e3a473f4)



=> flag: flag{this_was_10_years_ago?} 
