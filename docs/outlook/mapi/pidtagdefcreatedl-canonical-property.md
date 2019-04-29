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
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="f5f3c-103">PidTagDefCreateDl 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5f3c-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="f5f3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5f3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5f3c-105">既定の配布リストのテンプレートエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5f3c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f5f3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5f3c-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="f5f3c-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="f5f3c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f5f3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5f3c-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="f5f3c-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="f5f3c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f5f3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5f3c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f5f3c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f5f3c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f5f3c-112">Area:</span></span>  <br/> |<span data-ttu-id="f5f3c-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="f5f3c-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5f3c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f5f3c-114">Remarks</span></span>

<span data-ttu-id="f5f3c-115">クライアントアプリケーションは、このプロパティを使用して、コンテナー内に配布リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="f5f3c-116">エントリ作成のサポートは、アドレス帳コンテナーでは省略可能です。これをサポートしていないものは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="f5f3c-117">このプロパティは、配布リストの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示できるエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="f5f3c-118">識別子を取得した後、クライアントは[IABContainer:: createentry](iabcontainer-createentry.md)メソッドへの呼び出しでその識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="f5f3c-119">このエントリは、既定の配布リストのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5f3c-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f5f3c-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f5f3c-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f5f3c-121">Header files</span></span>

<span data-ttu-id="f5f3c-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5f3c-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5f3c-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5f3c-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f5f3c-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f5f3c-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5f3c-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5f3c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5f3c-126">See also</span></span>



[<span data-ttu-id="f5f3c-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f5f3c-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="f5f3c-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f5f3c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5f3c-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5f3c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5f3c-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f5f3c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5f3c-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f5f3c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

