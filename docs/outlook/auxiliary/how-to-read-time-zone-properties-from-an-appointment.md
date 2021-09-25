---
title: 予定からタイム ゾーンのプロパティを読み取る
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: ba1b9425-6c16-cab2-da0a-a21734118098
description: このトピックでは、2 つの関数 BinToTZDEFINITION と BinToTZREG を呼び出して、予定からタイム ゾーン プロパティ PidLidAppointmentTimeZoneDefinitionStartDisplay と PidLidTimeZoneStruct を読み取る関数 ReadTimeZones を示します。
ms.openlocfilehash: 14774f5a565926bda2bdc16e846f3eed3d2002ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605457"
---
# <a name="read-time-zone-properties-from-an-appointment"></a>予定からタイム ゾーンのプロパティを読み取る

このトピックでは、2 つの関数を呼び出す関数と、予定からタイム ゾーン プロパティ  `ReadTimeZones`  `BinToTZDEFINITION`  `BinToTZREG` [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) と [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)を読み取る関数を示します。
  
**PidLidAppointmentTimeZoneDefinitionStartDisplay** には [、TZDEFINITION](tzdefinition.md) 構造体の永続形式にマップされるストリームが含まれています **。PidLidTimeZoneStruct** には [、TZREG](tzreg.md) 構造体の永続化された形式にマップするストリームが含まれています。 正確な **TZDEFINITION** 構造体と **TZREG** 構造体を取得するために、これらのプロパティのストリーム値を適切  `BinToTZDEFINITION`  `BinToTZREG` に解析するために使用されます。 これら 2 つの関数は [、「TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md) 構造体を読み取るバイナリ プロパティからストリームを解析する」および [「TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)構造体を読み取るバイナリ プロパティからストリームを解析する」で定義されています。 
  
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

