---
title: PidTagSearchAttachments の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803484"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="1a570-103">PidTagSearchAttachments の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1a570-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="1a570-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a570-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a570-105">ストア内の添付ファイルの内容の照会中に Unicode 文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a570-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1a570-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1a570-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a570-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="1a570-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="1a570-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1a570-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a570-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="1a570-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="1a570-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="1a570-110">Property type:</span></span>  <br/> |<span data-ttu-id="1a570-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a570-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a570-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1a570-112">Area:</span></span>  <br/> |<span data-ttu-id="1a570-113">検索</span><span class="sxs-lookup"><span data-stu-id="1a570-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1a570-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1a570-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="1a570-115">添付ファイルの内容を検索するときに使用されるこの MAPI 制限タグは可能性があります、現在あるダウンロード可能なヘッダー ファイルで定義されていません。</span><span class="sxs-lookup"><span data-stu-id="1a570-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="1a570-116">次の値を使用して、コードに追加できます >。`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="1a570-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="1a570-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1a570-117">Protocol specifications</span></span>

<span data-ttu-id="1a570-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a570-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a570-119">関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a570-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a570-120">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a570-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a570-121">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a570-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a570-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1a570-122">Header files</span></span>

<span data-ttu-id="1a570-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a570-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a570-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1a570-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a570-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a570-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1a570-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a570-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a570-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a570-127">See also</span></span>



[<span data-ttu-id="1a570-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a570-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a570-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1a570-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a570-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1a570-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a570-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1a570-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

