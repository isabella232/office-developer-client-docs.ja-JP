---
title: PidTagOriginalAuthorEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEntryId
api_type:
- COM
ms.assetid: 34654660-b003-42f5-9fcd-24ebaccd735d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 03244fb240231a105b0a25a0797c13b9bf7f7a80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803043"
---
# <a name="pidtagoriginalauthorentryid-canonical-property"></a><span data-ttu-id="072d3-103">PidTagOriginalAuthorEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="072d3-103">PidTagOriginalAuthorEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="072d3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="072d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="072d3-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="072d3-105">Contains the entry identifier of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="072d3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="072d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="072d3-107">PR_ORIGINAL_AUTHOR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="072d3-107">PR_ORIGINAL_AUTHOR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="072d3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="072d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="072d3-109">0x004C</span><span class="sxs-lookup"><span data-stu-id="072d3-109">0x004C</span></span>  <br/> |
|<span data-ttu-id="072d3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="072d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="072d3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="072d3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="072d3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="072d3-112">Area:</span></span>  <br/> |<span data-ttu-id="072d3-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="072d3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="072d3-114">備考</span><span class="sxs-lookup"><span data-stu-id="072d3-114">Remarks</span></span>

<span data-ttu-id="072d3-115">このプロパティは、メッセージの作成者のアドレスのプロパティのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="072d3-115">This property is one of the address properties for the author of a message.</span></span> <span data-ttu-id="072d3-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) の値にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="072d3-116">At first submission of the message, the client application should set this property to the value of **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span></span> <span data-ttu-id="072d3-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="072d3-117">It is never changed when the message is forwarded or replied to.</span></span> 
  
<span data-ttu-id="072d3-118">元の作成者プロパティは、ローカルのメッセージング ドメインの外部からの情報の保持に使用できます。</span><span class="sxs-lookup"><span data-stu-id="072d3-118">The original author property allows for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="072d3-119">このプロパティがその元の情報を保証する手段を提供する、インターネットからなど、別のメッセージング ドメインからメッセージが着信するときは、失われていません。</span><span class="sxs-lookup"><span data-stu-id="072d3-119">When a message arrives from another messaging domain, such as from the Internet, this property provides a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="072d3-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="072d3-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="072d3-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="072d3-121">Header files</span></span>

<span data-ttu-id="072d3-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="072d3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="072d3-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="072d3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="072d3-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="072d3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="072d3-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="072d3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="072d3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="072d3-126">See also</span></span>



[<span data-ttu-id="072d3-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="072d3-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="072d3-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="072d3-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="072d3-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="072d3-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="072d3-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="072d3-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

