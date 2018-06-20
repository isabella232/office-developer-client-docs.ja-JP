---
title: PidTagDefCreateDl の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802674"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="23a22-103">PidTagDefCreateDl の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="23a22-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="23a22-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23a22-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23a22-105">既定の配布リストのテンプレートのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23a22-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23a22-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="23a22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23a22-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="23a22-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="23a22-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="23a22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23a22-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="23a22-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="23a22-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="23a22-110">Data type:</span></span>  <br/> |<span data-ttu-id="23a22-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="23a22-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="23a22-112">領域:</span><span class="sxs-lookup"><span data-stu-id="23a22-112">Area:</span></span>  <br/> |<span data-ttu-id="23a22-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="23a22-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23a22-114">備考</span><span class="sxs-lookup"><span data-stu-id="23a22-114">Remarks</span></span>

<span data-ttu-id="23a22-115">クライアント アプリケーションでは、このプロパティを使用して、コンテナー内の配布リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="23a22-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="23a22-116">エントリの作成のサポートはオプションのアドレス帳コンテナーです。サポートしていないものは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="23a22-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="23a22-117">このプロパティでは、配布リストの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティで表示可能なエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a22-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="23a22-118">Id を入手すると、クライアントは、それを[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドの呼び出しで使用します。</span><span class="sxs-lookup"><span data-stu-id="23a22-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="23a22-119">エントリは、既定の配布リスト用のテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="23a22-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23a22-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23a22-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="23a22-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23a22-121">Header files</span></span>

<span data-ttu-id="23a22-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23a22-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="23a22-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23a22-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="23a22-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23a22-124">Mapitags.h</span></span>
  
> <span data-ttu-id="23a22-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23a22-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23a22-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="23a22-126">See also</span></span>



[<span data-ttu-id="23a22-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="23a22-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="23a22-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23a22-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23a22-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23a22-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23a22-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="23a22-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23a22-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="23a22-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

