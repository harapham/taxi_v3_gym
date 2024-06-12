Giải bài toán xe taxi tự hành theo mô tả như sau:
Môi trường là Taxi-v3 trong thư viện gym (env = gym.make("Taxi-v3").env). Vị trí taxi và vị trí hành khách sẽ được khởi tạo ngẫu nhiên. Yêu cầu là tối ưu reward nhận được (cách tính reward như trong mô tả sau: https://www.gymlibrary.dev/environments/toy_text/taxi/).

kết quả một function tên là strategy nhận đầu vào là các biến theo thứ tự sau:
1. Vị trí của xe taxi (1 trong 25 vị trí trong bản đồ 5x5 của taxi-v3)
2. Vị trí của hành khách (1 trong 4 điểm R, G, B, Y trong bản đồ)
3. Vị trí trả khách (Destination: 1 trong 4 điểm R, G, B, Y trong bản đồ)
Đầu ra của function này là list các action có thể, bao gồm:
0 = south
1 = north
2 = east
3 = west
4 = pickup
5 = dropoff
Các action này cách nhau bởi dấu phẩy.

Ví dụ: strategy(3,1,R,Y) trả về 1,1,1,2,0,0,0. Trong đó, vị trí taxi là ở ô (3,1), đón khách ở ô R và trả khách ở ô Y.
