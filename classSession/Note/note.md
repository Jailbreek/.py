**Girish Suryanarayana not Fowell**

**Konfigurasi**

**31 32 33 34 35     36 37 38 39 40**

**21 22 23 24 25     26 27 28 29 30**

**11 12 13 14 15     16 17 18 19 20**

**01 02 03 04 05     06 07 08 09 10**

![1688397553879.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2c029e04-6446-4785-b312-a7fe49d2859c/1688397553879.jpg)

![1688397629193.jpg](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29925270-d68c-46eb-a0a5-2980a7ea0ad1/1688397629193.jpg)

### Encapsulation Smell

| Encapsulation smell | Pelanggaran prinsip encapsulation | Penyebab | Martin Fowler smells |
| --- | --- | --- | --- |
| Deficient Encapsulation | Hide implementation details | Adanya akses terhadap member abstraksi, terutama jika access modifier public | Inappropriate Intimacy |
| Leaky Encapsulation | Hide implementation details | - List: Data diperoleh dengan swallow copy bukan deep copy- Penamaan method yang mengandung detail implementasi | Inappropriate Intimacy |
| Missing Encapsulation | Hide variations | a. Tidak ada pembagian Classb. Hierarki bucin alias ada hierarki kembar | Divergent Changes, Parallel Inheritence |
| Unexploited Encapsulation | Hide variations | Penggunaan if-else atau switch statement dalam object type checking | Switch Statements |

### Abstraction Smell

| Abstraction smell | Pelanggaran prinsip abstraction | Penyebab | Martin Fowler smells |
| --- | --- | --- | --- |
| Missing Abstraction | Provide a crisp conceptual boundary and a unique identity | Pemakaian komponen-komponen data/string tanpa membuatkan object class | Primitive Obsession, Data Clumps |
| Imperative Abstraction | Map domain entities | Proses dijadikan class, pemikiran Procedural dalam Object-oriented programming | Lazy Class (Potentially) |
| Incomplete Abstraction | Ensure coherence and completeness | Tidak ada pasang/lawan kata domain | - |
| Multifaceted Abstraction | Assign single and meaningful responsibility | Satu class memegang > 1 tanggungjawab | Divergent Changes + Large Class |
| Unnecessary Abstraction | Assign single and meaningful responsibility | Pembuatan class yang seharusnya tidak diperlukan (alias overengineering) | Speculative Generalities |
| Unutilized Abstraction | Assign single and meaningful responsibility | Ada class yang tidak terpakai sama sekali | Dead Code |
| Duplicate Abstraction | Avoid duplication | Ada method/implementasi yang sama antar class | Alternative Classes with Different Interfaces |

### Hierarchy Smell

| Hierarchy smell | Pelanggaran prinsip hierarchy | Penyebab | Martin Fowler smells |
| --- | --- | --- | --- |
| Missing Hierarchy | Apply meaningful classification | Pemakaian conditional checking untuk menentukan behaviour object yang seharusnya dapat diganti dengan polymorphism | - |
| Unnecessary Hierarchy | Apply meaningful classification | Developer membuatkan subclass hanya karena masalah perbedaan attribute bukan pada perbedaan behaviour | - |
| Unfactored Hierarchy | Apply meaningful generalization | Terdapat duplikat antara sesama saudara subclass atau antar subclass dengan superclass | Duplicate Code (class-to-class) |
| Wide Hierarchy | Apply meaningful generalization | Superclass mempunyai banyak anakan langsung tanpa intermediate class | - |
| Speculative Hierarchy | Apply meaningful generalization | Adanya class yang dibuatkan oleh developer karena alasan spekulatif untuk memenuhi kasus tertentu | Speculative Generalities |
| Deep Hierarchy | Apply meaningful generalization | Pembuatan hierarki terlalu besar dan terlalu dalam subclass levelnya. | - |
| Rebellious Hierarchy | Ensure substitutability | Subclass menolak behaviour dari superclass | Refused Bequest |
| Broken Hierarchy | Ensure substitutability | Hubungan relationship antar superclass dan subclass terputus karena ada pemaksaan hubungan inheritance | Refused Bequest (ISP) |
| Multipath Hierarchy | Avoid redundant paths | Subclass (cucu) mengambil jalan pintas inheritance ke base class | - |
| Cyclic Hierarchy | Ensure proper ordering | Superclass bergantung pada subclass | Feature Envy, Inappropriate Intimacy |

### Modularization Smell

| Modularization smell | Pelanggaran prinsip modularization | Penyebab | Martin Fowler smells |
| --- | --- | --- | --- |
| Broken Modularization | Localize related data and methods | 1. Pemisahan data dan method dalam class terpisah2. Method kecolongan bermain dengan class lain | 1. Data Class2. Feature Envy |
| Insufficient Modularization | Decompose abstractions to manageable size | 1. Class terlalu besar, tidak ada modularization2. Class/method terlalu kompleks | 1. Large class, divergent changes2. Long method |
| Cyclically-dependent Modularization | Create acyclic dependencies | Class saling dependensi satu sama lain dengan pasangannya atau teman selingkarnya | Shotgun Surgery, Feature Envy, Inappropriate Intimacy |
| Hub-like Modularization | Limit dependencies | Class terlalu banyak ketergantungan dari class lain atau dependensi masukan dari class lain | Shotgun Surgery (bisa terjadi pada class yang depend dengannya) |
