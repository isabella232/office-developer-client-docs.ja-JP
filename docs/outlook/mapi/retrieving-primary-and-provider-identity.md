---
title: プライマリ ID とプロバイダー ID の取得
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
# <a name="retrieving-primary-and-provider-identity"></a><span data-ttu-id="f6f3c-103">プライマリ ID とプロバイダー ID の取得</span><span class="sxs-lookup"><span data-stu-id="f6f3c-103">Retrieving Primary and Provider Identity</span></span>

  
  
<span data-ttu-id="f6f3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6f3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6f3c-105">サービス プロバイダー (通常はアドレス帳プロバイダー) には、さまざまな状況でセッションを表す ID を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-105">Service providers, typically address book providers, have the option of supplying an identity that can be used to represent the session in a variety of situations.</span></span> <span data-ttu-id="f6f3c-106">3 つのプロパティは、プロバイダーの ID を表します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-106">Three properties describe a provider's identity:</span></span>
  
- <span data-ttu-id="f6f3c-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6f3c-107">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f6f3c-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6f3c-108">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f6f3c-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6f3c-109">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="f6f3c-110">これらのプロパティは、対応する ID オブジェクトのエントリ識別子、表示名、および検索キー (通常はメッセージング ユーザー) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-110">These properties are set to the entry identifier, display name, and search key of the corresponding identity object, which is typically a messaging user.</span></span> <span data-ttu-id="f6f3c-111">ID を指定するプロバイダーは、STATUS_PRIMARY_IDENTITY **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティPR_RESOURCE_FLAGSフラグも設定します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-111">Providers that supply an identity also set the STATUS_PRIMARY_IDENTITY flag in their **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f6f3c-112">ニーズに応じて、特定のプロバイダーの ID またはセッションのプライマリ ID を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-112">Depending on your needs, you might use a particular provider's identity or the primary identity for the session.</span></span> <span data-ttu-id="f6f3c-113">プロバイダーの ID は、表示またはプロパティの取得にも使用できます (たとえば、PR_RESOURCE_PATH  [(PidTagResourcePath)。](pidtagresourcepath-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-113">You can use a provider's identity also for display purposes or to retrieve properties, such as **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)).</span></span> <span data-ttu-id="f6f3c-114">**PR_RESOURCE_PATH** 設定されている場合は、プロバイダーによって使用または作成されたファイルへのパスが含まれる。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-114">**PR_RESOURCE_PATH**, if set, contains the path to files used or created by the provider.</span></span> <span data-ttu-id="f6f3c-115">セッションの **PR_RESOURCE_PATH** に関連するファイルを検索する場合に、プライマリ ID を指定するプロバイダーの PR_RESOURCE_PATH プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-115">Retrieve the **PR_RESOURCE_PATH** property for the provider supplying the primary identity when you want to locate files that pertain to the user of the session.</span></span> 
  
 <span data-ttu-id="f6f3c-116">**特定のプロバイダーの ID を取得するには**</span><span class="sxs-lookup"><span data-stu-id="f6f3c-116">**To retrieve the identity of a specific provider**</span></span>
  
1. <span data-ttu-id="f6f3c-117">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-117">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="f6f3c-118">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して制限を作成し **、PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) 列と指定したプロバイダーの名前を一致します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-118">Build a restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match the **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) column with the name of the specified provider.</span></span> 
    
3. <span data-ttu-id="f6f3c-119">[IMAPITable::FindRow を呼び出して](imapitable-findrow.md)、プロバイダーの行を探します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-119">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the provider's row.</span></span> <span data-ttu-id="f6f3c-120">プロバイダーの ID は、存在する場合 **、PR_IDENTITY_ENTRYID列に** 格納されます。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-120">The provider's identity will be stored in the **PR_IDENTITY_ENTRYID** column, if it exists.</span></span> 
    
 <span data-ttu-id="f6f3c-121">**セッションのプライマリ ID を取得するには**</span><span class="sxs-lookup"><span data-stu-id="f6f3c-121">**To retrieve the primary identity for a session**</span></span>
  
- <span data-ttu-id="f6f3c-122">[IMAPISession::QueryIdentity を呼び出します](imapisession-queryidentity.md)。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-122">Call [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="f6f3c-123">**QueryIdentity は**、状態テーブルのいずれかの行の STATUS_PRIMARY_IDENTITY 列に PR_RESOURCE_FLAGS値が存在する場合にセッション ID を基にします。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-123">**QueryIdentity** bases session identity on the existence of the STATUS_PRIMARY_IDENTITY value in the **PR_RESOURCE_FLAGS** column for one of the rows in the status table.</span></span> <span data-ttu-id="f6f3c-124">どの状態行にもこの値が設定されている場合 **、QueryIdentity** は、3 つのプロパティを設定する最初のサービス プロバイダーに id をPR_IDENTITYします。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-124">If none of the status rows have this value set, **QueryIdentity** assigns identity to the first service provider that sets the three PR_IDENTITY properties.</span></span> <span data-ttu-id="f6f3c-125">ID を提供するサービス プロバイダーがない場合 **、QueryIdentity** は id をMAPI_W_NO_SERVICE。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-125">If no service provider supplies an identity, **QueryIdentity** returns MAPI_W_NO_SERVICE.</span></span> <span data-ttu-id="f6f3c-126">この場合は、プライマリ ID として機能できる汎用ユーザーを表す文字列を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-126">When this happens, you should create a character string to represent a generic user that can serve as the primary identity.</span></span> 
    
 <span data-ttu-id="f6f3c-127">**セッションのプライマリ ID を明示的に設定するには**</span><span class="sxs-lookup"><span data-stu-id="f6f3c-127">**To explicitly set the primary identity for a session**</span></span>
  
- <span data-ttu-id="f6f3c-128">[IMsgServiceAdmin::SetPrimaryIdentity を呼び出します](imsgserviceadmin-setprimaryidentity.md)。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-128">Call [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).</span></span> <span data-ttu-id="f6f3c-129">ターゲット サービス **プロバイダーの MAPIUID** を渡します。</span><span class="sxs-lookup"><span data-stu-id="f6f3c-129">Pass the **MAPIUID** for the target service provider.</span></span> 
    

