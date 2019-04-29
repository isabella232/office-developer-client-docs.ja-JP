---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 087d38face72e1e067350b1959b37313ebbd7c44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410680"
---
# <a name="mviprop"></a><span data-ttu-id="4c3ce-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="4c3ce-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="4c3ce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c3ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c3ce-105">指定したプロパティの MVI_FLAG を設定します。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c3ce-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4c3ce-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c3ce-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c3ce-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4c3ce-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="4c3ce-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="4c3ce-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4c3ce-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="4c3ce-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c3ce-110">Parameters</span></span>

 <span data-ttu-id="4c3ce-111">_マーク_</span><span class="sxs-lookup"><span data-stu-id="4c3ce-111">_tag_</span></span>
  
> <span data-ttu-id="4c3ce-112">変更するプロパティタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4c3ce-113">注釈</span><span class="sxs-lookup"><span data-stu-id="4c3ce-113">Remarks</span></span>

<span data-ttu-id="4c3ce-114">MVI_FLAG は、MV_FLAG の設定を結合し、プロパティを複数値として識別し、MV_INSTANCE を複数の行のテーブルに複数値のプロパティを表示することを要求します。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="4c3ce-115">影響を受けるプロパティのプロパティの種類は変更されますが、識別子は変更されません。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="4c3ce-116">たとえば、MVI_PROP マクロが PT_FLOAT 型のプロパティに適用されている場合、その型は PT_MV_FLOAT に変更されます。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="4c3ce-117">テーブルに含まれている場合は、値ごとに1行のプロパティを表すために複数の行が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="4c3ce-118">その他の列のプロパティが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="4c3ce-119">これらのフラグの詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」および「[複数値を持つ列の処理](working-with-multivalued-columns.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c3ce-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c3ce-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="4c3ce-120">See also</span></span>



[<span data-ttu-id="4c3ce-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4c3ce-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4c3ce-122">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="4c3ce-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

