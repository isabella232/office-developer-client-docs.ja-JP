---
title: バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 9e36e0d9-a28b-5978-0e23-f76e1bf506b5
description: このトピックでは、バイナリ プロパティ PidLidTimeZoneStruct に格納されている永続化された形式から TZREG 構造体を読み取る方法を示します。
ms.openlocfilehash: 95f78f2d0ddc24376287f2eaabc2ed0def3395e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596618"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure"></a>バイナリ プロパティからのストリームを解析し、TZREG 構造体を読み取る

このトピックでは、バイナリ プロパティ[PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)に格納されている永続化された形式から[TZREG](tzreg.md)構造体を読み取る方法を示します。
  
```cpp
TZREG* BinToTZREG(ULONG cbReg, LPBYTE lpbReg)  
{ 
    if (!lpbReg) return NULL;  
 
    // Update this if parsing code is changed. 
    if (cbReg &amp;lt; 3*sizeof(long) + 2*sizeof(WORD) + 2*sizeof(SYSTEMTIME)) return NULL; 
 
    TZREG tzReg = {0}; 
    LPBYTE lpPtr = lpbReg; 
 
    tzReg.lBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lStandardBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lDaylightBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    lpPtr += sizeof(WORD);// reserved 
 
    tzReg.stStandardDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
    lpPtr += sizeof(WORD);// reserved 
    tzReg.stDaylightDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
 
    TZREG* ptzReg = NULL; 
    ptzReg = new TZREG; 
    if (ptzReg) 
    { 
        *ptzReg = tzReg; 
    } 
 
    return ptzReg; 
} 

```

## <a name="see-also"></a>関連項目

- [予定からタイム ゾーンのプロパティを読み取る](how-to-read-time-zone-properties-from-an-appointment.md)

