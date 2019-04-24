---
title: PidTagSearchAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336324"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="06278-103">PidTagSearchAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06278-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="06278-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06278-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06278-105">ストア上の添付ファイルコンテンツで照会されている Unicode 文字列が格納されています。</span><span class="sxs-lookup"><span data-stu-id="06278-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="06278-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06278-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06278-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="06278-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="06278-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06278-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06278-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="06278-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="06278-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="06278-110">Property type:</span></span>  <br/> |<span data-ttu-id="06278-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="06278-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="06278-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="06278-112">Area:</span></span>  <br/> |<span data-ttu-id="06278-113">検索</span><span class="sxs-lookup"><span data-stu-id="06278-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="06278-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06278-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="06278-115">添付ファイルのコンテンツを検索するときに使用されるこの MAPI 制限タグは、現在持っているダウンロード可能なヘッダーファイルでは定義されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="06278-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="06278-116">コードに追加するには、次の値を使用します。 >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="06278-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="06278-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="06278-117">Protocol specifications</span></span>

<span data-ttu-id="06278-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06278-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06278-119">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="06278-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06278-120">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06278-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06278-121">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="06278-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06278-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="06278-122">Header files</span></span>

<span data-ttu-id="06278-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06278-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="06278-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06278-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="06278-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="06278-125">Mapitags.h</span></span>
  
> <span data-ttu-id="06278-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06278-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06278-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="06278-127">See also</span></span>



[<span data-ttu-id="06278-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="06278-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06278-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06278-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06278-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06278-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06278-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="06278-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

