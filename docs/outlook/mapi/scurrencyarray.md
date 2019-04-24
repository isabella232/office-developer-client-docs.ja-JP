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
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360698"
---
# <a name="scurrencyarray"></a><span data-ttu-id="41198-103">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="41198-103">SCurrencyArray</span></span>

  
  
<span data-ttu-id="41198-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41198-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41198-105">PT_MV_CURRENCY 型のプロパティを記述するために使用される通貨値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="41198-105">Contains an array of currency values that are used to describe a property of type PT_MV_CURRENCY.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41198-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="41198-106">Header file:</span></span>  <br/> |<span data-ttu-id="41198-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41198-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a><span data-ttu-id="41198-108">Members</span><span class="sxs-lookup"><span data-stu-id="41198-108">Members</span></span>

 <span data-ttu-id="41198-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="41198-109">**cValues**</span></span>
  
> <span data-ttu-id="41198-110">lpcur メンバーによって参照されて\*\*\*\* いる配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="41198-110">Count of values in the array pointed to by the **lpcur** member.</span></span> 
    
 <span data-ttu-id="41198-111">**lpcur**</span><span class="sxs-lookup"><span data-stu-id="41198-111">**lpcur**</span></span>
  
> <span data-ttu-id="41198-112">通貨の値を含む[通貨](currency.md)構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="41198-112">Pointer to an array of [CURRENCY](currency.md) structures that contain the currency values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="41198-113">解説</span><span class="sxs-lookup"><span data-stu-id="41198-113">Remarks</span></span>

<span data-ttu-id="41198-114">PT_MV_CURRENCY の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41198-114">For information about PT_MV_CURRENCY, see [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41198-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="41198-115">See also</span></span>



[<span data-ttu-id="41198-116">単位</span><span class="sxs-lookup"><span data-stu-id="41198-116">CURRENCY</span></span>](currency.md)
  
[<span data-ttu-id="41198-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="41198-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="41198-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="41198-118">MAPI Structures</span></span>](mapi-structures.md)

