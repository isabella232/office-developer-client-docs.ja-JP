---
title: PidTagDelegateFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359900"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="1233c-103">PidTagDelegateFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1233c-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1233c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1233c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1233c-105">代理人が委任者のプライベートメッセージオブジェクトを表示できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1233c-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1233c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1233c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1233c-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1233c-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1233c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1233c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1233c-109">0x686b</span><span class="sxs-lookup"><span data-stu-id="1233c-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="1233c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1233c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1233c-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="1233c-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="1233c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1233c-112">Area:</span></span>  <br/> |<span data-ttu-id="1233c-113">メッセージクラスで定義された、パススルーテーブル</span><span class="sxs-lookup"><span data-stu-id="1233c-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1233c-114">解説</span><span class="sxs-lookup"><span data-stu-id="1233c-114">Remarks</span></span>

<span data-ttu-id="1233c-115">このプロパティの各エントリには、次のいずれかの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1233c-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="1233c-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="1233c-116">**Flag**</span></span>|<span data-ttu-id="1233c-117">**値**</span><span class="sxs-lookup"><span data-stu-id="1233c-117">**Value**</span></span>|<span data-ttu-id="1233c-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="1233c-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1233c-119">hideprivate</span><span class="sxs-lookup"><span data-stu-id="1233c-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="1233c-120">.0</span><span class="sxs-lookup"><span data-stu-id="1233c-120">0</span></span>  <br/> |<span data-ttu-id="1233c-121">代理人は、プライベートメッセージオブジェクトを表示できません。</span><span class="sxs-lookup"><span data-stu-id="1233c-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="1233c-122">showprivate</span><span class="sxs-lookup"><span data-stu-id="1233c-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="1233c-123">1-d</span><span class="sxs-lookup"><span data-stu-id="1233c-123">1</span></span>  <br/> |<span data-ttu-id="1233c-124">代理人は、プライベートメッセージオブジェクトを表示することを許可されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1233c-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="1233c-125">このプロパティは、デリゲート情報オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1233c-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="1233c-126">"showprivate" という値は、委任者がプライベートメッセージオブジェクトを表示するように指定していることを示します。</span><span class="sxs-lookup"><span data-stu-id="1233c-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="1233c-127">この設定は、代理人が校閲者、作成者、または編集者の役割を持つすべてのフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1233c-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1233c-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1233c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1233c-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1233c-129">Protocol specifications</span></span>

<span data-ttu-id="1233c-130">[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1233c-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1233c-131">代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。</span><span class="sxs-lookup"><span data-stu-id="1233c-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1233c-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1233c-132">Header files</span></span>

<span data-ttu-id="1233c-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1233c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="1233c-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1233c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="1233c-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1233c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="1233c-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1233c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1233c-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="1233c-137">See also</span></span>



[<span data-ttu-id="1233c-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1233c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1233c-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1233c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1233c-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1233c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1233c-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1233c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

