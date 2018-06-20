---
title: プライマリ デバイスとプロバイダーの Id を取得しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2a87e32fe21aa6fb1d9296c568a74da994c146bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803766"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="ebf1e-103">プライマリ デバイスとプロバイダーの Id を取得しています。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="ebf1e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebf1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebf1e-105">通常のアドレス帳プロバイダー、サービス ・ プロバイダーには、さまざまな状況でセッションを表すために使用できる id を指定するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="ebf1e-106">3 つのプロパティでは、プロバイダーの識別情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="ebf1e-107">**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebf1e-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="ebf1e-108">**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebf1e-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="ebf1e-109">**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ebf1e-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="ebf1e-110">これらのプロパティは、エントリ id、表示名、および対応する id のオブジェクトは、メッセージングのユーザーは、通常の検索キーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="ebf1e-111">Id を提供するプロバイダーは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティに STATUS_PRIMARY_IDENTITY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ebf1e-112">必要に応じて、セッションの特定のプロバイダーの id またはプライマリを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="ebf1e-113">表示のためにまたは**PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) などのプロパティを取得するためには、プロバイダーの id を使用します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="ebf1e-114">**PR_RESOURCE_PATH**場合、は、使用、またはプロバイダーによって作成されたファイルへのパスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="ebf1e-115">セッションのユーザーに関連するファイルを検索する場合は、プライマリ id を提供するプロバイダーの**PR_RESOURCE_PATH**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="ebf1e-116">**特定のプロバイダーの id を取得するには**</span><span class="sxs-lookup"><span data-stu-id="ebf1e-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="ebf1e-117">ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="ebf1e-118">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して、指定されたプロバイダーの名前を**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) の列と一致する制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="ebf1e-119">プロバイダーの行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="ebf1e-120">プロバイダーの識別情報は、存在する場合、[ **PR_IDENTITY_ENTRYID** ] 列で、保存されます。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="ebf1e-121">**セッションのプライマリ id を取得するには**</span><span class="sxs-lookup"><span data-stu-id="ebf1e-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="ebf1e-122">[IMAPISession::QueryIdentity](imapisession-queryidentity.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="ebf1e-123">**QueryIdentity**に基づいて、セッションの id、STATUS_PRIMARY_IDENTITY、 **PR_RESOURCE_FLAGS**の列の値の状態テーブル内の行のいずれかが存在します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="ebf1e-124">ステータス行の [なし] この値が設定されて、 **QueryIdentity**は 3 つの PR_IDENTITY プロパティを設定する最初のサービス プロバイダーの id を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="ebf1e-125">サービス プロバイダーには、id が用意されていない、 **QueryIdentity**は MAPI_W_NO_SERVICE を返します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="ebf1e-126">このような場合、プライマリ id として使用できる汎用的なユーザーを表す文字列を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="ebf1e-127">**セッションのプライマリ id を明示的に設定するには**</span><span class="sxs-lookup"><span data-stu-id="ebf1e-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="ebf1e-128">[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="ebf1e-129">ターゲット ・ サービス ・ プロバイダーの**MAPIUID**を渡します。</span><span class="sxs-lookup"><span data-stu-id="ebf1e-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

