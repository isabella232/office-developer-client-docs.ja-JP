---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803841"
---
# <a name="sdatetimearray"></a><span data-ttu-id="1f869-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="1f869-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="1f869-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f869-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f869-105">PT_MV_SYSTIME の種類のプロパティを説明するために使用する時刻の値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f869-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f869-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1f869-106">Header file:</span></span>  <br/> |<span data-ttu-id="1f869-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f869-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="1f869-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="1f869-108">Members</span></span>

 <span data-ttu-id="1f869-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="1f869-109">**cValues**</span></span>
  
> <span data-ttu-id="1f869-110">**Lpft**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="1f869-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="1f869-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="1f869-111">**lpft**</span></span>
  
> <span data-ttu-id="1f869-112">Time 値を格納する[FILETIME](filetime.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1f869-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1f869-113">備考</span><span class="sxs-lookup"><span data-stu-id="1f869-113">Remarks</span></span>

<span data-ttu-id="1f869-114">PT_MV_SYSTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f869-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1f869-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f869-115">See also</span></span>



[<span data-ttu-id="1f869-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="1f869-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="1f869-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1f869-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1f869-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1f869-118">MAPI Structures</span></span>](mapi-structures.md)

