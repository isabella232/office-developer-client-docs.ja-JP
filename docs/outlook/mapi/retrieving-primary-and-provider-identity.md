---
title: プライマリとプロバイダー id の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430813"
---
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="92612-103">プライマリとプロバイダー id の取得</span><span class="sxs-lookup"><span data-stu-id="92612-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="92612-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92612-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92612-105">サービスプロバイダー (通常はアドレス帳プロバイダー) は、さまざまな状況でセッションを表すために使用できる id を提供するオプションを備えています。</span><span class="sxs-lookup"><span data-stu-id="92612-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="92612-106">次の3つのプロパティは、プロバイダーの id を記述します。</span><span class="sxs-lookup"><span data-stu-id="92612-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="92612-107">**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92612-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92612-108">**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92612-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92612-109">**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="92612-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="92612-110">これらのプロパティは、主にメッセージングユーザーである、対応する identity オブジェクトのエントリ id、表示名、および検索キーに設定されます。</span><span class="sxs-lookup"><span data-stu-id="92612-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="92612-111">id を指定するプロバイダーも、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに STATUS_PRIMARY_IDENTITY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="92612-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="92612-112">必要に応じて、特定のプロバイダーの id またはセッションのプライマリ id を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="92612-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="92612-113">プロバイダーの id を使用して、表示を目的にしたり、 **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)) などのプロパティを取得したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="92612-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="92612-114">**PR_RESOURCE_PATH**(設定されている場合) は、プロバイダーによって使用または作成されたファイルへのパスを含みます。</span><span class="sxs-lookup"><span data-stu-id="92612-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="92612-115">セッションのユーザーに関連するファイルを検索する場合は、プライマリ id を提供するプロバイダーの**PR_RESOURCE_PATH**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="92612-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="92612-116">**特定のプロバイダーの id を取得するには**</span><span class="sxs-lookup"><span data-stu-id="92612-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="92612-117">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="92612-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="92612-118">[spropertyrestriction](spropertyrestriction.md)構造を使用して制限を構築し、 **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) 列と指定されたプロバイダーの名前を照合します。</span><span class="sxs-lookup"><span data-stu-id="92612-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="92612-119">$ [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、プロバイダーの行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="92612-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="92612-120">プロバイダーの id は、 **PR_IDENTITY_ENTRYID**列が存在する場合は、その列に格納されます。</span><span class="sxs-lookup"><span data-stu-id="92612-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="92612-121">**セッションのプライマリ id を取得するには**</span><span class="sxs-lookup"><span data-stu-id="92612-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="92612-122">呼び出し[imapisession:: queryidentity](imapisession-queryidentity.md)。</span><span class="sxs-lookup"><span data-stu-id="92612-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="92612-123">**queryidentity**は、[状態] テーブルの行の1つの**PR_RESOURCE_FLAGS**列に STATUS_PRIMARY_IDENTITY 値が存在する場合に、セッション id をベースとします。</span><span class="sxs-lookup"><span data-stu-id="92612-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="92612-124">この値が設定されている状態行がない場合、 **queryidentity**は、3つの PR_IDENTITY プロパティを設定する最初のサービスプロバイダーに id を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="92612-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="92612-125">id を提供するサービスプロバイダーがない場合、 **queryidentity**は MAPI_W_NO_SERVICE を返します。</span><span class="sxs-lookup"><span data-stu-id="92612-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="92612-126">このような場合、プライマリ id として使用できる汎用ユーザーを表す文字列を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92612-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="92612-127">**セッションのプライマリ id を明示的に設定するには**</span><span class="sxs-lookup"><span data-stu-id="92612-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="92612-128">Call [IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)。</span><span class="sxs-lookup"><span data-stu-id="92612-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="92612-129">対象のサービスプロバイダーの**MAPIUID**を渡します。</span><span class="sxs-lookup"><span data-stu-id="92612-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

