---
title: PidTagControlStructure 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf91620042f916d51f27be50d15f72db537ad5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335246"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="defa6-103">PidTagControlStructure 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="defa6-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="defa6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="defa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="defa6-105">ダイアログボックスで使用されるコントロールの構造体へのポインターを格納します。</span><span class="sxs-lookup"><span data-stu-id="defa6-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="defa6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="defa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="defa6-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="defa6-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="defa6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="defa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="defa6-109">0x3f01</span><span class="sxs-lookup"><span data-stu-id="defa6-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="defa6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="defa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="defa6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="defa6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="defa6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="defa6-112">Area:</span></span>  <br/> |<span data-ttu-id="defa6-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="defa6-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="defa6-114">解説</span><span class="sxs-lookup"><span data-stu-id="defa6-114">Remarks</span></span>

<span data-ttu-id="defa6-115">このプロパティは、コントロール構造のいずれかにキャストされる long ポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="defa6-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="defa6-116">制御構造には次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="defa6-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="defa6-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="defa6-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="defa6-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="defa6-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="defa6-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="defa6-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="defa6-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="defa6-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="defa6-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="defa6-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="defa6-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="defa6-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="defa6-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="defa6-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="defa6-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="defa6-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="defa6-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="defa6-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="defa6-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="defa6-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="defa6-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="defa6-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="defa6-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="defa6-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="defa6-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="defa6-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="defa6-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="defa6-130">Header files</span></span>

<span data-ttu-id="defa6-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="defa6-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="defa6-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="defa6-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="defa6-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="defa6-133">Mapitags.h</span></span>
  
> <span data-ttu-id="defa6-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="defa6-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="defa6-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="defa6-135">See also</span></span>



[<span data-ttu-id="defa6-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="defa6-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="defa6-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="defa6-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="defa6-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="defa6-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="defa6-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="defa6-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

