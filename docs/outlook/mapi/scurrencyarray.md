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
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803851"
---
# <a name="scurrencyarray"></a><span data-ttu-id="f62b4-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="f62b4-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="f62b4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f62b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f62b4-105">PT_MV_CURRENCY の種類のプロパティを説明するために使用する通貨値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f62b4-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f62b4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f62b4-106">Header file:</span></span>  <br/> |<span data-ttu-id="f62b4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f62b4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="f62b4-108">Members</span><span class="sxs-lookup"><span data-stu-id="f62b4-108">Members</span></span>

 <span data-ttu-id="f62b4-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="f62b4-109">**cValues**</span></span>
  
> <span data-ttu-id="f62b4-110">**Lpcur**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="f62b4-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="f62b4-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="f62b4-111">**lpcur**</span></span>
  
> <span data-ttu-id="f62b4-112">通貨値が含まれている[通貨](currency.md)の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f62b4-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f62b4-113">注釈</span><span class="sxs-lookup"><span data-stu-id="f62b4-113">Remarks</span></span>

<span data-ttu-id="f62b4-114">PT_MV_CURRENCY については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f62b4-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f62b4-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f62b4-115">See also</span></span>



[<span data-ttu-id="f62b4-116">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="f62b4-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="f62b4-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f62b4-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f62b4-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f62b4-118">MAPI Structures</span></span>](mapi-structures.md)

