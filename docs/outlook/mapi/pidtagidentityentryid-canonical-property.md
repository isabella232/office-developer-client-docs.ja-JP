---
title: PidTagIdentityEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327931"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="44e2c-103">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44e2c-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="44e2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44e2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44e2c-105">メッセージングシステム内での定義に従って、サービスプロバイダーの id のエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="44e2c-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44e2c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44e2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44e2c-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="44e2c-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="44e2c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44e2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44e2c-109">0x3e01</span><span class="sxs-lookup"><span data-stu-id="44e2c-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="44e2c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44e2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="44e2c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="44e2c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="44e2c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44e2c-112">Area:</span></span>  <br/> |<span data-ttu-id="44e2c-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="44e2c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44e2c-114">解説</span><span class="sxs-lookup"><span data-stu-id="44e2c-114">Remarks</span></span>

<span data-ttu-id="44e2c-115">このプロパティは、オブジェクトのプロパティとして表示されませんが、ステータステーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="44e2c-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="44e2c-116">これは、サービスプロバイダーの id の一部であり、状態テーブルの行を公開します。</span><span class="sxs-lookup"><span data-stu-id="44e2c-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="44e2c-117">通常、プロバイダーの id は、サーバー上でそのアカウントを参照しますが、メッセージングシステム内でプロバイダーが定義する任意の表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="44e2c-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="44e2c-118">この proprerty は、通常、適切なアドレス帳エントリ識別子に設定されます。</span><span class="sxs-lookup"><span data-stu-id="44e2c-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="44e2c-119">すべての id プロパティを提供するサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="44e2c-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="44e2c-120">同じメッセージサービスに属するプロバイダーは、identity プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44e2c-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="44e2c-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44e2c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="44e2c-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="44e2c-122">Header files</span></span>

<span data-ttu-id="44e2c-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44e2c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="44e2c-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44e2c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="44e2c-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="44e2c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="44e2c-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="44e2c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44e2c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="44e2c-127">See also</span></span>



[<span data-ttu-id="44e2c-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="44e2c-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="44e2c-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44e2c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44e2c-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44e2c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44e2c-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44e2c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44e2c-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44e2c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

