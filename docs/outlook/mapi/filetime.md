---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800063"
---
# <a name="filetime"></a><span data-ttu-id="db61a-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="db61a-103">FILETIME</span></span>

  
  
<span data-ttu-id="db61a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db61a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db61a-105">符号なし 64 ビットの日付と、ファイルの時刻の値を保持します。</span><span class="sxs-lookup"><span data-stu-id="db61a-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="db61a-106">この値は、1601 年 1 月 1 日の開始以降の 100 ナノ秒単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="db61a-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db61a-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="db61a-107">Header file:</span></span>  <br/> |<span data-ttu-id="db61a-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db61a-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="db61a-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="db61a-109">Members</span></span>

 <span data-ttu-id="db61a-110">**dwLowDateTime**</span><span class="sxs-lookup"><span data-stu-id="db61a-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="db61a-111">ファイル時刻の値の下位 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="db61a-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="db61a-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="db61a-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="db61a-113">ファイル時刻の値の上位の 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="db61a-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db61a-114">備考</span><span class="sxs-lookup"><span data-stu-id="db61a-114">Remarks</span></span>

<span data-ttu-id="db61a-115">タイプ PT_SYSTIME のプロパティは、 **FILETIME**構造体の値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="db61a-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="db61a-116">このようなプロパティでは、**値**メンバー [SPropValue](spropvalue.md)構造体の定義内の**FILETIME**データ型があります。</span><span class="sxs-lookup"><span data-stu-id="db61a-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="db61a-117">**FILETIME**構造体の定義は、 _Win32 プログラマーズ リファレンス_では、MAPI のヘッダー ファイル Mapidefs.h には。</span><span class="sxs-lookup"><span data-stu-id="db61a-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="db61a-118">MAPI では、Win32 の定義が使用可能な場合が定義されているかどうかを確認するには、条件付きで構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="db61a-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db61a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="db61a-119">See also</span></span>



[<span data-ttu-id="db61a-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="db61a-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="db61a-121">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="db61a-121">MAPI Structures</span></span>](mapi-structures.md)

