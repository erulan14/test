# Тестовое задание

## Практические задачи

Стеки технологии которые нужны quasar, leaflet, google-polyline, axios

1. Задача
Сделать компонент где можно выбрать интервал (от и до с датой и времени) интервал должен быть разделен

пример на фото 

![изображение](https://github.com/erulan14/test_nurdaulet/assets/42293127/5245d591-7a8e-4348-8a4e-c84009f3ea22)


поосле выбора интервала нужно сделать кнопку где будет выполнен GET запрос на api для получение отчета о поездки, 
ссылка на api: https://glot.kz/report/{id}/

id для теста можете написать 43

**параметры запроса**

- type – 1
- from – вермя в секнудах (начало интервала)
- to – время в секундах (конец интервала)
  
**для авторизации нужно получить токен пользователья его вам позже скинуть**

получаете данные и распределяете по таблице как на примере фото 
![изображение](https://github.com/erulan14/test_nurdaulet/assets/42293127/0e3c0ddc-8c72-4a7b-8703-c5c1361743c8)

Для демонстрации работы компонента необходимо сделать простую HTML страницу.

**Формат данных от сервера**

Сервер возвращает JSON-массив данных.
Пример данных: 

```js
{
  "schema": {
    "fields": [
      {
        "name": "Дата",
        "type": "string"
      },
      {
        "name": "Пробег, км.",
        "type": "number"
      },
      {
        "name": "Общий расход топлива, л.",
        "type": "number"
      },
      {
        "name": "Моточасы, ч/м",
        "type": "string"
      },
      {
        "name": "Средний скорость",
        "type": "number"
      },
      {
        "name": "Расход на 100км,л",
        "type": "number"
      },
      {
        "name": "потребление л/ч",
        "type": "number"
      }
    ],
    "pandas_version": "1.4.0"
  },
  "data": [
    {
      "Дата": "10.08.2023, 08:16:03",
      "Пробег, км.": 10.79,
      "Общий расход топлива, л.": 0,
      "Моточасы, ч/м": "00ч27м",
      "Средний скорость": 28,
      "Расход на 100км,л": 0,
      "потребление л/ч": 0
    },
    {
      "Дата": "10.08.2023, 11:39:55",
      "Пробег, км.": 8.58,
      "Общий расход топлива, л.": 0,
      "Моточасы, ч/м": "00ч25м",
      "Средний скорость": 29,
      "Расход на 100км,л": 0,
      "потребление л/ч": 0
    },
    {
      "Дата": "10.08.2023, 12:13:37",
      "Пробег, км.": 12.89,
      "Общий расход топлива, л.": 0,
      "Моточасы, ч/м": "01ч20м",
      "Средний скорость": 23,
      "Расход на 100км,л": 0,
      "потребление л/ч": 0
    },
    {
      "Дата": "10.08.2023, 13:57:06",
      "Пробег, км.": 3.16,
      "Общий расход топлива, л.": 0,
      "Моточасы, ч/м": "00ч13м",
      "Средний скорость": 25,
      "Расход на 100км,л": 0,
      "потребление л/ч": 0
    },
    {
      "Дата": null,
      "Пробег, км.": 35.42,
      "Общий расход топлива, л.": 0,
      "Моточасы, ч/м": "0д2ч26м",
      "Средний скорость": 26,
      "Расход на 100км,л": 0,
      "потребление л/ч": 0
    }
  ]
}
```

2. Задача
Если выполнили 1 задание, в таблице нужно сделать кнопку для показа поездки на карте.
Нужно получить по нажатием кнопки координаты поездки по api 
ссылка на api: https://glot.kz/route/{id}/

**параметры запроса**
- from – вермя в секнудах (начало интервала)
- to – время в секундах (конец интервала)

**для авторизации нужно получить токен пользователья его вам позже скинуть**

**Формат данных от сервера**

Сервер возвращает JSON-массив данных.
Пример данных: 

```js
"wm_hLejmaG??????????????WC??f@KDCDCHAn@Mh@?BE?GIYQg@gAoDIYIQ??CIGOIc@BGNEd@GtAS|YeEfGw@vC]LERC@?J?lAQJ@FDFJR^f@zApAdEfApDTv@fArD~ArDPp@HNB@BD~OMjFy@pFu@hD_@zEw@lB_@`IkANE`@GxAWPEj@Il@MxB[D@PBLFJLfFvN|A~DrAbEr@~BT|@HRPj@bAbDnAzDpAtDhAxDlAnDZhBXp@Vd@Vd@bArDTn@j@`B~@xC~GrSlAtDlA`DRl@L\\BDZd@HAj@IfC_@bDi@dBSXGZGHGFCHCj@I~@KnFq@hG_AfBYtSwCfF}@|@K`AM`AIn@KLEnAy@EOSi@a@yAiAuDwA{DjBkIr@Mp@Kd@KVCp@M~AYnJmAPAVEz@OpBWzDe@\\FzCr@dAVpB`@xBn@`GrAtGxA`@JJFD@FF\\Hr@L~@R`FnAxAR~@ZZFFBHBb@LH?fBaE@EBGXq@t@eBBGKEMCmAWiAMsN|@k@jAINA@}HQ{FqAkAYc@GSEEAQAg@Ow@UoQmAqARGDM?C?EEEEEIM]u@sCqA{DqFcPwAgDqAwDqAsC_@iA}BsHM[Se@gAkCu@}Ae@}@a@yAcEeQMc@IQNmCv@I|F}@~@OJC?CACAEGGIB@B????????CQ??J`@??F???LA??f@K??x@O??nB]??rFw@??vDc@??nAU??T@??@D??EF??}]fFeBTWDOBIBOFa@HiCZaG|@oFr@qFx@qEr@{BNa@@mALoEfAaBTs@LOD??EB]DsAPmDl@sFv@gDb@kALu@JQDONQVW^_Pv@gCRo@FKBiBTcADoAJaBTMAO?A?HGIAMBg@JmCb@gEl@wFbAs_@pFiG`A}Fn@yFv@wW`EE@WBaC^qC`@w@LmAR_G`AyFz@eFt@i@HUDE@KBqARwFp@wDj@_FdAc@^q@`AaA|BwApD_BfD{AvDg@dA[`@OXc@x@@AAGyAfEu@tBk@`A]f@cBlDeBvDOZwArDeFtLA@MTMRIHQXENQl@CHIRKVa@n@g@r@_@nAGfARxAhAvCDNL^P^H\\Vz@pArDnArDx@nClAxD`AtCjArDjFpDl@Kx@KxEs@vFw@vLcBjFu@xDg@hBYXIAISe@cA}@??j@n@PbABBFBF?FCd@IlB[LEG@n@KREHK?GGYUg@c@_AFEPAPAhC]??AR?SEKF?f@Gd@CB@D?P?\\ElAQHAt@vBHLP`@Xj@bApDbAfD^jADT?B??jErLlAnDrAvDlA~Ch@bBBFPBJBJDLAt@OhScDZKbBQp@EhBSnFy@hEm@fG{@zFaAbGw@`YeEtF}@pASZEz@IdBS~FeA~@QREXEREVGXC|Cm@fBSxBWlFu@jC]P?ZErFw@RAn@GNFHRP^vA~DnA`DN^?F@JJT^x@LFP@VEjASrD{@xCg@hHqA~Aa@PClE{@PGv@c@l@ObEm@bGYr@Cj@K@AlGaArFk@VAFCDAb@CLC|@MbAYRa@rC}G@G@?HG@GOCAER?K@ATRGEGA@PNe@GAGDD@DBDzBmEJWOMPk@X[ICJ?JSP_@rBoEFWRk@XaAJQFEDGDE\\u@DGDYDIAODK\\[HKJ[dAaCPa@b@cAx@yBhBaErCmG~AsDXq@~@cBjAiCJu@KIS@c@E[Au@KuZmBEEAECMIu@a@uCOYGO_@o@M]i@{AcAsD}AcEoAeEkAuDuAyDk@qASc@EKCMK[kAuCqAgE}B_GaBwDQ_@?O?UKa@]s@Ws@KUKa@{CyL{@iCIQOa@M_@CEO_@Oc@gAyCAAjLsD?E?CAC|@U`AGpBSnFk@jEe@d@IPC@??@yRtCuFx@w@F{@T}A^cAZGHAJ@LHPRd@z@|BlDlNTfBfApB\\l@BNN`@N`@hG~P~@vBBFEFIAEABCRd@jAbCpAjDXp@ZHNElBa@nFm@fFw@rDk@tAOPBd@HbEt@fFtAtCn@TBb@Lx@P|J~BLFVDn@NXNh@RNDfALj@N\\@x@LtFlA~EvA~MbDvCr@VDBA@ABC?C@C?CDOFMB?FA@@LWIAKBH@???@MHORIZQFKASCk@OcFcA}EiAeF{AaBa@cFkARAaAIm@Ee@EkB_@qCm@QEs@SaBg@kFqAUGOGKA[Gm@OaFmAqFqA]Iw@QuAUk@?O@oARuB\\MAIGCKI]Mw@_AqCGQCAG?K@o@L_BVoF|@cAPm@J[F{AFIIQe@k@eBsAuDg@aBgAkD{B{FUq@m@oAa@u@q@aBIe@U_EoAoDeAuBODX@BOMa@KWaAqDB[b@InFg@jCe@TGEU??@?CECEAC"
```

После полуение данных, нужно получить координаты зашифрованные через библиотеку google-polyline
деокодируем коориданты и рисуем на карте линию поездки с использованием библиотеки leaflet

пример на фото

![изображение](https://github.com/erulan14/test_nurdaulet/assets/42293127/c0031af0-6bc5-4ff5-b2ae-5c1ffddf78d1)





