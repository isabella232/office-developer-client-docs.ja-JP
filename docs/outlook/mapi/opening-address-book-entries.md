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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422160"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="401aa-103">アドレス帳エントリを開く</span><span class="sxs-lookup"><span data-stu-id="401aa-103">Opening address book entries</span></span>

<span data-ttu-id="401aa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="401aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="401aa-105">クライアントまたはプロバイダーがオブジェクトの 1 つを開くことを要求した場合、MAPI はプロバイダーの [IABLogon::OpenEntry メソッドを呼び出](iablogon-openentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="401aa-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="401aa-106">MAPI は、エントリ識別子の [MAPIUID](mapiuid.md)部分を調べて **、IMAPISupport::SetProviderUID** への呼び出しでプロバイダーが登録した **MAPIUID** に一致することで、ターゲット オブジェクトを表すエントリ識別子がプロバイダーに属すると判断します。</span><span class="sxs-lookup"><span data-stu-id="401aa-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="401aa-107">MAPI は **、OpenEntry メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="401aa-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="401aa-108">プロバイダーは、対応するオブジェクト (コンテナー、配布リスト、またはメッセージング ユーザー) を取得して応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="401aa-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="401aa-109">NULL エントリ識別子は、アドレス帳プロバイダーのルート コンテナーを開く要求を示します。</span><span class="sxs-lookup"><span data-stu-id="401aa-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="401aa-110">クライアントはルート コンテナーを開いて、階層テーブルとその受信者にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="401aa-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="401aa-111">一時受信者を作成するためのテンプレートのみを提供するアドレス帳プロバイダーは、ルート コンテナーの **OpenEntry** 呼び出しをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="401aa-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="401aa-112">IABLogon::OpenEntry を実装するには</span><span class="sxs-lookup"><span data-stu-id="401aa-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="401aa-113">エントリ識別子がプロバイダーがサポートする有効な識別子を確認します。</span><span class="sxs-lookup"><span data-stu-id="401aa-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="401aa-114">有効なエントリ識別子でない場合は、次の値をMAPI_E_INVALID_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="401aa-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="401aa-115">_ulFlags_ パラメーターで渡されるフラグを確認します。</span><span class="sxs-lookup"><span data-stu-id="401aa-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="401aa-116">MAPI がアプリケーションで渡MAPI_MODIFYプロバイダーがオブジェクトの変更を許可しない場合は、エラー値をMAPI_E_ACCESS_DENIEDします。</span><span class="sxs-lookup"><span data-stu-id="401aa-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="401aa-117">_lpInterface_ パラメーターで要求されたインターフェイスが、プロバイダーに開く要求されたオブジェクトの種類に対して有効か確認します。</span><span class="sxs-lookup"><span data-stu-id="401aa-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="401aa-118">無効なパラメーターが渡された場合は、エラー値をMAPI_E_INTERFACE_NOT_SUPPORTEDします。</span><span class="sxs-lookup"><span data-stu-id="401aa-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="401aa-119">_cbEntryID_ パラメーターが 0 の場合、これはプロバイダーのルート コンテナーを開く要求です。</span><span class="sxs-lookup"><span data-stu-id="401aa-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="401aa-120">ルート コンテナーを作成し **、IABContainer インターフェイス実装へのポインターを** 返します。</span><span class="sxs-lookup"><span data-stu-id="401aa-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="401aa-121">プロバイダーが複数のログオン オブジェクトを実装している場合は、それぞれが独自に登録済みの **MAPIUID** を持ち、エントリ識別子に含まれる **MAPIUID** を適切なログオン オブジェクトにマップします。</span><span class="sxs-lookup"><span data-stu-id="401aa-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="401aa-122">_lpulObjectType_ パラメーターに適切な値を設定できるよう、プロバイダーに属するメッセージング ユーザー、配布リスト、またはコンテナー、または一時メッセージング ユーザーまたは配布リストなど、エントリ識別子が表すオブジェクトの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="401aa-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="401aa-123">適切な種類のオブジェクトを作成し、次の基本プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="401aa-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="401aa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="401aa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="401aa-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="401aa-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="401aa-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="401aa-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="401aa-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="401aa-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="401aa-128">エントリ **PR_EMAIL_ADDRESS** 情報から、PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。</span><span class="sxs-lookup"><span data-stu-id="401aa-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="401aa-129">オブジェクトのインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="401aa-129">Return a pointer to the interface implementation for the object.</span></span> 
    

