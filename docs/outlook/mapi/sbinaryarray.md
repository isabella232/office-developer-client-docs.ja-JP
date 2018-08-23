---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586467"
---
# <a name="sbinaryarray"></a><span data-ttu-id="d2091-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="d2091-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="d2091-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2091-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2091-105">バイナリ値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2091-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2091-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d2091-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2091-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2091-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="d2091-108">Members</span><span class="sxs-lookup"><span data-stu-id="d2091-108">Members</span></span>

 <span data-ttu-id="d2091-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="d2091-109">**cValues**</span></span>
  
> <span data-ttu-id="d2091-110">**Lpbin**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="d2091-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="d2091-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="d2091-111">**lpbin**</span></span>
  
> <span data-ttu-id="d2091-112">バイナリ値を格納する[SBinary](sbinary.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d2091-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2091-113">注釈</span><span class="sxs-lookup"><span data-stu-id="d2091-113">Remarks</span></span>

<span data-ttu-id="d2091-114">**SBinaryArray**構造体を使用して、PT_MV_BINARY の種類のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="d2091-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="d2091-115">PT_MV_BINARY の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2091-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2091-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2091-116">See also</span></span>



[<span data-ttu-id="d2091-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="d2091-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="d2091-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d2091-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d2091-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d2091-119">MAPI Structures</span></span>](mapi-structures.md)

