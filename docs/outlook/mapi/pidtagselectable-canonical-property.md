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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359018"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="626f4-103">PidTagSelectable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="626f4-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="626f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="626f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="626f4-105">一時テーブル内のエントリを選択できる場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="626f4-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="626f4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="626f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="626f4-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="626f4-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="626f4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="626f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="626f4-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="626f4-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="626f4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="626f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="626f4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="626f4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="626f4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="626f4-112">Area:</span></span>  <br/> |<span data-ttu-id="626f4-113">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="626f4-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626f4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="626f4-114">Remarks</span></span>

<span data-ttu-id="626f4-115">このプロパティは、主に 1 回のテーブルの視覚的な書式設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="626f4-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="626f4-116">テンプレートは、グループの見出しを示すエントリを作成してグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="626f4-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="626f4-117">見出しに対してこのプロパティを FALSE に設定すると、ユーザーはグループ内の実際のテンプレートのみを選択し、この見出しエントリは選択できます。</span><span class="sxs-lookup"><span data-stu-id="626f4-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="626f4-118">このプロパティは、アドレス帳階層テーブルではなく、1 回限定のテーブルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="626f4-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="626f4-119">MAPI を使用すると、アドレス帳プロバイダーは 2 つの方法でアイテムを視覚的にグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="626f4-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="626f4-120">最初に、特定の行は選択できない状態で見出しとして機能します。</span><span class="sxs-lookup"><span data-stu-id="626f4-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="626f4-121">次に、選択できる項目を見出しに対してインデントするには、PR_DEPTH **(** [PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="626f4-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="626f4-122">このプロパティは、このアイテムをリストから選択して 1 回きりアドレスを作成できるかどうかを示すために、このようなグループ化で使用されます。</span><span class="sxs-lookup"><span data-stu-id="626f4-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="626f4-123">たとえば、クライアントに FAX アドレスを作成する複数のテンプレートがある場合、次のように表示できます。</span><span class="sxs-lookup"><span data-stu-id="626f4-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="626f4-124">FAX テンプレート (深度 0、選択不可)</span><span class="sxs-lookup"><span data-stu-id="626f4-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="626f4-125">ローカル (深度 1、選択可能)</span><span class="sxs-lookup"><span data-stu-id="626f4-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="626f4-126">長距離 (深度 1、選択可能)</span><span class="sxs-lookup"><span data-stu-id="626f4-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="626f4-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="626f4-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="626f4-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="626f4-128">Protocol specifications</span></span>

<span data-ttu-id="626f4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626f4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626f4-130">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="626f4-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="626f4-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="626f4-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="626f4-132">アドレス帳テンプレートで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="626f4-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="626f4-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="626f4-133">Header files</span></span>

<span data-ttu-id="626f4-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="626f4-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="626f4-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="626f4-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="626f4-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="626f4-136">Mapitags.h</span></span>
  
> <span data-ttu-id="626f4-137">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="626f4-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="626f4-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="626f4-138">See also</span></span>



[<span data-ttu-id="626f4-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="626f4-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="626f4-140">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="626f4-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="626f4-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="626f4-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="626f4-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="626f4-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="626f4-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="626f4-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="626f4-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="626f4-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

