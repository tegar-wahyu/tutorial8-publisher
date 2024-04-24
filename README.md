# Module 8 - Publisher
## Reflection
**a. How many data your publisher program will send to the message broker in one run?**
> Publisher akan mengirim 5 data ke message broker dalam one run. Hal ini berdasarkan 5 panggilan ke `publish_event` dalam main function di `src/main.rs`. Setiap panggilan akan mengirim `UserCreatedEventMessage` ke message broker.

**b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?**
> URL `amqp://guest:guest@localhost:5672` adalah connection string untuk message broker. Karena connection string pada publisher dan subscriber sama, hal ini berarti keduanya terhubung ke message broker yang sama. Hal ini memungkinkan publisher untuk mengirim message ke broker, dan subscriber untuk menerima message tersebut dari broker.