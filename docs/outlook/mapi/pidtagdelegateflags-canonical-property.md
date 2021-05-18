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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359900"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="c7681-103">PidTagDelegateFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7681-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c7681-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7681-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7681-105">代理人が委任者のプライベート メッセージ オブジェクトを表示できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7681-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7681-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c7681-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7681-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c7681-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c7681-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c7681-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7681-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="c7681-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="c7681-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c7681-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7681-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c7681-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c7681-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c7681-112">Area:</span></span>  <br/> |<span data-ttu-id="c7681-113">メッセージ クラス定義の送信可能</span><span class="sxs-lookup"><span data-stu-id="c7681-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7681-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c7681-114">Remarks</span></span>

<span data-ttu-id="c7681-115">このプロパティの各エントリは、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7681-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="c7681-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c7681-116">**Flag**</span></span>|<span data-ttu-id="c7681-117">**値**</span><span class="sxs-lookup"><span data-stu-id="c7681-117">**Value**</span></span>|<span data-ttu-id="c7681-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="c7681-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7681-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="c7681-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="c7681-120">0</span><span class="sxs-lookup"><span data-stu-id="c7681-120">0</span></span>  <br/> |<span data-ttu-id="c7681-121">代理人は、プライベート メッセージ オブジェクトの表示を許可しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7681-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="c7681-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="c7681-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="c7681-123">1</span><span class="sxs-lookup"><span data-stu-id="c7681-123">1</span></span>  <br/> |<span data-ttu-id="c7681-124">代理人は、プライベート メッセージ オブジェクトの表示を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7681-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="c7681-125">このプロパティは、デリゲート情報オブジェクトで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7681-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="c7681-126">"ShowPrivate" の値は、ユーザーがプライベート メッセージ オブジェクトを表示する必要がある場合を示します。</span><span class="sxs-lookup"><span data-stu-id="c7681-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="c7681-127">この基本設定は、代理人がレビューアー、作成者、または編集者の役割を持つすべてのフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c7681-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7681-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c7681-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7681-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c7681-129">Protocol specifications</span></span>

<span data-ttu-id="c7681-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7681-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7681-131">メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7681-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7681-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c7681-132">Header files</span></span>

<span data-ttu-id="c7681-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7681-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7681-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c7681-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7681-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c7681-135">Mapitags.h</span></span>
  
> <span data-ttu-id="c7681-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c7681-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7681-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7681-137">See also</span></span>



[<span data-ttu-id="c7681-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c7681-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7681-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7681-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7681-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c7681-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7681-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c7681-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

