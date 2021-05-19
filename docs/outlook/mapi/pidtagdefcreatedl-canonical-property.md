---
title: PidTagDefCreateDl 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417792"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="a0735-103">PidTagDefCreateDl 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0735-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="a0735-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0735-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0735-105">既定の配布リストのテンプレート エントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a0735-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0735-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a0735-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0735-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="a0735-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="a0735-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a0735-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a0735-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="a0735-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="a0735-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a0735-110">Data type:</span></span>  <br/> |<span data-ttu-id="a0735-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0735-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0735-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a0735-112">Area:</span></span>  <br/> |<span data-ttu-id="a0735-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="a0735-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0735-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a0735-114">Remarks</span></span>

<span data-ttu-id="a0735-115">クライアント アプリケーションは、このプロパティを使用してコンテナー内に配布リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0735-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="a0735-116">エントリの作成のサポートは、アドレス帳コンテナーではオプションです。このプロパティをサポートしていないユーザーは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a0735-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="a0735-117">このプロパティは、配布リストの PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示されるエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0735-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="a0735-118">識別子を取得した後、クライアントは [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドの呼び出しで識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0735-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="a0735-119">このエントリは、既定の配布リストのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="a0735-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a0735-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a0735-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a0735-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a0735-121">Header files</span></span>

<span data-ttu-id="a0735-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0735-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0735-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0735-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="a0735-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a0735-124">Mapitags.h</span></span>
  
> <span data-ttu-id="a0735-125">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="a0735-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0735-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0735-126">See also</span></span>



[<span data-ttu-id="a0735-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a0735-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="a0735-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a0735-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0735-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a0735-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0735-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a0735-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0735-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a0735-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

