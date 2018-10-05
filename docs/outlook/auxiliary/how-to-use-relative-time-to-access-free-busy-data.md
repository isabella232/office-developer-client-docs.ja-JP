---
title: 空き時間情報データにアクセスするのに相対時間を使用する
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: 空き/予約済み API の IFreeBusyData のインターフェイスでは、1601 年 1 月 1 日からの分を世界協定時刻 (UTC) での表現の数は、相対的な時間の概念を使用し、型の値の長さは。
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386937"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>空き時間情報データにアクセスするのに相対時間を使用する

空き/予約済み API の[IFreeBusyData](ifreebusydata.md)インタ フェースは 1601 年 1 月 1 日からの分を世界協定時刻 (UTC) での表現の数は、相対的な時間の概念を使用して、 **LONG**型の値です。 
  
いくつかの一般的に使用される相対時間値は、次のように。
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
相対時間値が有効であるかを確認するために上記の相対的な時間の最大値と最小値を使用します。
  
NTFS は、 [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx)形式でネイティブ ファイルの時刻を記録するためは、 **FILETIME**との間の相対的な時間を変換するのには次のコード例を使用するのには便利な場合があります。 
  
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

