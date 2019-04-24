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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359018"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="ffc84-103">PidTagSelectable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffc84-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="ffc84-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffc84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffc84-105">1回限りのテーブル内の項目を選択できる場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffc84-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ffc84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffc84-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="ffc84-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="ffc84-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ffc84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ffc84-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="ffc84-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="ffc84-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ffc84-110">Data type:</span></span>  <br/> |<span data-ttu-id="ffc84-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ffc84-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ffc84-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ffc84-112">Area:</span></span>  <br/> |<span data-ttu-id="ffc84-113">アドレス帳コンテナー</span><span class="sxs-lookup"><span data-stu-id="ffc84-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffc84-114">解説</span><span class="sxs-lookup"><span data-stu-id="ffc84-114">Remarks</span></span>

<span data-ttu-id="ffc84-115">このプロパティは、1回限りのテーブルの表示形式に主に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="ffc84-116">テンプレートは、グループの見出しを示すエントリを作成することによってグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="ffc84-117">見出しに対してこのプロパティを FALSE に設定すると、ユーザーはグループ内の実際のテンプレートのみを選択できるようになり、この見出しエントリは選択できません。</span><span class="sxs-lookup"><span data-stu-id="ffc84-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="ffc84-118">このプロパティは、アドレス帳の階層テーブルではなく、1回限りのテーブルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="ffc84-119">MAPI では、アドレス帳プロバイダーは2つの方法でアイテムを視覚的にグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="ffc84-120">最初に、特定の行を unselectable にして見出しとして機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="ffc84-121">次に、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用して、選択可能なアイテムを見出しに対してインデントすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="ffc84-122">このプロパティは、このようなグループ化で、この項目をリストから選択して1回限りのアドレスを作成できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ffc84-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="ffc84-123">たとえば、クライアントに fax アドレスを作成するためのテンプレートがいくつかある場合は、次のように表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="ffc84-124">FAX テンプレート (深さ0、選択不可)</span><span class="sxs-lookup"><span data-stu-id="ffc84-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="ffc84-125">ローカル (深さ1、選択可能)</span><span class="sxs-lookup"><span data-stu-id="ffc84-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="ffc84-126">長距離 (深さ1、選択可能な)</span><span class="sxs-lookup"><span data-stu-id="ffc84-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ffc84-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ffc84-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffc84-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ffc84-128">Protocol specifications</span></span>

<span data-ttu-id="ffc84-129">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffc84-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffc84-130">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffc84-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffc84-131">[[OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffc84-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffc84-132">アドレス帳テンプレートで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffc84-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffc84-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ffc84-133">Header files</span></span>

<span data-ttu-id="ffc84-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffc84-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffc84-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ffc84-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="ffc84-136">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ffc84-136">Mapitags.h</span></span>
  
> <span data-ttu-id="ffc84-137">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffc84-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffc84-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffc84-138">See also</span></span>



[<span data-ttu-id="ffc84-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="ffc84-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="ffc84-140">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffc84-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="ffc84-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ffc84-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffc84-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ffc84-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffc84-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffc84-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffc84-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ffc84-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

