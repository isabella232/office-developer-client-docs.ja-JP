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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409504"
---
# <a name="filetime"></a><span data-ttu-id="707d9-103">FILETIME</span><span class="sxs-lookup"><span data-stu-id="707d9-103">FILETIME</span></span>

  
  
<span data-ttu-id="707d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="707d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="707d9-105">ファイルの、未署名の64ビットの日付と時刻の値を保持します。</span><span class="sxs-lookup"><span data-stu-id="707d9-105">Holds an unsigned 64-bit date and time value for a file.</span></span> <span data-ttu-id="707d9-106">この値は、1601年1月1日からの100ナノ秒単位の数を表します。</span><span class="sxs-lookup"><span data-stu-id="707d9-106">This value represents the number of 100-nanosecond units since the start of January 1, 1601.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="707d9-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="707d9-107">Header file:</span></span>  <br/> |<span data-ttu-id="707d9-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="707d9-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a><span data-ttu-id="707d9-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="707d9-109">Members</span></span>

 <span data-ttu-id="707d9-110">**dwlowdatetime**</span><span class="sxs-lookup"><span data-stu-id="707d9-110">**dwLowDateTime**</span></span>
  
> <span data-ttu-id="707d9-111">file time 値の低順位32ビット。</span><span class="sxs-lookup"><span data-stu-id="707d9-111">Low-order 32 bits of the file time value.</span></span> 
    
 <span data-ttu-id="707d9-112">**dwHighDateTime**</span><span class="sxs-lookup"><span data-stu-id="707d9-112">**dwHighDateTime**</span></span>
  
> <span data-ttu-id="707d9-113">file time 値の上位32ビット。</span><span class="sxs-lookup"><span data-stu-id="707d9-113">High-order 32 bits of the file time value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="707d9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="707d9-114">Remarks</span></span>

<span data-ttu-id="707d9-115">PT_SYSTIME 型のプロパティには、その値の**FILETIME**構造があります。</span><span class="sxs-lookup"><span data-stu-id="707d9-115">A property of type PT_SYSTIME has a **FILETIME** structure for its value.</span></span> <span data-ttu-id="707d9-116">このようなプロパティは、 [spropvalue](spropvalue.md)構造の定義において、**値**メンバーの**FILETIME**データ型を持っています。</span><span class="sxs-lookup"><span data-stu-id="707d9-116">Such a property has a **FILETIME** data type for the **Value** member in its definition in an [SPropValue](spropvalue.md) structure.</span></span> 
  
<span data-ttu-id="707d9-117">**FILETIME**構造体の定義は、 _Win32 プログラマーズリファレンス_および MAPI ヘッダーファイル mapidefs.h にあります。</span><span class="sxs-lookup"><span data-stu-id="707d9-117">The definition of the **FILETIME** structure is in the  _Win32 Programmer's Reference_ and in the MAPI header file Mapidefs.h.</span></span> <span data-ttu-id="707d9-118">MAPI は、Win32 定義が使用できない場合に、その構造が定義されていることを確認するために、その構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="707d9-118">MAPI defines the structure conditionally to make sure that it is defined when the Win32 definition is unavailable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="707d9-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="707d9-119">See also</span></span>



[<span data-ttu-id="707d9-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="707d9-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="707d9-121">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="707d9-121">MAPI Structures</span></span>](mapi-structures.md)

