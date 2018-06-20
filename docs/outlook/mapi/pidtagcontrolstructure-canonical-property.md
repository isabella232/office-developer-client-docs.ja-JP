---
title: PidTagControlStructure の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802629"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="df6b4-103">PidTagControlStructure の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="df6b4-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="df6b4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df6b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df6b4-105">ダイアログ ボックスで使用されているコントロールの構造体へのポインターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="df6b4-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df6b4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="df6b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df6b4-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="df6b4-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="df6b4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="df6b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df6b4-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="df6b4-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="df6b4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="df6b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="df6b4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df6b4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df6b4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="df6b4-112">Area:</span></span>  <br/> |<span data-ttu-id="df6b4-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="df6b4-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df6b4-114">備考</span><span class="sxs-lookup"><span data-stu-id="df6b4-114">Remarks</span></span>

<span data-ttu-id="df6b4-115">このプロパティは、コントロールの構造体のいずれかにキャストされる long ポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="df6b4-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="df6b4-116">制御構造体は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df6b4-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="df6b4-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="df6b4-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="df6b4-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="df6b4-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="df6b4-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="df6b4-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="df6b4-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="df6b4-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="df6b4-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="df6b4-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="df6b4-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="df6b4-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="df6b4-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="df6b4-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="df6b4-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="df6b4-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="df6b4-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="df6b4-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="df6b4-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="df6b4-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="df6b4-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="df6b4-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="df6b4-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="df6b4-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="df6b4-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="df6b4-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="df6b4-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="df6b4-130">Header files</span></span>

<span data-ttu-id="df6b4-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df6b4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="df6b4-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="df6b4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="df6b4-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="df6b4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="df6b4-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="df6b4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df6b4-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="df6b4-135">See also</span></span>



[<span data-ttu-id="df6b4-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="df6b4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df6b4-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="df6b4-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df6b4-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="df6b4-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df6b4-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="df6b4-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

