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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585578"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="4996a-103">PidTagIdentityDisplay 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4996a-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="4996a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4996a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4996a-105">メッセージング システム内で定義されているように、サービス プロバイダーの id の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4996a-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4996a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4996a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4996a-107">PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="4996a-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="4996a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4996a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4996a-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="4996a-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="4996a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4996a-110">Data type:</span></span>  <br/> |<span data-ttu-id="4996a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4996a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4996a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4996a-112">Area:</span></span>  <br/> |<span data-ttu-id="4996a-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="4996a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4996a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4996a-114">Remarks</span></span>

<span data-ttu-id="4996a-115">状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとして、これらのプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="4996a-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="4996a-116">状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。</span><span class="sxs-lookup"><span data-stu-id="4996a-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="4996a-117">プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="4996a-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="4996a-118">Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4996a-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="4996a-119">同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4996a-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4996a-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4996a-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4996a-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4996a-121">Header files</span></span>

<span data-ttu-id="4996a-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4996a-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4996a-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4996a-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4996a-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4996a-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4996a-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4996a-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4996a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4996a-126">See also</span></span>



[<span data-ttu-id="4996a-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="4996a-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="4996a-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4996a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4996a-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4996a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4996a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4996a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4996a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4996a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

