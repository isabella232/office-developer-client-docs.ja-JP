---
title: PidTagSearchRecipientEmailBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359158"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="7d921-103">PidTagSearchRecipientEmailBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d921-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="7d921-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d921-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d921-105">ストア上の未送信メッセージの**BCC**行に指定されている受信者の電子メールアドレスまたは表示名の一覧で、クエリが行われている Unicode 文字列が格納されています。</span><span class="sxs-lookup"><span data-stu-id="7d921-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7d921-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7d921-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d921-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="7d921-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="7d921-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7d921-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d921-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="7d921-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="7d921-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="7d921-110">Property type:</span></span>  <br/> |<span data-ttu-id="7d921-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d921-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7d921-112">接続</span><span class="sxs-lookup"><span data-stu-id="7d921-112">Access:</span></span>  <br/> |<span data-ttu-id="7d921-113">検索</span><span class="sxs-lookup"><span data-stu-id="7d921-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d921-114">解説</span><span class="sxs-lookup"><span data-stu-id="7d921-114">Remarks</span></span>

<span data-ttu-id="7d921-115">このプロパティは、送受信されたメッセージには BCC 情報が含まれていないため、送信されていないストアのメッセージのみに関連します。</span><span class="sxs-lookup"><span data-stu-id="7d921-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7d921-116">この MAPI 制限タグは、ブラインドカーボンコピーとしてメッセージが送信される電子メールアドレスまたは表示名を検索するときに使用されますが、現在所有しているダウンロード可能なヘッダーファイルでは定義されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d921-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="7d921-117">コードに追加するには、次の値を使用します。 >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="7d921-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d921-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7d921-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d921-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7d921-119">Protocol specifications</span></span>

<span data-ttu-id="7d921-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d921-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d921-121">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d921-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d921-122">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d921-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d921-123">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d921-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d921-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7d921-124">Header files</span></span>

<span data-ttu-id="7d921-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d921-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d921-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d921-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d921-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7d921-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7d921-128">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d921-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d921-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d921-129">See also</span></span>



[<span data-ttu-id="7d921-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d921-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d921-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d921-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d921-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7d921-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d921-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7d921-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

