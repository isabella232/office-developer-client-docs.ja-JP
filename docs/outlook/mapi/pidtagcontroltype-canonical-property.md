---
title: PidTagControlType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734204"
---
# <a name="pidtagcontroltype-canonical-property"></a><span data-ttu-id="7b710-103">PidTagControlType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b710-103">PidTagControlType Canonical Property</span></span>

  
  
<span data-ttu-id="7b710-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b710-105">ダイアログ ボックスで使用されるコントロールのコントロールの種類を示す値を格納します。</span><span class="sxs-lookup"><span data-stu-id="7b710-105">Contains a value indicating a control type for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b710-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7b710-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b710-107">PR_CONTROL_TYPE</span><span class="sxs-lookup"><span data-stu-id="7b710-107">PR_CONTROL_TYPE</span></span>  <br/> |
|<span data-ttu-id="7b710-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7b710-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b710-109">0x3F02</span><span class="sxs-lookup"><span data-stu-id="7b710-109">0x3F02</span></span>  <br/> |
|<span data-ttu-id="7b710-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7b710-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b710-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7b710-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7b710-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7b710-112">Area:</span></span>  <br/> |<span data-ttu-id="7b710-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="7b710-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b710-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7b710-114">Remarks</span></span>

<span data-ttu-id="7b710-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7b710-115">This property can have exactly one of the following values:</span></span>
    
<span data-ttu-id="7b710-116">DTCT_LABEL (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="7b710-116">DTCT_LABEL (0x00000000)</span></span>
  
> <span data-ttu-id="7b710-117">ダイアログ ラベル。</span><span class="sxs-lookup"><span data-stu-id="7b710-117">A dialog label.</span></span>
   
<span data-ttu-id="7b710-118">DTCT_EDIT (0x000000001)</span><span class="sxs-lookup"><span data-stu-id="7b710-118">DTCT_EDIT (0x00000001)</span></span>
  
> <span data-ttu-id="7b710-119">ダイアログの編集テキスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-119">A dialog edit text box.</span></span>

<span data-ttu-id="7b710-120">DTCT_LBX (0x000000002)</span><span class="sxs-lookup"><span data-stu-id="7b710-120">DTCT_LBX (0x00000002)</span></span>
  
> <span data-ttu-id="7b710-121">ダイアログ リスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-121">A dialog list box.</span></span>
    
<span data-ttu-id="7b710-122">DTCT_COMBOBOX (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="7b710-122">DTCT_COMBOBOX (0x00000003)</span></span>
  
> <span data-ttu-id="7b710-123">ダイアログ コンボ ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-123">A dialog combo box.</span></span>

<span data-ttu-id="7b710-124">DTCT_DDLBX (0x000000004)</span><span class="sxs-lookup"><span data-stu-id="7b710-124">DTCT_DDLBX (0x00000004)</span></span>
  
> <span data-ttu-id="7b710-125">ダイアログ ボックスのドロップダウン リスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-125">A dialog drop-down list box.</span></span>

<span data-ttu-id="7b710-126">DTCT_CHECKBOX (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="7b710-126">DTCT_CHECKBOX (0x00000005)</span></span>
  
> <span data-ttu-id="7b710-127">ダイアログ チェック ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-127">A dialog check box.</span></span>

<span data-ttu-id="7b710-128">DTCT_GROUPBOX (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="7b710-128">DTCT_GROUPBOX (0x00000006)</span></span>
  
> <span data-ttu-id="7b710-129">ダイアログ グループ ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-129">A dialog group box.</span></span>
  
<span data-ttu-id="7b710-130">DTCT_BUTTON (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="7b710-130">DTCT_BUTTON (0x00000007)</span></span>
  
> <span data-ttu-id="7b710-131">ダイアログ ボタン コントロール。</span><span class="sxs-lookup"><span data-stu-id="7b710-131">A dialog button control.</span></span>
    
<span data-ttu-id="7b710-132">DTCT_PAGE (0x000000008)</span><span class="sxs-lookup"><span data-stu-id="7b710-132">DTCT_PAGE (0x00000008)</span></span>
  
> <span data-ttu-id="7b710-133">タブ付きダイアログ ページ。</span><span class="sxs-lookup"><span data-stu-id="7b710-133">A dialog tabbed page.</span></span>
    
<span data-ttu-id="7b710-134">DTCT_RADIOBUTTON (0x00000009)</span><span class="sxs-lookup"><span data-stu-id="7b710-134">DTCT_RADIOBUTTON (0x00000009)</span></span>
  
> <span data-ttu-id="7b710-135">ダイアログのラジオ ボタン。</span><span class="sxs-lookup"><span data-stu-id="7b710-135">A dialog radio button.</span></span>
    
<span data-ttu-id="7b710-136">DTCT_MVLISTBOX (0x0000000B)</span><span class="sxs-lookup"><span data-stu-id="7b710-136">DTCT_MVLISTBOX (0x0000000B)</span></span>
  
> <span data-ttu-id="7b710-137">文字列型の複数値プロパティによって設定される複数値リスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-137">A multivalued list box populated by a multivalued property of type string.</span></span>
    
<span data-ttu-id="7b710-138">DTCT_MVDDLBX (0x0000000C)</span><span class="sxs-lookup"><span data-stu-id="7b710-138">DTCT_MVDDLBX (0x0000000C)</span></span>
  
> <span data-ttu-id="7b710-139">文字列型の複数値プロパティによって設定される複数値ドロップダウン リスト ボックス。</span><span class="sxs-lookup"><span data-stu-id="7b710-139">A multivalued drop-down list box populated by a multivalued property of type string.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="7b710-140">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7b710-140">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7b710-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7b710-141">Header files</span></span>

<span data-ttu-id="7b710-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b710-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b710-143">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b710-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b710-144">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b710-144">mapitags.h</span></span>
  
> <span data-ttu-id="7b710-145">代替名として表示されるプロパティの定義を含む。</span><span class="sxs-lookup"><span data-stu-id="7b710-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b710-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b710-146">See also</span></span>



[<span data-ttu-id="7b710-147">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7b710-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b710-148">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b710-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b710-149">標準プロパティ名と MAPI 名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7b710-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b710-150">MAPI 名と標準プロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7b710-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

