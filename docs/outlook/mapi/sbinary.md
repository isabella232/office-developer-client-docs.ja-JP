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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407845"
---
# <a name="sbinary"></a><span data-ttu-id="5d4b4-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="5d4b4-103">SBinary</span></span>

  
  
<span data-ttu-id="5d4b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d4b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d4b4-105">型のプロパティをPT_BINARY。</span><span class="sxs-lookup"><span data-stu-id="5d4b4-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d4b4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5d4b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d4b4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d4b4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="5d4b4-108">Members</span><span class="sxs-lookup"><span data-stu-id="5d4b4-108">Members</span></span>

 <span data-ttu-id="5d4b4-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="5d4b4-109">**cb**</span></span>
  
> <span data-ttu-id="5d4b4-110">**lpb** メンバー内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5d4b4-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="5d4b4-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="5d4b4-111">**lpb**</span></span>
  
> <span data-ttu-id="5d4b4-112">プロパティ値PT_BINARYポインター。</span><span class="sxs-lookup"><span data-stu-id="5d4b4-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d4b4-113">注釈</span><span class="sxs-lookup"><span data-stu-id="5d4b4-113">Remarks</span></span>

<span data-ttu-id="5d4b4-114">プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5d4b4-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d4b4-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d4b4-115">See also</span></span>



[<span data-ttu-id="5d4b4-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5d4b4-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5d4b4-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5d4b4-117">MAPI Structures</span></span>](mapi-structures.md)

