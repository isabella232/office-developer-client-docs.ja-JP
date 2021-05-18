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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423336"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="f0ea0-103">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0ea0-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f0ea0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0ea0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0ea0-105">メッセージング システム内で定義されているサービス プロバイダーの ID のエントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0ea0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f0ea0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0ea0-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f0ea0-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f0ea0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f0ea0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f0ea0-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="f0ea0-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="f0ea0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f0ea0-110">Data type:</span></span>  <br/> |<span data-ttu-id="f0ea0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f0ea0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f0ea0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f0ea0-112">Area:</span></span>  <br/> |<span data-ttu-id="f0ea0-113">MAPI の状態</span><span class="sxs-lookup"><span data-stu-id="f0ea0-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ea0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f0ea0-114">Remarks</span></span>

<span data-ttu-id="f0ea0-115">このプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、状態テーブルの列としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="f0ea0-116">これは、状態テーブル行を公開するサービス プロバイダーの ID の一部です。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="f0ea0-117">プロバイダーの ID は通常、サーバー上のアカウントを参照しますが、プロバイダーがメッセージング システム内で定義する任意の表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="f0ea0-118">この proprerty は、通常、適切なアドレス帳エントリ識別子に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="f0ea0-119">ID プロパティを提供するサービス プロバイダーは、すべての ID プロパティを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="f0ea0-120">同じメッセージ サービスに属するプロバイダーは、ID プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f0ea0-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f0ea0-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f0ea0-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f0ea0-122">Header files</span></span>

<span data-ttu-id="f0ea0-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0ea0-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0ea0-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f0ea0-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f0ea0-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f0ea0-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f0ea0-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0ea0-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0ea0-127">See also</span></span>



[<span data-ttu-id="f0ea0-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="f0ea0-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="f0ea0-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f0ea0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0ea0-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f0ea0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0ea0-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f0ea0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0ea0-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f0ea0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

