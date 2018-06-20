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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804061"
---
# <a name="swstringarray"></a><span data-ttu-id="e80e2-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="e80e2-103">SWStringArray</span></span>

  
  
<span data-ttu-id="e80e2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e80e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e80e2-105">PT_MV_UNICODE の種類のプロパティを説明するために使用する文字の文字列の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e80e2-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e80e2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e80e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="e80e2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e80e2-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="e80e2-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="e80e2-108">Members</span></span>

 <span data-ttu-id="e80e2-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="e80e2-109">**cValues**</span></span>
  
> <span data-ttu-id="e80e2-110">**LppszW**メンバーが指す配列内の文字列の数です。</span><span class="sxs-lookup"><span data-stu-id="e80e2-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="e80e2-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="e80e2-111">**lppszW**</span></span>
  
> <span data-ttu-id="e80e2-112">Unicode 文字の null 終了文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e80e2-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e80e2-113">備考</span><span class="sxs-lookup"><span data-stu-id="e80e2-113">Remarks</span></span>

<span data-ttu-id="e80e2-114">PT_MV_UNICODE の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e80e2-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e80e2-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e80e2-115">See also</span></span>



[<span data-ttu-id="e80e2-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e80e2-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e80e2-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e80e2-117">MAPI Structures</span></span>](mapi-structures.md)

