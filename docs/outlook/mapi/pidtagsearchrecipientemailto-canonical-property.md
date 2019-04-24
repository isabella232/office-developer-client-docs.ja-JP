---
title: PidTagSearchRecipientEmailTo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358920"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="c9ea0-103">PidTagSearchRecipientEmailTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9ea0-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="c9ea0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ea0-105">ストア上のメッセージの [宛先] 行に記載されている受信者の電子メールアドレスまたは表示名\*\*\*\* の一覧で、クエリが行われている Unicode 文字列が格納されています。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="c9ea0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c9ea0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9ea0-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="c9ea0-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="c9ea0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c9ea0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9ea0-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="c9ea0-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="c9ea0-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="c9ea0-110">Property type:</span></span>  <br/> |<span data-ttu-id="c9ea0-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9ea0-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c9ea0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c9ea0-112">Area:</span></span>  <br/> |<span data-ttu-id="c9ea0-113">検索</span><span class="sxs-lookup"><span data-stu-id="c9ea0-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c9ea0-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c9ea0-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="c9ea0-115">この MAPI 制限タグは、メッセージが送信される電子メールアドレスまたは表示名を検索するときに使用しますが、現在所有しているダウンロード可能なヘッダーファイルでは定義されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="c9ea0-116">コードに追加するには、次の値を使用します。 >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="c9ea0-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="c9ea0-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c9ea0-117">Protocol specifications</span></span>

<span data-ttu-id="c9ea0-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9ea0-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9ea0-119">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9ea0-120">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9ea0-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9ea0-121">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9ea0-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="c9ea0-122">Header files</span></span>

<span data-ttu-id="c9ea0-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9ea0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9ea0-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9ea0-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="c9ea0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c9ea0-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c9ea0-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9ea0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9ea0-127">See also</span></span>



[<span data-ttu-id="c9ea0-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c9ea0-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9ea0-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c9ea0-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9ea0-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c9ea0-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9ea0-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c9ea0-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

