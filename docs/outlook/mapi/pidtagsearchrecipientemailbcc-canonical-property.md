---
title: PidTagSearchRecipientEmailBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359158"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="fa16d-103">PidTagSearchRecipientEmailBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa16d-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="fa16d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa16d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa16d-105">ストア上の未送信メッセージの **BCC** 行でアドレス指定された受信者の電子メール アドレスまたは表示名の一覧でクエリされている Unicode 文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa16d-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="fa16d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fa16d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa16d-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="fa16d-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="fa16d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fa16d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa16d-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="fa16d-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="fa16d-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="fa16d-110">Property type:</span></span>  <br/> |<span data-ttu-id="fa16d-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fa16d-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fa16d-112">アクセス:</span><span class="sxs-lookup"><span data-stu-id="fa16d-112">Access:</span></span>  <br/> |<span data-ttu-id="fa16d-113">検索</span><span class="sxs-lookup"><span data-stu-id="fa16d-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa16d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fa16d-114">Remarks</span></span>

<span data-ttu-id="fa16d-115">このプロパティは、送信または受信されたメッセージに BCC 情報が含まれているため、送信されていないストア上のメッセージにのみ関連します。</span><span class="sxs-lookup"><span data-stu-id="fa16d-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fa16d-116">この MAPI 制限タグは、メッセージがブラインド カーボン コピーとして送信される電子メール アドレスまたは表示名を検索するときに使用され、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fa16d-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="fa16d-117">次の値を使用して、コードに追加できます。>  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="fa16d-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fa16d-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fa16d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa16d-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fa16d-119">Protocol specifications</span></span>

<span data-ttu-id="fa16d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa16d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa16d-121">関連するプロトコル仕様へのMicrosoft Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="fa16d-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa16d-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa16d-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa16d-123">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fa16d-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa16d-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fa16d-124">Header files</span></span>

<span data-ttu-id="fa16d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa16d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa16d-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fa16d-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa16d-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fa16d-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fa16d-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fa16d-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa16d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa16d-129">See also</span></span>



[<span data-ttu-id="fa16d-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fa16d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa16d-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fa16d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa16d-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fa16d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa16d-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fa16d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

