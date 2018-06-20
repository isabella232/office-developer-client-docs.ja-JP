---
title: PidTagSelectable の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 225c435107ba79183c737ddb8e09cda1ffbd83f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803496"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="361fa-103">PidTagSelectable の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="361fa-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="361fa-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="361fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="361fa-105">一時テーブル内のエントリを選択できる場合、TRUE が格納されます。</span><span class="sxs-lookup"><span data-stu-id="361fa-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="361fa-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="361fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="361fa-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="361fa-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="361fa-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="361fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="361fa-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="361fa-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="361fa-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="361fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="361fa-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="361fa-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="361fa-112">領域:</span><span class="sxs-lookup"><span data-stu-id="361fa-112">Area:</span></span>  <br/> |<span data-ttu-id="361fa-113">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="361fa-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="361fa-114">備考</span><span class="sxs-lookup"><span data-stu-id="361fa-114">Remarks</span></span>

<span data-ttu-id="361fa-115">一時テーブルの見た目を整えるためには、主にこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="361fa-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="361fa-116">グループの見出しを示すエントリを作成するテンプレートをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="361fa-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="361fa-117">見出しの場合は FALSE にこのプロパティの設定により、ユーザーがグループに、この見出しエントリではないので実際のテンプレートのみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="361fa-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="361fa-118">このプロパティは、アドレス帳の階層テーブルに、一時テーブルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="361fa-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="361fa-119">MAPI は、2 つの方法で視覚的にアイテムをグループ化、アドレス帳プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="361fa-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="361fa-120">最初に、特定の行は、選択可能なが見出しとして機能できます。</span><span class="sxs-lookup"><span data-stu-id="361fa-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="361fa-121">2 つ目は、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用してするには、その見出しを基準にして選択可能な項目がインデントされます。</span><span class="sxs-lookup"><span data-stu-id="361fa-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="361fa-122">このプロパティは、一時アドレスを作成するのには、リストからこの項目を選択できるかどうかを示すために、このようなグループ化で使用されます。</span><span class="sxs-lookup"><span data-stu-id="361fa-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="361fa-123">などのクライアントは、fax アドレスを作成するためのいくつかのテンプレートには、表示に次のように。</span><span class="sxs-lookup"><span data-stu-id="361fa-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="361fa-124">FAX テンプレート (深さ 0、選択不可)</span><span class="sxs-lookup"><span data-stu-id="361fa-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="361fa-125">ローカル (深さ 1、選択可能です)</span><span class="sxs-lookup"><span data-stu-id="361fa-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="361fa-126">長距離 (深さ 1、選択可能です)</span><span class="sxs-lookup"><span data-stu-id="361fa-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="361fa-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="361fa-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="361fa-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="361fa-128">Protocol specifications</span></span>

<span data-ttu-id="361fa-129">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="361fa-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="361fa-130">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="361fa-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="361fa-131">[[MS OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="361fa-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="361fa-132">プロパティは、アドレス帳のテンプレートの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="361fa-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="361fa-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="361fa-133">Header files</span></span>

<span data-ttu-id="361fa-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="361fa-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="361fa-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="361fa-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="361fa-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="361fa-136">Mapitags.h</span></span>
  
> <span data-ttu-id="361fa-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="361fa-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="361fa-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="361fa-138">See also</span></span>



[<span data-ttu-id="361fa-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="361fa-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="361fa-140">PidTagFolderType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="361fa-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="361fa-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="361fa-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="361fa-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="361fa-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="361fa-143">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="361fa-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="361fa-144">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="361fa-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

