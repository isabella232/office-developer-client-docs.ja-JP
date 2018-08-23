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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572453"
---
# <a name="scurrencyarray"></a><span data-ttu-id="0dd12-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="0dd12-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="0dd12-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd12-105">PT_MV_CURRENCY の種類のプロパティを説明するために使用する通貨値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0dd12-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dd12-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0dd12-106">Header file:</span></span>  <br/> |<span data-ttu-id="0dd12-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dd12-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="0dd12-108">Members</span><span class="sxs-lookup"><span data-stu-id="0dd12-108">Members</span></span>

 <span data-ttu-id="0dd12-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="0dd12-109">**cValues**</span></span>
  
> <span data-ttu-id="0dd12-110">**Lpcur**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="0dd12-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="0dd12-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="0dd12-111">**lpcur**</span></span>
  
> <span data-ttu-id="0dd12-112">通貨値が含まれている[通貨](currency.md)の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0dd12-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0dd12-113">注釈</span><span class="sxs-lookup"><span data-stu-id="0dd12-113">Remarks</span></span>

<span data-ttu-id="0dd12-114">PT_MV_CURRENCY については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0dd12-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0dd12-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="0dd12-115">See also</span></span>



[<span data-ttu-id="0dd12-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="0dd12-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="0dd12-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0dd12-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0dd12-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0dd12-118">MAPI Structures</span></span>](mapi-structures.md)

