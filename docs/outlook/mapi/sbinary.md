---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803799"
---
# <a name="sbinary"></a><span data-ttu-id="cfe3b-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="cfe3b-103">SBinary</span></span>

  
  
<span data-ttu-id="cfe3b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfe3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfe3b-105">PT_BINARY の型のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cfe3b-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfe3b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cfe3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="cfe3b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cfe3b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="cfe3b-108">Members</span><span class="sxs-lookup"><span data-stu-id="cfe3b-108">Members</span></span>

 <span data-ttu-id="cfe3b-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="cfe3b-109">**cb**</span></span>
  
> <span data-ttu-id="cfe3b-110">**Lpb**のメンバーのバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="cfe3b-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="cfe3b-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="cfe3b-111">**lpb**</span></span>
  
> <span data-ttu-id="cfe3b-112">PT_BINARY プロパティの値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cfe3b-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cfe3b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="cfe3b-113">Remarks</span></span>

<span data-ttu-id="cfe3b-114">プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfe3b-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cfe3b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="cfe3b-115">See also</span></span>



[<span data-ttu-id="cfe3b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cfe3b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="cfe3b-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="cfe3b-117">MAPI Structures</span></span>](mapi-structures.md)

