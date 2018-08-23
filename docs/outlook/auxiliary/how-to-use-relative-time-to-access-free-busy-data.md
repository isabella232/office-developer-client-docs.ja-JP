---
title: 空き時間情報データにアクセスするのに相対時間を使用する
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: 空き/予約済み API の IFreeBusyData のインターフェイスでは、1601 年 1 月 1 日からの分を世界協定時刻 (UTC) での表現の数は、相対的な時間の概念を使用し、型の値の長さは。
ms.openlocfilehash: b83cd46cfcc4d84d4fc3bf000dd8b0acdda545dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799323"
---
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="78814-103">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="78814-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="78814-104">空き/予約済み API の[IFreeBusyData](ifreebusydata.md)インタ フェースは 1601 年 1 月 1 日からの分を世界協定時刻 (UTC) での表現の数は、相対的な時間の概念を使用して、 **LONG**型の値です。</span><span class="sxs-lookup"><span data-stu-id="78814-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="78814-105">いくつかの一般的に使用される相対時間値は、次のように。</span><span class="sxs-lookup"><span data-stu-id="78814-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="78814-106">相対時間値が有効であるかを確認するために上記の相対的な時間の最大値と最小値を使用します。</span><span class="sxs-lookup"><span data-stu-id="78814-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="78814-107">NTFS は、 [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx)形式でネイティブ ファイルの時刻を記録するためは、 **FILETIME**との間の相対的な時間を変換するのには次のコード例を使用するのには便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="78814-107">Because NTFS records file times natively in [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="78814-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="78814-108">See also</span></span>

- [<span data-ttu-id="78814-109">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="78814-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="78814-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="78814-110">IFreeBusyData</span></span>](ifreebusydata.md)

