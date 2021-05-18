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
# <a name="swstringarray"></a><span data-ttu-id="17ad7-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="17ad7-103">SWStringArray</span></span>

  
  
<span data-ttu-id="17ad7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17ad7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17ad7-105">文字列型のプロパティを記述するために使用される文字列の配列をPT_MV_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="17ad7-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17ad7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="17ad7-106">Header file:</span></span>  <br/> |<span data-ttu-id="17ad7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17ad7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="17ad7-108">Members</span><span class="sxs-lookup"><span data-stu-id="17ad7-108">Members</span></span>

 <span data-ttu-id="17ad7-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="17ad7-109">**cValues**</span></span>
  
> <span data-ttu-id="17ad7-110">lppszW メンバーが指す配列 **内の文字列の** 数。</span><span class="sxs-lookup"><span data-stu-id="17ad7-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="17ad7-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="17ad7-111">**lppszW**</span></span>
  
> <span data-ttu-id="17ad7-112">Null で終了した Unicode 文字文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="17ad7-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17ad7-113">注釈</span><span class="sxs-lookup"><span data-stu-id="17ad7-113">Remarks</span></span>

<span data-ttu-id="17ad7-114">プロパティの詳細については、「プロパティPT_MV_UNICODE」 [を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="17ad7-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17ad7-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="17ad7-115">See also</span></span>



[<span data-ttu-id="17ad7-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="17ad7-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="17ad7-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="17ad7-117">MAPI Structures</span></span>](mapi-structures.md)

