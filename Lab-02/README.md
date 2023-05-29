# LAB-02
# Основы проектирования сети
### Цели
- Настроить OSPF для Underlay сети.
### Схема сети
![pic_01.jpg](pic_01.jpg)
### Настройка оборудования
 <details>
<summary>  Настройка Spine-01: </summary>

```
hostname Spine-01

interface Ethernet1/1
  no switchport
  ip address 10.2.1.0/31
  no shutdown

interface Ethernet1/2
  no switchport
  ip address 10.2.1.2/31
  no shutdown

interface Ethernet1/3
  no switchport
  ip address 10.2.1.4/31
  no shutdown

interface loopback1
  ip address 10.0.1.0/32
```
</details>
 <details>
<summary>  Настройка Spine-02: </summary>

```
hostname Spine-02

interface Ethernet1/1
  no switchport
  ip address 10.2.2.0/31
  no shutdown

interface Ethernet1/2
  no switchport
  ip address 10.2.2.2/31
  no shutdown

interface Ethernet1/3
  no switchport
  ip address 10.2.2.4/31
  no shutdown

interface loopback1
  ip address 10.0.2.0/32
```
</details>
 <details>
<summary>  Настройка Leaf-01: </summary>

```
hostname Leaf-01

interface Ethernet1/1
  no switchport
  ip address 10.2.1.1/31
  no shutdown

interface Ethernet1/2
  no switchport
  ip address 10.2.2.1/31
  no shutdown

interface loopback1
  ip address 10.1.1.1/32
```
</details>
 <details>
<summary>  Настройка Leaf-02: </summary>

```
hostname Leaf-02

interface Ethernet1/1
  no switchport
  ip address 10.2.1.3/31
  no shutdown

interface Ethernet1/2
  no switchport
  ip address 10.2.2.3/31
  no shutdown

interface loopback1
  ip address 10.1.1.2/32
```
</details>
 <details>
<summary>  Настройка Leaf-03: </summary>

```
hostname Leaf-03

interface Ethernet1/1
  no switchport
  ip address 10.2.1.5/31
  no shutdown

interface Ethernet1/2
  no switchport
  ip address 10.2.2.5/31
  no shutdown

interface loopback1
  ip address 10.1.1.3/32
```
</details>
