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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803802"
---
# <a name="sbinaryarray"></a><span data-ttu-id="fcb15-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="fcb15-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="fcb15-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcb15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fcb15-105">バイナリ値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fcb15-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb15-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fcb15-106">Header file:</span></span>  <br/> |<span data-ttu-id="fcb15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcb15-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="fcb15-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="fcb15-108">Members</span></span>

 <span data-ttu-id="fcb15-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="fcb15-109">**cValues**</span></span>
  
> <span data-ttu-id="fcb15-110">**Lpbin**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="fcb15-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="fcb15-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="fcb15-111">**lpbin**</span></span>
  
> <span data-ttu-id="fcb15-112">バイナリ値を格納する[SBinary](sbinary.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fcb15-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fcb15-113">備考</span><span class="sxs-lookup"><span data-stu-id="fcb15-113">Remarks</span></span>

<span data-ttu-id="fcb15-114">**SBinaryArray**構造体を使用して、PT_MV_BINARY の種類のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="fcb15-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="fcb15-115">PT_MV_BINARY の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fcb15-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fcb15-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcb15-116">See also</span></span>



[<span data-ttu-id="fcb15-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="fcb15-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="fcb15-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fcb15-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="fcb15-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fcb15-119">MAPI Structures</span></span>](mapi-structures.md)

