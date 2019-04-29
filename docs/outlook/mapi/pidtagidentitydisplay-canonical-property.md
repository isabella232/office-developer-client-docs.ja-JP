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
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="cbf40-103">PidTagIdentityDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cbf40-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="cbf40-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbf40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbf40-105">メッセージングシステム内で定義される、サービスプロバイダーの id の表示名を含みます。</span><span class="sxs-lookup"><span data-stu-id="cbf40-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbf40-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cbf40-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbf40-107">PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="cbf40-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="cbf40-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cbf40-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbf40-109">0x3e00</span><span class="sxs-lookup"><span data-stu-id="cbf40-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="cbf40-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cbf40-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbf40-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cbf40-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cbf40-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cbf40-112">Area:</span></span>  <br/> |<span data-ttu-id="cbf40-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="cbf40-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbf40-114">注釈</span><span class="sxs-lookup"><span data-stu-id="cbf40-114">Remarks</span></span>

<span data-ttu-id="cbf40-115">これらのプロパティは、オブジェクトのプロパティとして表示されませんが、ステータステーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="cbf40-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="cbf40-116">これは、サービスプロバイダーの id の一部であり、状態テーブルの行を公開します。</span><span class="sxs-lookup"><span data-stu-id="cbf40-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="cbf40-117">通常、プロバイダーの id は、サーバー上でそのアカウントを参照しますが、メッセージングシステム内でプロバイダーが定義する任意の表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="cbf40-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="cbf40-118">すべての id プロパティを提供するサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="cbf40-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="cbf40-119">同じメッセージサービスに属するプロバイダーは、identity プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbf40-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cbf40-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cbf40-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cbf40-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cbf40-121">Header files</span></span>

<span data-ttu-id="cbf40-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbf40-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbf40-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cbf40-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbf40-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="cbf40-124">Mapitags.h</span></span>
  
> <span data-ttu-id="cbf40-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cbf40-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbf40-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbf40-126">See also</span></span>



[<span data-ttu-id="cbf40-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="cbf40-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="cbf40-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cbf40-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbf40-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cbf40-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbf40-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cbf40-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbf40-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cbf40-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

