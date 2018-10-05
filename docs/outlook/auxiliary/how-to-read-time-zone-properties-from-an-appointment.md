---
title: 予定からタイム ゾーンのプロパティを読み取る
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ba1b9425-6c16-cab2-da0a-a21734118098
description: このトピックでは、ReadTimeZones、BinToTZDEFINITION と BinToTZREG、予定表で、PidLidAppointmentTimeZoneDefinitionStartDisplay と PidLidTimeZoneStruct、タイム ゾーンのプロパティを読み取ることの 2 つの関数を呼び出す関数を示します。
ms.openlocfilehash: 67755ba49c5572005c6138e34329491148a199a1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396037"
---
# <a name="read-time-zone-properties-from-an-appointment"></a>予定からタイム ゾーンのプロパティを読み取る

このトピックで説明する関数では、 `ReadTimeZones`、2 つの関数を呼び出す`BinToTZDEFINITION`と`BinToTZREG`、予定表で、 [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)と[PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)、タイム ゾーンのプロパティを読み取ることです。
  
**PidLidAppointmentTimeZoneDefinitionStartDisplay**には、 [TZDEFINITION](tzdefinition.md)構造体の保存形式に対応するストリームが含まれていて、 **PidLidTimeZoneStruct**にはの[TZREG](tzreg.md)の保存形式に対応するストリームが含まれています。構造体です。 正確な**TZDEFINITION**と**TZREG**の構造を取得するのには`BinToTZDEFINITION`と`BinToTZREG`これらのプロパティのストリームの値を適切に解析するために使用します。 これら 2 つの関数は、それぞれの[TZDEFINITION 構造体を読み取るためのバイナリのプロパティからのストリームを解析](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)し、 [TZREG 構造体を読み取るためのバイナリのプロパティからのストリームの解析](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)をで定義されます。 
  
```cpp
void ReadTimeZones(LPMAPIPROP lpAppointment) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID[2] = {0}; 
    LPMAPINAMEID lpNamedID[2]; 
    lpNamedID[0] = &amp;NamedID[0]; 
    lpNamedID[1] = &amp;NamedID[1]; 
    NamedID[0].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[0].ulKind = MNID_ID; 
    NamedID[0].Kind.lID = dispidTimeZoneStruct; 
    NamedID[1].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[1].ulKind = MNID_ID; 
    NamedID[1].Kind.lID = dispidApptTZDefStartDisplay; 
    hRes = lpAppointment->GetIDsFromNames( 
        2, 
        lpNamedID, 
        NULL, 
        &amp;lpNamedPropTags); 
    if (SUCCEEDED(hRes) &amp;&amp; lpNamedPropTags) 
    { 
        SizedSPropTagArray(2,sptaTzProps) = {2, 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_BINARY), 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[1],PT_BINARY), 
        }; 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
        hRes = lpAppointment->GetProps( 
            (LPSPropTagArray)&amp;sptaTzProps, 
            NULL, 
            &amp;cProps, 
            &amp;lpProps); 
        if (SUCCEEDED(hRes) &amp;&amp; 2 == cProps &amp;&amp; lpProps) 
        { 
            if (PT_BINARY == PROP_TYPE(lpProps[0].ulPropTag)) 
            { 
                TZREG* ptzReg = BinToTZREG(lpProps[0].Value.bin.cb,lpProps[0].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzReg. 
                delete ptzReg; 
            } 
            if (PT_BINARY == PROP_TYPE(lpProps[1].ulPropTag)) 
            { 
                TZDEFINITION* ptzDef = BinToTZDEFINITION(lpProps[1].Value.bin.cb,lpProps[1].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzDef. 
                delete[] ptzDef; 
            } 
           } 
        MAPIFreeBuffer(lpProps); 
    } 
    MAPIFreeBuffer(lpNamedPropTags); 
}
```

## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

