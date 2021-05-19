---
title: PidTagSearchRecipientEmailCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358948"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="a916c-103">PidTagSearchRecipientEmailCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a916c-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="a916c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a916c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a916c-105">ストア上のメッセージの CC 行でアドレス指定されている受信者の電子メール アドレスまたは表示名の一覧でクエリされている **Unicode** 文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a916c-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="a916c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a916c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a916c-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="a916c-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="a916c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a916c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a916c-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="a916c-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="a916c-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="a916c-110">Property type:</span></span>  <br/> |<span data-ttu-id="a916c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a916c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a916c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a916c-112">Area:</span></span>  <br/> |<span data-ttu-id="a916c-113">検索</span><span class="sxs-lookup"><span data-stu-id="a916c-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a916c-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a916c-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="a916c-115">この MAPI 制限タグは、メッセージがカーボン コピーとして送信される電子メール アドレスまたは表示名を検索するときに使用され、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a916c-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="a916c-116">次の値を使用して、コードに追加できます。>  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="a916c-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="a916c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a916c-117">Protocol specifications</span></span>

<span data-ttu-id="a916c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a916c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a916c-119">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="a916c-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a916c-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a916c-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a916c-121">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="a916c-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a916c-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a916c-122">Header files</span></span>

<span data-ttu-id="a916c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a916c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a916c-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a916c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a916c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a916c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a916c-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a916c-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a916c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a916c-127">See also</span></span>



[<span data-ttu-id="a916c-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a916c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a916c-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a916c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a916c-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a916c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a916c-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a916c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

