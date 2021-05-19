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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418835"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="b132c-103">PidLidOfflineStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b132c-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b132c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b132c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b132c-105">[MS-LISTSWS] を実装するサーバー上のドキュメント ファイルの状態を決定します。</span><span class="sxs-lookup"><span data-stu-id="b132c-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b132c-106">関連付けられたプロパティ</span><span class="sxs-lookup"><span data-stu-id="b132c-106">Associated properties</span></span>  <br/> |<span data-ttu-id="b132c-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="b132c-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="b132c-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="b132c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b132c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b132c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b132c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b132c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b132c-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="b132c-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="b132c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b132c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b132c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b132c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b132c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="b132c-114">Area:</span></span>  <br/> |<span data-ttu-id="b132c-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="b132c-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b132c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="b132c-116">Remarks</span></span>

<span data-ttu-id="b132c-117">次の表に、このプロパティの値を示します。</span><span class="sxs-lookup"><span data-stu-id="b132c-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="b132c-118">**値**</span><span class="sxs-lookup"><span data-stu-id="b132c-118">**Value**</span></span>|<span data-ttu-id="b132c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b132c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b132c-120">0</span><span class="sxs-lookup"><span data-stu-id="b132c-120">0</span></span>  <br/> |<span data-ttu-id="b132c-121">ドキュメントはチェックアウトされません。</span><span class="sxs-lookup"><span data-stu-id="b132c-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="b132c-122">1</span><span class="sxs-lookup"><span data-stu-id="b132c-122">1</span></span>  <br/> |<span data-ttu-id="b132c-123">ドキュメントは現在のユーザーにチェックアウトされます。</span><span class="sxs-lookup"><span data-stu-id="b132c-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="b132c-124">2</span><span class="sxs-lookup"><span data-stu-id="b132c-124">2</span></span>  <br/> |<span data-ttu-id="b132c-125">ドキュメントはチェックアウトされませんが、現在のユーザーは現在のコンピューターで編集用に保存されたファイルのコピーを持っています。</span><span class="sxs-lookup"><span data-stu-id="b132c-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="b132c-126">このプロパティはローカルで計算され、ユーザーがアイテムを別のアカウントにドラッグしない限り、いつでもサーバーに送信されません。</span><span class="sxs-lookup"><span data-stu-id="b132c-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="b132c-127">その場合、ユーザー定義のカスタム プロパティとして扱います。</span><span class="sxs-lookup"><span data-stu-id="b132c-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b132c-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b132c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b132c-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b132c-129">Protocol specifications</span></span>

<span data-ttu-id="b132c-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="b132c-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b132c-131">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="b132c-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b132c-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b132c-132">Header files</span></span>

<span data-ttu-id="b132c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b132c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b132c-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b132c-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b132c-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b132c-135">See also</span></span>



[<span data-ttu-id="b132c-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b132c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b132c-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b132c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b132c-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b132c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b132c-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b132c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

