---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430386"
---
# <a name="sapptimearray"></a><span data-ttu-id="fbc6a-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="fbc6a-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="fbc6a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbc6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbc6a-105">時間値の配列を含む。</span><span class="sxs-lookup"><span data-stu-id="fbc6a-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbc6a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fbc6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fbc6a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbc6a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="fbc6a-108">Members</span><span class="sxs-lookup"><span data-stu-id="fbc6a-108">Members</span></span>

 <span data-ttu-id="fbc6a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="fbc6a-109">**cValues**</span></span>
  
> <span data-ttu-id="fbc6a-110">lpat メンバーが指す配列内の **値の** 数。</span><span class="sxs-lookup"><span data-stu-id="fbc6a-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="fbc6a-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="fbc6a-111">**lpat**</span></span>
  
> <span data-ttu-id="fbc6a-112">アプリケーションの時刻値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbc6a-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fbc6a-113">注釈</span><span class="sxs-lookup"><span data-stu-id="fbc6a-113">Remarks</span></span>

<span data-ttu-id="fbc6a-114">**SAppTimeArray 構造体は**、データ型のプロパティを定義するために使用PT_MV_APPTIME。</span><span class="sxs-lookup"><span data-stu-id="fbc6a-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="fbc6a-115">プロパティの詳細については、「PT_MV_APPTIMEプロパティ [の種類の一覧」を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc6a-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fbc6a-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbc6a-116">See also</span></span>



[<span data-ttu-id="fbc6a-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fbc6a-117">MAPI Structures</span></span>](mapi-structures.md)

