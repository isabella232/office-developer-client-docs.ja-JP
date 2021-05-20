---
title: PidTagIdentityDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431422"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="ff9b3-103">PidTagIdentityDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff9b3-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="ff9b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff9b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff9b3-105">メッセージング システム内で定義されているサービス プロバイダーの ID の表示名を格納します。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff9b3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ff9b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff9b3-107">PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="ff9b3-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="ff9b3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ff9b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff9b3-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="ff9b3-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="ff9b3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ff9b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff9b3-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff9b3-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ff9b3-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ff9b3-112">Area:</span></span>  <br/> |<span data-ttu-id="ff9b3-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="ff9b3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff9b3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ff9b3-114">Remarks</span></span>

<span data-ttu-id="ff9b3-115">これらのプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、状態テーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="ff9b3-116">これは、状態テーブル行を公開するサービス プロバイダーの ID の一部です。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="ff9b3-117">プロバイダーの ID は通常、サーバー上のアカウントを参照しますが、プロバイダーがメッセージング システム内で定義する任意の表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="ff9b3-118">ID プロパティを提供するサービス プロバイダーは、すべての ID プロパティを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="ff9b3-119">同じメッセージ サービスに属するプロバイダーは、ID プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ff9b3-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ff9b3-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ff9b3-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ff9b3-121">Header files</span></span>

<span data-ttu-id="ff9b3-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff9b3-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff9b3-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff9b3-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff9b3-124">Mapitags.h</span></span>
  
> <span data-ttu-id="ff9b3-125">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ff9b3-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff9b3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff9b3-126">See also</span></span>



[<span data-ttu-id="ff9b3-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="ff9b3-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="ff9b3-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ff9b3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff9b3-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ff9b3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff9b3-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ff9b3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff9b3-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ff9b3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

