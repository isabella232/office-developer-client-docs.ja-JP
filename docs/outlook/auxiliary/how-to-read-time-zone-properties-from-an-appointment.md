---
title: 予定からタイム ゾーンのプロパティを読み取る
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ba1b9425-6c16-cab2-da0a-a21734118098
description: このトピックでは、2つの関数を呼び出して、PidLidAppointmentTimeZoneDefinitionStartDisplay と PidLidTimeZoneStruct のタイムゾーンプロパティの読み取りを予定から読み込む関数である readtimezones ゾーンを示します。
ms.openlocfilehash: 67755ba49c5572005c6138e34329491148a199a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317620"
---
# <a name="read-time-zone-properties-from-an-appointment"></a><span data-ttu-id="72bb2-103">予定からタイム ゾーンのプロパティを読み取る</span><span class="sxs-lookup"><span data-stu-id="72bb2-103">Read time zone properties from an appointment</span></span>

<span data-ttu-id="72bb2-104">このトピックでは、2 `ReadTimeZones` `BinToTZDEFINITION`つの`BinToTZREG`関数を呼び出し、予定からタイムゾーンのプロパティ[PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx)と[PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)を読み取る関数を示します。</span><span class="sxs-lookup"><span data-stu-id="72bb2-104">This topic shows a function,  `ReadTimeZones`, that calls the two functions,  `BinToTZDEFINITION` and  `BinToTZREG`, to read the time zone properties, [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) and [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx), from an appointment.</span></span>
  
<span data-ttu-id="72bb2-105">**PidLidAppointmentTimeZoneDefinitionStartDisplay**には、 [TZDEFINITION](tzdefinition.md)構造の永続化された形式にマップするストリームが含まれています。 **PidLidTimeZoneStruct**には、 [TZREG](tzreg.md)の永続化された形式にマップされるストリームが含まれています。造.</span><span class="sxs-lookup"><span data-stu-id="72bb2-105">**PidLidAppointmentTimeZoneDefinitionStartDisplay** contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure, and **PidLidTimeZoneStruct** contains a stream that maps to the persisted format of a [TZREG](tzreg.md) structure.</span></span> <span data-ttu-id="72bb2-106">正確な**TZDEFINITION**および**TZREG**構造`BinToTZDEFINITION`を取得するため`BinToTZREG`に、これらのプロパティのストリーム値を適切に解析するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72bb2-106">To obtain the exact **TZDEFINITION** and **TZREG** structures,  `BinToTZDEFINITION` and  `BinToTZREG` are used to parse the stream values of these properties appropriately.</span></span> <span data-ttu-id="72bb2-107">この2つの関数は、[バイナリプロパティからのストリームを解析して、TZDEFINITION 構造体を読み取り](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)、[バイナリプロパティからのストリームを解析](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)し、それぞれ TZREG 構造を読み取るように定義されています。</span><span class="sxs-lookup"><span data-stu-id="72bb2-107">These two functions are defined in [Parse a stream from a binary property to read the TZDEFINITION structure](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md) and [Parse a stream from a binary property to read the TZREG structure](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md), respectively.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="72bb2-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="72bb2-108">See also</span></span>

- [<span data-ttu-id="72bb2-109">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="72bb2-109">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

