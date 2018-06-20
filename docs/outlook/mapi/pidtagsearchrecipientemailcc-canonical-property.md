---
title: PidTagSearchRecipientEmailCc の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6fe59bf837d6123e5655e853531d6ab53393af91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803502"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="bc991-103">PidTagSearchRecipientEmailCc の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bc991-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="bc991-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc991-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc991-105">照会中の電子メール アドレスまたはストア内のメッセージの [ **CC** ] 行でアドレス指定された受信者の表示名の一覧で、Unicode 文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc991-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bc991-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bc991-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc991-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="bc991-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="bc991-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bc991-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc991-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="bc991-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="bc991-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="bc991-110">Property type:</span></span>  <br/> |<span data-ttu-id="bc991-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc991-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bc991-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bc991-112">Area:</span></span>  <br/> |<span data-ttu-id="bc991-113">検索</span><span class="sxs-lookup"><span data-stu-id="bc991-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bc991-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bc991-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="bc991-115">この MAPI 制限のタグ、電子メール アドレスを検索するか、カーボン コピーとしてメッセージを送信する名前を表示するときに使用しない、現在あるダウンロード可能なヘッダー ファイルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="bc991-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="bc991-116">次の値を使用して、コードに追加できます >。`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="bc991-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="bc991-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bc991-117">Protocol specifications</span></span>

<span data-ttu-id="bc991-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc991-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc991-119">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bc991-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bc991-120">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc991-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc991-121">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bc991-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc991-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bc991-122">Header files</span></span>

<span data-ttu-id="bc991-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc991-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc991-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bc991-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc991-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bc991-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bc991-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc991-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc991-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc991-127">See also</span></span>



[<span data-ttu-id="bc991-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc991-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc991-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc991-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc991-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bc991-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc991-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bc991-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

