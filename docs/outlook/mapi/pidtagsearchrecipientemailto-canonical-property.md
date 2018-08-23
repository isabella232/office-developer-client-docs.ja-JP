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
ms.openlocfilehash: 5d6c029ba91b6b3489d3f6544ead6788760363a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803497"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="86252-103">PidTagSearchRecipientEmailTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="86252-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="86252-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86252-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86252-105">照会中の電子メール アドレスまたはストア内のメッセージの [**宛先**] 行でアドレス指定された受信者の表示名の一覧で、Unicode 文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86252-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="86252-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="86252-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86252-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="86252-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="86252-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="86252-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86252-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="86252-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="86252-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="86252-110">Property type:</span></span>  <br/> |<span data-ttu-id="86252-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="86252-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="86252-112">領域:</span><span class="sxs-lookup"><span data-stu-id="86252-112">Area:</span></span>  <br/> |<span data-ttu-id="86252-113">検索</span><span class="sxs-lookup"><span data-stu-id="86252-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="86252-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="86252-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="86252-115">この MAPI 制限のタグ、電子メール アドレスを検索または表示名のメッセージを送信するときに使用しない現在あるダウンロード可能なヘッダー ファイルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="86252-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="86252-116">次の値を使用して、コードに追加できます >。`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="86252-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="86252-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="86252-117">Protocol specifications</span></span>

<span data-ttu-id="86252-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86252-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86252-119">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="86252-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86252-120">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86252-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86252-121">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="86252-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86252-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="86252-122">Header files</span></span>

<span data-ttu-id="86252-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86252-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="86252-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="86252-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="86252-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86252-125">Mapitags.h</span></span>
  
> <span data-ttu-id="86252-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="86252-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86252-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="86252-127">See also</span></span>



[<span data-ttu-id="86252-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86252-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86252-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="86252-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86252-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86252-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86252-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="86252-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

