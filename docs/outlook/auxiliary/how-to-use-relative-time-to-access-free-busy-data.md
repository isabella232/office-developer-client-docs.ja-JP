---
title: 相対時間を使用して空き時間情報にアクセスする
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: Free/Busy API の IFreeBusyData インターフェイスでは、相対時間という概念が使用されます 。これは、1601 年 1 月 1 日からの分数で、世界時 (UTC) で表され、LONG 型の値です。
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317634"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>相対時間を使用して空き時間情報にアクセスする

Free/Busy API の[IFreeBusyData](ifreebusydata.md)インターフェイスでは、相対時間という概念が使用されます 。これは、1601 年 1 月 1 日からの分数で、世界時 (UTC) で表され、LONG 型の値です。 
  
一般的に使用される相対時間の値を次に示します。
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
相対時間の値が有効な場合は、前の最大時間と最小相対時間の値を使用します。
  
NTFS は FILETIME 形式でファイル時間をネイティブに記録しますので、次のコード例を使用して [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) の相対時間を変換すると **便利です**。 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

