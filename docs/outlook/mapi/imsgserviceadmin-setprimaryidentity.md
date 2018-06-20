---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800992"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="fe987-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="fe987-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="fe987-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe987-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe987-105">メッセージ サービス プロファイルのプライマリ id のサプライヤーになることを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe987-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="fe987-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe987-106">Parameters</span></span>

 <span data-ttu-id="fe987-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="fe987-107">_lpUID_</span></span>
  
> <span data-ttu-id="fe987-108">[in]主の id を指定するのにはメッセージ サービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体または**SetPrimaryIdentity**が現在の id をクリアする必要があることを示す、NULL へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fe987-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="fe987-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe987-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fe987-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="fe987-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fe987-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fe987-111">Return value</span></span>

<span data-ttu-id="fe987-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe987-112">S_OK</span></span> 
  
> <span data-ttu-id="fe987-113">メッセージ サービスは、プライマリ id の提供元を正常に割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="fe987-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="fe987-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fe987-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="fe987-115">**SetPrimaryIdentity**では、SERVICE_NO_PRIMARY_IDENTITY フラグの**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティを設定するメッセージ サービスを指定しようとしています。</span><span class="sxs-lookup"><span data-stu-id="fe987-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe987-116">備考</span><span class="sxs-lookup"><span data-stu-id="fe987-116">Remarks</span></span>

<span data-ttu-id="fe987-117">**IMsgServiceAdmin::SetPrimaryIdentity**メソッドは、プロファイルのプライマリ id の提供元として、メッセージ サービスを確立します。</span><span class="sxs-lookup"><span data-stu-id="fe987-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="fe987-118">プライマリ id は、通常はメッセージ サービスにログオンしているユーザーです。</span><span class="sxs-lookup"><span data-stu-id="fe987-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="fe987-119">3 つのプロパティによって表されます。</span><span class="sxs-lookup"><span data-stu-id="fe987-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="fe987-120">**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fe987-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="fe987-121">**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fe987-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="fe987-122">**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fe987-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="fe987-123">指定されたメッセージ サービスですべてのサービス プロバイダーは、表示名、エントリ id、およびプライマリ id を提供するメッセージングのユーザーのキーを検索するにはこれら 3 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe987-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="fe987-124">クライアントは、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)メソッドを呼び出すことによって、プライマリ id のエントリ id を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fe987-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="fe987-125">主の id を提供するメッセージ サービスのメンバーであるすべてのプロバイダーの STATUS_PRIMARY_IDENTITY とメッセージ サービスの SERVICE_PRIMARY_IDENTITY、 **PR_RESOURCE_FLAGS**プロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="fe987-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="fe987-126">サービス プロバイダーは、メッセージ サービスのプライマリ id を提供できません、 **PR_RESOURCE_FLAGS**を STATUS_NO_PRIMARY_IDENTITY に設定します。</span><span class="sxs-lookup"><span data-stu-id="fe987-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="fe987-127">**SetPrimaryIdentity**は、SERVICE_NO_PRIMARY_IDENTITY をプライマリ id を指定していないが、各メッセージ サービスの**PR_RESOURCE_FLAGS**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe987-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="fe987-128">クライアントがサービスにログオンすると、MAPI には詳細情報が含まれているメッセージの各サービス プロバイダーは、ユーザーごとの id を確立できます。</span><span class="sxs-lookup"><span data-stu-id="fe987-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="fe987-129">ただし、MAPI は MAPI セッションごとに複数のサービス プロバイダーへの接続をサポートするためは全体として、MAPI セッションの特定のユーザーの id の定義をしっかりユーザーの id は、どのサービスが含まれているによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fe987-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="fe987-130">クライアントは、そのユーザーのプライマリ id として、ユーザーのメッセージ サービスによって確立された多くのユーザーのいずれかを指定するのには**SetPrimaryIdentity**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fe987-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe987-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe987-131">See also</span></span>



[<span data-ttu-id="fe987-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="fe987-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="fe987-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="fe987-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="fe987-134">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe987-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

