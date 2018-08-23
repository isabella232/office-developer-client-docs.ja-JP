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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581357"
---
# <a name="swstringarray"></a><span data-ttu-id="ab02f-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="ab02f-103">SWStringArray</span></span>

  
  
<span data-ttu-id="ab02f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab02f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab02f-105">PT_MV_UNICODE の種類のプロパティを説明するために使用する文字の文字列の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab02f-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab02f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab02f-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab02f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab02f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="ab02f-108">Members</span><span class="sxs-lookup"><span data-stu-id="ab02f-108">Members</span></span>

 <span data-ttu-id="ab02f-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="ab02f-109">**cValues**</span></span>
  
> <span data-ttu-id="ab02f-110">**LppszW**メンバーが指す配列内の文字列の数です。</span><span class="sxs-lookup"><span data-stu-id="ab02f-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="ab02f-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="ab02f-111">**lppszW**</span></span>
  
> <span data-ttu-id="ab02f-112">Unicode 文字の null 終了文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab02f-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab02f-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ab02f-113">Remarks</span></span>

<span data-ttu-id="ab02f-114">PT_MV_UNICODE の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab02f-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab02f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab02f-115">See also</span></span>



[<span data-ttu-id="ab02f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ab02f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ab02f-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ab02f-117">MAPI Structures</span></span>](mapi-structures.md)

