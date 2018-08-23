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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f8f58ee18095dec8a222ae8b5a19cbefbaafa663
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801687"
---
# <a name="mviprop"></a><span data-ttu-id="dba43-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="dba43-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="dba43-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dba43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dba43-105">指定したプロパティの MVI_FLAG を設定します。</span><span class="sxs-lookup"><span data-stu-id="dba43-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dba43-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dba43-106">Header file:</span></span>  <br/> |<span data-ttu-id="dba43-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dba43-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dba43-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="dba43-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="dba43-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dba43-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="dba43-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dba43-110">Parameters</span></span>

 <span data-ttu-id="dba43-111">_タグ_</span><span class="sxs-lookup"><span data-stu-id="dba43-111">_tag_</span></span>
  
> <span data-ttu-id="dba43-112">変更するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="dba43-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dba43-113">注釈</span><span class="sxs-lookup"><span data-stu-id="dba43-113">Remarks</span></span>

<span data-ttu-id="dba43-114">MVI_FLAG として、複数値を持つプロパティを識別する、MV_FLAG、MV_INSTANCE、複数の行のテーブルに、複数値を持つプロパティが表示されることを要求するの設定を結合します。</span><span class="sxs-lookup"><span data-stu-id="dba43-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="dba43-115">影響を受けるプロパティのプロパティの型が変更されたが、識別子は変更されません。</span><span class="sxs-lookup"><span data-stu-id="dba43-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="dba43-116">などの PT_FLOAT の種類のプロパティには、MVI_PROP マクロを適用するときは、その型が PT_MV_FLOAT に変更されます。</span><span class="sxs-lookup"><span data-stu-id="dba43-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="dba43-117">、テーブルに含まれるときは、複数の行を使用して値ごとに 1 つの行のプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="dba43-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="dba43-118">他の列のプロパティが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="dba43-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="dba43-119">これらのフラグの詳細については、 [MAPI プロパティの型の概要](mapi-property-type-overview.md)」および「[複数値を持つ列の使用](working-with-multivalued-columns.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dba43-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dba43-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="dba43-120">See also</span></span>



[<span data-ttu-id="dba43-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dba43-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="dba43-122">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="dba43-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

