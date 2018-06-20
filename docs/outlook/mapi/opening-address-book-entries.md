---
title: アドレス帳のエントリを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801695"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="aefdf-103">アドレス帳のエントリを開く</span><span class="sxs-lookup"><span data-stu-id="aefdf-103">Opening address book entries</span></span>

<span data-ttu-id="aefdf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aefdf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aefdf-105">クライアントまたはプロバイダーが要求されると、オブジェクトの 1 つを開くことを MAPI は、プロバイダーの[IABLogon::OpenEntry](iablogon-openentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="aefdf-106">MAPI では、ターゲット オブジェクトを表すエントリの識別子が、 [MAPIUID](mapiuid.md)の部分のエントリ id を調べ、**への呼び出しでは、プロバイダーが登録されている**MAPIUID**に一致することによって、プロバイダーに属することを決定します。IMAPISupport::SetProviderUID**。</span><span class="sxs-lookup"><span data-stu-id="aefdf-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="aefdf-107">MAPI は、 **OpenEntry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="aefdf-108">プロバイダーが対応するオブジェクトを取得することで応答する必要があります: コンテナー、配布リスト、またはメッセージングのユーザーです。</span><span class="sxs-lookup"><span data-stu-id="aefdf-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="aefdf-109">NULL エントリの識別子では、アドレス帳プロバイダーのルート コンテナーを開く要求を示します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="aefdf-110">クライアントは、その階層のテーブルとその受信者にアクセスするルート コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="aefdf-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="aefdf-111">のみ 1 回限りの受信者を作成するためのテンプレートを提供するアドレス帳プロバイダーは、ルート コンテナーの**OpenEntry**呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="aefdf-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="aefdf-112">IABLogon::OpenEntry を実装するには</span><span class="sxs-lookup"><span data-stu-id="aefdf-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="aefdf-113">エントリの識別子が、プロバイダーがサポートする有効な識別子であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="aefdf-114">エントリの有効な識別子でない場合は、MAPI_E_INVALID_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="aefdf-115">_UlFlags_パラメーターに渡されるフラグを確認します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="aefdf-116">MAPI_MODIFY MAPI が渡された場合は、プロバイダーでは、そのオブジェクトを変更することはできません、失敗し、MAPI_E_ACCESS_DENIED のエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="aefdf-117">_LpInterface_パラメーターで要求されたインターフェイスは、プロバイダーは、開くを要求されているオブジェクトの種類に対して有効なことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="aefdf-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="aefdf-118">無効なパラメーターが渡された場合は失敗し、MAPI_E_INTERFACE_NOT_SUPPORTED のエラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="aefdf-119">_CbEntryID_パラメーターが 0 の場合は、これは、プロバイダーのルート コンテナーを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="aefdf-120">ルート コンテナーを作成し、**これにより**インターフェイスの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="aefdf-121">プロバイダーは、いくつかのログオン オブジェクトを実装する場合は、それぞれ独自に**MAPIUID**、 **MAPIUID**は、適切なログオン オブジェクトのエントリ id に含まれているマップが登録されています。</span><span class="sxs-lookup"><span data-stu-id="aefdf-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="aefdf-122">エントリの識別子を表すオブジェクトの種類を決定する: メッセージ ユーザー、配布リスト、または_lpulObjectType_の適切な値を設定することができるように、プロバイダー、または 1 回限りのメッセージングのユーザーまたは配布リストに属するコンテナーパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="aefdf-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="aefdf-123">適切な型のオブジェクトを作成し、次の基本的なプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="aefdf-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aefdf-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="aefdf-125">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aefdf-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="aefdf-126">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aefdf-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="aefdf-127">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aefdf-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="aefdf-128">エントリ id の情報から、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="aefdf-129">オブジェクトのインターフェイスの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="aefdf-129">Return a pointer to the interface implementation for the object.</span></span> 
    

