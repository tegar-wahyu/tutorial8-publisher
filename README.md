# Module 8 - Publisher
## Reflection
### a. How many data your publisher program will send to the message broker in one run?
> Publisher akan mengirim 5 data ke message broker dalam one run. Hal ini berdasarkan 5 panggilan ke `publish_event` dalam main function di `src/main.rs`. Setiap panggilan akan mengirim `UserCreatedEventMessage` ke message broker.

### b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
> URL `amqp://guest:guest@localhost:5672` adalah connection string untuk message broker. Karena connection string pada publisher dan subscriber sama, hal ini berarti keduanya terhubung ke message broker yang sama. Hal ini memungkinkan publisher untuk mengirim message ke broker, dan subscriber untuk menerima message tersebut dari broker.

### Running RabbitMQ as message broker.
![alt text](images/InitialRabbitMQ.png)

### Sending and processing event.
![alt text](images/Sending&Processing.png)

### Monitoring chart based on publisher.
![alt text](images/MonitorChart.png)
> Jika dijalankan cargo run berkali-kali dalam satu detik, maka laju "Publish" akan meningkat pada periode tersebut seperti yang ditunjukkan oleh puncak-puncak pada grafik.
>
> Sebaliknya, jika dijalankan cargo run sekali dalam satu detik, maka laju "Publish" akan lebih rendah pada periode tersebut, seperti yang ditunjukkan oleh lembah-lembah pada grafik.
>
>Hal ini menunjukkan bahwa message rates yang diterima oleh message broker RabbitMQ akan meningkat seiring dengan meningkatnya jumlah pesan yang di-publish oleh publisher dalam satu periode waktu tertentu. Semakin banyak pesan yang diterbitkan dalam satu detik, semakin tinggi laju pesan yang ditunjukkan pada grafik.