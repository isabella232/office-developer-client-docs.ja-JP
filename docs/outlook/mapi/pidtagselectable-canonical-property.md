---
title: PidTagSelectable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383458"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="2d861-103">PidTagSelectable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d861-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="2d861-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d861-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d861-105">一時テーブル内のエントリを選択できる場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="2d861-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d861-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2d861-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d861-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="2d861-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="2d861-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2d861-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d861-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="2d861-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="2d861-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2d861-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d861-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2d861-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2d861-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2d861-112">Area:</span></span>  <br/> |<span data-ttu-id="2d861-113">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="2d861-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d861-114">備考</span><span class="sxs-lookup"><span data-stu-id="2d861-114">Remarks</span></span>

<span data-ttu-id="2d861-115">一時テーブルの見た目を整えるためには、主にこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d861-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="2d861-116">グループの見出しを示すエントリを作成するテンプレートをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="2d861-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="2d861-117">見出しの場合は FALSE にこのプロパティの設定により、ユーザーがグループに、この見出しエントリではないので実際のテンプレートのみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="2d861-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="2d861-118">このプロパティは、アドレス帳の階層テーブルに、一時テーブルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2d861-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="2d861-119">MAPI は、2 つの方法で視覚的にアイテムをグループ化、アドレス帳プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2d861-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="2d861-120">最初に、特定の行は、選択可能なが見出しとして機能できます。</span><span class="sxs-lookup"><span data-stu-id="2d861-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="2d861-121">2 つ目は、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用してするには、その見出しを基準にして選択可能な項目がインデントされます。</span><span class="sxs-lookup"><span data-stu-id="2d861-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="2d861-122">このプロパティは、一時アドレスを作成するのには、リストからこの項目を選択できるかどうかを示すために、このようなグループ化で使用されます。</span><span class="sxs-lookup"><span data-stu-id="2d861-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="2d861-123">などのクライアントは、fax アドレスを作成するためのいくつかのテンプレートには、表示に次のように。</span><span class="sxs-lookup"><span data-stu-id="2d861-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="2d861-124">FAX テンプレート (深さ 0、選択不可)</span><span class="sxs-lookup"><span data-stu-id="2d861-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="2d861-125">ローカル (深さ 1、選択可能です)</span><span class="sxs-lookup"><span data-stu-id="2d861-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="2d861-126">長距離 (深さ 1、選択可能です)</span><span class="sxs-lookup"><span data-stu-id="2d861-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d861-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2d861-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d861-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2d861-128">Protocol specifications</span></span>

<span data-ttu-id="2d861-129">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d861-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d861-130">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2d861-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d861-131">[[MS OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d861-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d861-132">プロパティは、アドレス帳のテンプレートの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d861-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d861-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2d861-133">Header files</span></span>

<span data-ttu-id="2d861-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d861-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d861-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2d861-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d861-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2d861-136">Mapitags.h</span></span>
  
> <span data-ttu-id="2d861-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2d861-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d861-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d861-138">See also</span></span>



[<span data-ttu-id="2d861-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="2d861-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="2d861-140">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d861-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="2d861-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d861-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d861-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2d861-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d861-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d861-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d861-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d861-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

