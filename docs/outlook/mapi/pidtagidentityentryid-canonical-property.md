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
ms.openlocfilehash: e724cc727292158fab26495e5d627b42dfe00daa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802827"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="e99e3-103">PidTagIdentityEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e99e3-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e99e3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e99e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e99e3-105">メッセージング システム内で定義されているように、サービス プロバイダーの id のエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e99e3-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e99e3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e99e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e99e3-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e99e3-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e99e3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e99e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e99e3-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="e99e3-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="e99e3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e99e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e99e3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e99e3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e99e3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e99e3-112">Area:</span></span>  <br/> |<span data-ttu-id="e99e3-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="e99e3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e99e3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e99e3-114">Remarks</span></span>

<span data-ttu-id="e99e3-115">状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。</span><span class="sxs-lookup"><span data-stu-id="e99e3-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="e99e3-116">状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。</span><span class="sxs-lookup"><span data-stu-id="e99e3-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="e99e3-117">プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e99e3-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="e99e3-118">このプロパティは通常、適切なアドレス帳のエントリ id を設定します。</span><span class="sxs-lookup"><span data-stu-id="e99e3-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="e99e3-119">Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e99e3-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="e99e3-120">同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e99e3-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e99e3-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e99e3-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e99e3-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e99e3-122">Header files</span></span>

<span data-ttu-id="e99e3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e99e3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e99e3-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e99e3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e99e3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e99e3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e99e3-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e99e3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e99e3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e99e3-127">See also</span></span>



[<span data-ttu-id="e99e3-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e99e3-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="e99e3-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e99e3-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e99e3-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e99e3-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e99e3-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e99e3-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e99e3-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e99e3-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

