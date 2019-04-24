---
title: アドレス帳エントリを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326328"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="f2cfa-103">アドレス帳エントリを開く</span><span class="sxs-lookup"><span data-stu-id="f2cfa-103">Opening address book entries</span></span>

<span data-ttu-id="f2cfa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cfa-105">クライアントまたはプロバイダーが、いずれかのオブジェクトを開くことを要求した場合、MAPI はプロバイダーの[IABLogon:: openentry](iablogon-openentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="f2cfa-106">MAPI は、エントリ識別子の[MAPIUID](mapiuid.md)部分を調べ、それを呼び出し\*\*\*\* **でプロバイダーが登録した MAPIUID に一致させることによって、ターゲットオブジェクトを表すエントリ識別子がプロバイダーに属していると判断します。imapisupport:: setprovideruid**。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="f2cfa-107">その後、MAPI が**openentry**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="f2cfa-108">プロバイダーは、対応するオブジェクト (コンテナー、配布リスト、またはメッセージングユーザー) を取得することによって応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="f2cfa-109">NULL エントリ識別子は、アドレス帳プロバイダーのルートコンテナーを開く要求を示します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="f2cfa-110">クライアントは、ルートコンテナーを開いて、階層テーブルとその受信者にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="f2cfa-111">1回限りの受信者を作成するためのテンプレートのみを提供するアドレス帳プロバイダーは、ルートコンテナーの**openentry**呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="f2cfa-112">IABLogon:: openentry を実装するには</span><span class="sxs-lookup"><span data-stu-id="f2cfa-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="f2cfa-113">入力識別子がプロバイダーがサポートしている有効な識別子であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="f2cfa-114">有効なエントリ識別子でない場合は、MAPI_E_INVALID_ENTRYID を返します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f2cfa-115">_ulflags_パラメーターを使用して渡されたフラグを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f2cfa-116">MAPI が MAPI_MODIFY で渡され、プロバイダーがそのオブジェクトの変更を許可していない場合は、エラーが発生し、MAPI_E_ACCESS_DENIED エラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="f2cfa-117">_lpinterface_パラメーターで要求されたインターフェイスが、プロバイダーが開くように求められたオブジェクトの種類に対して有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="f2cfa-118">無効なパラメーターが渡された場合は、fail を返し、MAPI_E_INTERFACE_NOT_SUPPORTED エラーの値を返します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="f2cfa-119">_cbEntryID_パラメーターが0の場合、これはプロバイダーのルートコンテナーを開くための要求です。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="f2cfa-120">ルートコンテナーを作成し、その**IABContainer**インターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="f2cfa-121">プロバイダーが複数のログオンオブジェクトを実装しており、それぞれに**MAPIUID**登録されている場合は、エントリ識別子に含まれる**MAPIUID**と適切なログオンオブジェクトをマップします。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="f2cfa-122">エントリ識別子が表すオブジェクトの種類を決定します。これは、プロバイダーに属するメッセージングユーザー、配布リスト、またはコンテナーで、または、 _lpulObjectType_に対して適切な値を設定できるように、1回限りのメッセージングユーザーまたは配布リストに属しています。parameter.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="f2cfa-123">適切な型のオブジェクトを作成し、次の基本的なプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="f2cfa-124">**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2cfa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="f2cfa-125">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2cfa-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="f2cfa-126">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2cfa-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="f2cfa-127">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2cfa-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="f2cfa-128">エントリ識別子の情報から**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="f2cfa-129">オブジェクトのインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f2cfa-129">Return a pointer to the interface implementation for the object.</span></span> 
    

