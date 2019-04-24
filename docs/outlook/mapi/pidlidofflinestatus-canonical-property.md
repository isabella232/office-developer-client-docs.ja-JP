---
title: PidLidOfflineStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326300"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="cbd1a-103">PidLidOfflineStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cbd1a-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="cbd1a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbd1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbd1a-105">[MS] を実装しているサーバー上のドキュメントファイルの状態を判別します。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbd1a-106">関連付けられたプロパティ</span><span class="sxs-lookup"><span data-stu-id="cbd1a-106">Associated properties</span></span>  <br/> |<span data-ttu-id="cbd1a-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="cbd1a-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="cbd1a-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="cbd1a-108">Property set:</span></span>  <br/> |<span data-ttu-id="cbd1a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cbd1a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cbd1a-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cbd1a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cbd1a-111">0x000085b9</span><span class="sxs-lookup"><span data-stu-id="cbd1a-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="cbd1a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cbd1a-112">Data type:</span></span>  <br/> |<span data-ttu-id="cbd1a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cbd1a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cbd1a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="cbd1a-114">Area:</span></span>  <br/> |<span data-ttu-id="cbd1a-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="cbd1a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbd1a-116">解説</span><span class="sxs-lookup"><span data-stu-id="cbd1a-116">Remarks</span></span>

<span data-ttu-id="cbd1a-117">次の表に、このプロパティに指定できる値を示します。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="cbd1a-118">**値**</span><span class="sxs-lookup"><span data-stu-id="cbd1a-118">**Value**</span></span>|<span data-ttu-id="cbd1a-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="cbd1a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbd1a-120">.0</span><span class="sxs-lookup"><span data-stu-id="cbd1a-120">0</span></span>  <br/> |<span data-ttu-id="cbd1a-121">ドキュメントはチェックアウトされていません。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="cbd1a-122">1-d</span><span class="sxs-lookup"><span data-stu-id="cbd1a-122">1</span></span>  <br/> |<span data-ttu-id="cbd1a-123">ドキュメントは現在のユーザーにチェックアウトされています。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="cbd1a-124">pbm-2</span><span class="sxs-lookup"><span data-stu-id="cbd1a-124">2</span></span>  <br/> |<span data-ttu-id="cbd1a-125">ドキュメントはチェックアウトされていませんが、現在のユーザーは現在のコンピューターで編集のために保存されたファイルのコピーを持っています。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="cbd1a-126">このプロパティはローカルで計算され、ユーザーが別のアカウントにアイテムをドラッグしない限り、常にサーバーに送信されません。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="cbd1a-127">その場合は、ユーザー定義のカスタムプロパティとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cbd1a-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cbd1a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbd1a-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cbd1a-129">Protocol specifications</span></span>

<span data-ttu-id="cbd1a-130">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="cbd1a-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="cbd1a-131">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbd1a-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cbd1a-132">Header files</span></span>

<span data-ttu-id="cbd1a-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbd1a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbd1a-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cbd1a-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbd1a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbd1a-135">See also</span></span>



[<span data-ttu-id="cbd1a-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cbd1a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbd1a-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cbd1a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbd1a-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cbd1a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbd1a-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cbd1a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

