---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439402"
---
# <a name="scurrencyarray"></a><span data-ttu-id="cdc8c-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="cdc8c-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="cdc8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc8c-105">データ型のプロパティを記述するために使用される通貨値の配列をPT_MV_CURRENCY。</span><span class="sxs-lookup"><span data-stu-id="cdc8c-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cdc8c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cdc8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="cdc8c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdc8c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="cdc8c-108">Members</span><span class="sxs-lookup"><span data-stu-id="cdc8c-108">Members</span></span>

 <span data-ttu-id="cdc8c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="cdc8c-109">**cValues**</span></span>
  
> <span data-ttu-id="cdc8c-110">lpcur メンバーが指す配列内の **値の** 数。</span><span class="sxs-lookup"><span data-stu-id="cdc8c-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="cdc8c-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="cdc8c-111">**lpcur**</span></span>
  
> <span data-ttu-id="cdc8c-112">通貨値を含む [CURRENCY](currency.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cdc8c-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cdc8c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="cdc8c-113">Remarks</span></span>

<span data-ttu-id="cdc8c-114">プロパティの詳細についてはPT_MV_CURRENCYプロパティ [の種類の一覧を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="cdc8c-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cdc8c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdc8c-115">See also</span></span>



[<span data-ttu-id="cdc8c-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="cdc8c-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="cdc8c-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cdc8c-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="cdc8c-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="cdc8c-118">MAPI Structures</span></span>](mapi-structures.md)

