---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413606"
---
# <a name="swstringarray"></a><span data-ttu-id="eb758-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="eb758-103">SWStringArray</span></span>

  
  
<span data-ttu-id="eb758-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb758-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb758-105">PT_MV_UNICODE 型のプロパティを記述するために使用される文字列の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="eb758-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb758-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="eb758-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb758-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb758-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="eb758-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="eb758-108">Members</span></span>

 <span data-ttu-id="eb758-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="eb758-109">**cValues**</span></span>
  
> <span data-ttu-id="eb758-110">**lppszw**メンバーによって示される配列内の文字列の数。</span><span class="sxs-lookup"><span data-stu-id="eb758-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="eb758-111">**lppszw**</span><span class="sxs-lookup"><span data-stu-id="eb758-111">**lppszW**</span></span>
  
> <span data-ttu-id="eb758-112">null で終了する Unicode 文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb758-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb758-113">注釈</span><span class="sxs-lookup"><span data-stu-id="eb758-113">Remarks</span></span>

<span data-ttu-id="eb758-114">PT_MV_UNICODE の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb758-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb758-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb758-115">See also</span></span>



[<span data-ttu-id="eb758-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eb758-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="eb758-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="eb758-117">MAPI Structures</span></span>](mapi-structures.md)

