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
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584843"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="7a302-103">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a302-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7a302-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a302-105">メッセージング システム内で定義されているように、サービス プロバイダーの id のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a302-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a302-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a302-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a302-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7a302-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7a302-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a302-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a302-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="7a302-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="7a302-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a302-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a302-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7a302-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7a302-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7a302-112">Area:</span></span>  <br/> |<span data-ttu-id="7a302-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="7a302-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a302-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7a302-114">Remarks</span></span>

<span data-ttu-id="7a302-115">状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="7a302-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="7a302-116">状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。</span><span class="sxs-lookup"><span data-stu-id="7a302-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="7a302-117">プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="7a302-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="7a302-118">このプロパティは通常、適切なアドレス帳のエントリ id を設定します。</span><span class="sxs-lookup"><span data-stu-id="7a302-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="7a302-119">Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a302-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="7a302-120">同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a302-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7a302-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a302-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7a302-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a302-122">Header files</span></span>

<span data-ttu-id="7a302-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a302-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a302-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a302-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a302-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a302-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7a302-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a302-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a302-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a302-127">See also</span></span>



[<span data-ttu-id="7a302-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="7a302-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="7a302-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a302-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a302-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a302-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a302-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a302-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a302-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7a302-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

