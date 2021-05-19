---
title: PidTagIdentitySearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423749"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="72035-103">PidTagIdentitySearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72035-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="72035-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72035-105">メッセージング システム内で定義されているサービス プロバイダーの ID の検索キーを格納します。</span><span class="sxs-lookup"><span data-stu-id="72035-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72035-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="72035-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72035-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="72035-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="72035-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="72035-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72035-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="72035-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="72035-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="72035-110">Data type:</span></span>  <br/> |<span data-ttu-id="72035-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="72035-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="72035-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="72035-112">Area:</span></span>  <br/> |<span data-ttu-id="72035-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="72035-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72035-114">注釈</span><span class="sxs-lookup"><span data-stu-id="72035-114">Remarks</span></span>

<span data-ttu-id="72035-115">このプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、状態テーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="72035-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="72035-116">これは、状態テーブル行を公開するサービス プロバイダーの ID の一部です。</span><span class="sxs-lookup"><span data-stu-id="72035-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="72035-117">プロバイダーの ID は通常、サーバー上のアカウントを参照しますが、プロバイダーがメッセージング システム内で定義する任意の表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="72035-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="72035-118">ID プロパティを提供するサービス プロバイダーは、すべての ID プロパティを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72035-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="72035-119">同じメッセージ サービスに属するプロバイダーは、ID プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72035-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="72035-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="72035-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="72035-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="72035-121">Header files</span></span>

<span data-ttu-id="72035-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72035-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="72035-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="72035-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="72035-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="72035-124">Mapitags.h</span></span>
  
> <span data-ttu-id="72035-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="72035-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72035-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="72035-126">See also</span></span>



[<span data-ttu-id="72035-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="72035-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="72035-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="72035-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72035-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="72035-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72035-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="72035-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72035-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="72035-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

