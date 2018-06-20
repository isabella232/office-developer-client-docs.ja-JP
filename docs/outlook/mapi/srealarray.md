---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803992"
---
# <a name="srealarray"></a><span data-ttu-id="f666c-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="f666c-103">SRealArray</span></span>

  
  
<span data-ttu-id="f666c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f666c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f666c-105">PT_MV_R4 の種類のプロパティを説明するために使用される浮動小数点値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f666c-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f666c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f666c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f666c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f666c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="f666c-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="f666c-108">Members</span></span>

 <span data-ttu-id="f666c-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="f666c-109">**cValues**</span></span>
  
> <span data-ttu-id="f666c-110">**Lpflt**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="f666c-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="f666c-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="f666c-111">**lpflt**</span></span>
  
> <span data-ttu-id="f666c-112">Float 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f666c-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f666c-113">備考</span><span class="sxs-lookup"><span data-stu-id="f666c-113">Remarks</span></span>

<span data-ttu-id="f666c-114">PT_MV_R4 プロパティのデータ型の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f666c-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f666c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f666c-115">See also</span></span>



[<span data-ttu-id="f666c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f666c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f666c-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f666c-117">MAPI Structures</span></span>](mapi-structures.md)

