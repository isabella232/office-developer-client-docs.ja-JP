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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438289"
---
# <a name="sbinaryarray"></a><span data-ttu-id="fa848-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="fa848-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="fa848-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa848-105">バイナリ値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="fa848-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa848-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fa848-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa848-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa848-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="fa848-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="fa848-108">Members</span></span>

 <span data-ttu-id="fa848-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="fa848-109">**cValues**</span></span>
  
> <span data-ttu-id="fa848-110">**lpbin**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="fa848-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="fa848-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="fa848-111">**lpbin**</span></span>
  
> <span data-ttu-id="fa848-112">バイナリ値を保持する[sbinary](sbinary.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fa848-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa848-113">注釈</span><span class="sxs-lookup"><span data-stu-id="fa848-113">Remarks</span></span>

<span data-ttu-id="fa848-114">**sbinaryarray**構造体は、PT_MV_BINARY 型のプロパティを記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa848-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="fa848-115">PT_MV_BINARY の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa848-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa848-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa848-116">See also</span></span>



[<span data-ttu-id="fa848-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="fa848-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="fa848-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fa848-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="fa848-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fa848-119">MAPI Structures</span></span>](mapi-structures.md)

