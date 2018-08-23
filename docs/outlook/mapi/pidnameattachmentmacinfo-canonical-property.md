---
title: PidNameAttachmentMacInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAttachmentMacInfo
api_type:
- COM
ms.assetid: c46656d5-2cb1-45eb-9f66-9c2b6e3315cf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 633a7e0ea7cc2b6ffdbc555e2e470ec66ef77f8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565607"
---
# <a name="pidnameattachmentmacinfo-canonical-property"></a><span data-ttu-id="71094-103">PidNameAttachmentMacInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="71094-103">PidNameAttachmentMacInfo Canonical Property</span></span>

  
  
<span data-ttu-id="71094-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71094-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71094-105">Macintosh ベースの電子メール クライアントによって使用される適切なのヘッダーとリソース フォーク データで構成されている [RFC3282] 添付ファイルの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71094-105">Contains an [RFC3282] attachment value that is comprised of appropriate header and resource fork data used by Macintosh-based email clients.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71094-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="71094-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="71094-107">なし</span><span class="sxs-lookup"><span data-stu-id="71094-107">None</span></span>  <br/> |
|<span data-ttu-id="71094-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="71094-108">Property set:</span></span>  <br/> |<span data-ttu-id="71094-109">PSETID_Attachment</span><span class="sxs-lookup"><span data-stu-id="71094-109">PSETID_Attachment</span></span>  <br/> |
|<span data-ttu-id="71094-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="71094-110">Property name:</span></span>  <br/> |<span data-ttu-id="71094-111">AttachmentMacInfo</span><span class="sxs-lookup"><span data-stu-id="71094-111">AttachmentMacInfo</span></span>  <br/> |
|<span data-ttu-id="71094-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="71094-112">Data type:</span></span>  <br/> |<span data-ttu-id="71094-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="71094-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="71094-114">領域:</span><span class="sxs-lookup"><span data-stu-id="71094-114">Area:</span></span>  <br/> |<span data-ttu-id="71094-115">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="71094-115">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71094-116">注釈</span><span class="sxs-lookup"><span data-stu-id="71094-116">Remarks</span></span>

<span data-ttu-id="71094-117">詳細については、MS OXCMAIL セクション 2.2.4.2 アップル ・ ファイル ・ フォーマットを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71094-117">For more information, see MS-OXCMAIL section 2.2.4.2 Apple File Formats.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71094-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="71094-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71094-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="71094-119">Protocol specifications</span></span>

<span data-ttu-id="71094-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71094-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71094-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="71094-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71094-122">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71094-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71094-123">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="71094-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71094-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="71094-124">Header files</span></span>

<span data-ttu-id="71094-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71094-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="71094-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="71094-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71094-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="71094-127">See also</span></span>



[<span data-ttu-id="71094-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="71094-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71094-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="71094-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71094-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="71094-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71094-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="71094-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

