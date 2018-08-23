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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565145"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a><span data-ttu-id="22eab-103">PidTagIdentitySearchKey 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="22eab-103">PidTagIdentitySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="22eab-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22eab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22eab-105">メッセージング システム内で定義されているように、サービス プロバイダーの id の検索キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="22eab-105">Contains the search key for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22eab-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="22eab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22eab-107">PR_IDENTITY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="22eab-107">PR_IDENTITY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="22eab-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="22eab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22eab-109">0x3E05</span><span class="sxs-lookup"><span data-stu-id="22eab-109">0x3E05</span></span>  <br/> |
|<span data-ttu-id="22eab-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="22eab-110">Data type:</span></span>  <br/> |<span data-ttu-id="22eab-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="22eab-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="22eab-112">領域:</span><span class="sxs-lookup"><span data-stu-id="22eab-112">Area:</span></span>  <br/> |<span data-ttu-id="22eab-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="22eab-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22eab-114">注釈</span><span class="sxs-lookup"><span data-stu-id="22eab-114">Remarks</span></span>

<span data-ttu-id="22eab-115">状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="22eab-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="22eab-116">状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。</span><span class="sxs-lookup"><span data-stu-id="22eab-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="22eab-117">プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="22eab-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="22eab-118">Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22eab-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="22eab-119">同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22eab-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="22eab-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="22eab-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="22eab-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="22eab-121">Header files</span></span>

<span data-ttu-id="22eab-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22eab-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="22eab-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="22eab-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="22eab-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22eab-124">Mapitags.h</span></span>
  
> <span data-ttu-id="22eab-125">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="22eab-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22eab-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="22eab-126">See also</span></span>



[<span data-ttu-id="22eab-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="22eab-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="22eab-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="22eab-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22eab-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="22eab-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22eab-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22eab-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22eab-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="22eab-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

