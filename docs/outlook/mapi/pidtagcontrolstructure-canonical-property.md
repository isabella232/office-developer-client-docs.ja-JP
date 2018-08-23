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
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802629"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="90ebb-103">PidTagControlStructure 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="90ebb-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="90ebb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90ebb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90ebb-105">ダイアログ ボックスで使用されているコントロールの構造体へのポインターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="90ebb-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90ebb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="90ebb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90ebb-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="90ebb-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="90ebb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="90ebb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90ebb-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="90ebb-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="90ebb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="90ebb-110">Data type:</span></span>  <br/> |<span data-ttu-id="90ebb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="90ebb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="90ebb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="90ebb-112">Area:</span></span>  <br/> |<span data-ttu-id="90ebb-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="90ebb-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90ebb-114">注釈</span><span class="sxs-lookup"><span data-stu-id="90ebb-114">Remarks</span></span>

<span data-ttu-id="90ebb-115">このプロパティは、コントロールの構造体のいずれかにキャストされる long ポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="90ebb-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="90ebb-116">制御構造体は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="90ebb-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="90ebb-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="90ebb-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="90ebb-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="90ebb-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="90ebb-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="90ebb-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="90ebb-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="90ebb-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="90ebb-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="90ebb-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="90ebb-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="90ebb-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="90ebb-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="90ebb-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="90ebb-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="90ebb-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="90ebb-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="90ebb-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="90ebb-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="90ebb-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="90ebb-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="90ebb-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="90ebb-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="90ebb-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="90ebb-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="90ebb-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="90ebb-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="90ebb-130">Header files</span></span>

<span data-ttu-id="90ebb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90ebb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="90ebb-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="90ebb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="90ebb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90ebb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="90ebb-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="90ebb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90ebb-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="90ebb-135">See also</span></span>



[<span data-ttu-id="90ebb-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90ebb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90ebb-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="90ebb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90ebb-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90ebb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90ebb-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="90ebb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

