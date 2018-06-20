---
title: PidTagOriginalAuthorName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803049"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="02b92-103">PidTagOriginalAuthorName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="02b92-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="02b92-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02b92-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02b92-105">転送または返信する前にメッセージは、メッセージの最初のバージョンの作成者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02b92-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02b92-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="02b92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02b92-107">PR_ORIGINAL_AUTHOR_NAME、PR_ORIGINAL_AUTHOR_NAME_A、PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="02b92-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="02b92-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="02b92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02b92-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="02b92-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="02b92-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="02b92-110">Data type:</span></span>  <br/> |<span data-ttu-id="02b92-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="02b92-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="02b92-112">領域:</span><span class="sxs-lookup"><span data-stu-id="02b92-112">Area:</span></span>  <br/> |<span data-ttu-id="02b92-113">Email</span><span class="sxs-lookup"><span data-stu-id="02b92-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02b92-114">備考</span><span class="sxs-lookup"><span data-stu-id="02b92-114">Remarks</span></span>

<span data-ttu-id="02b92-115">これらのプロパティでは、メッセージの作成者のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="02b92-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="02b92-116">メッセージの最初の提出書類は、クライアント アプリケーションは、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) の値にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02b92-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="02b92-117">メッセージを転送または返信するときは変更されません。</span><span class="sxs-lookup"><span data-stu-id="02b92-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="02b92-118">ローカルのメッセージング ドメインの外部からの情報の保持の元の作成者プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="02b92-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="02b92-119">別のメッセージング ドメインからメッセージが到着するなど、インターネットからこれらのプロパティは、元の情報が失われていないことを確認する方法。</span><span class="sxs-lookup"><span data-stu-id="02b92-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02b92-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="02b92-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02b92-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="02b92-121">Protocol specifications</span></span>

<span data-ttu-id="02b92-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02b92-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02b92-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="02b92-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02b92-124">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02b92-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02b92-125">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="02b92-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02b92-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="02b92-126">Header files</span></span>

<span data-ttu-id="02b92-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02b92-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="02b92-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="02b92-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="02b92-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02b92-129">Mapitags.h</span></span>
  
> <span data-ttu-id="02b92-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="02b92-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02b92-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="02b92-131">See also</span></span>



[<span data-ttu-id="02b92-132">PidTagDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="02b92-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="02b92-133">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="02b92-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02b92-134">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="02b92-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02b92-135">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="02b92-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02b92-136">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="02b92-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

