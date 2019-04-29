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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430365"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="58caf-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="58caf-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="58caf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58caf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58caf-105">メッセージサービスがプロファイルのプライマリ id のサプライヤーであることを指定します。</span><span class="sxs-lookup"><span data-stu-id="58caf-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="58caf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58caf-106">Parameters</span></span>

 <span data-ttu-id="58caf-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="58caf-107">_lpUID_</span></span>
  
> <span data-ttu-id="58caf-108">順番プライマリ id を指定するメッセージサービスの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。または NULL。これは、 **setprimaryidentity**が現在の id をクリアする必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="58caf-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="58caf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58caf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="58caf-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="58caf-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58caf-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="58caf-111">Return value</span></span>

<span data-ttu-id="58caf-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="58caf-112">S_OK</span></span> 
  
> <span data-ttu-id="58caf-113">メッセージサービスに、プライマリ id のサプライヤーが正常に割り当てられました。</span><span class="sxs-lookup"><span data-stu-id="58caf-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="58caf-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="58caf-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="58caf-115">**setprimaryidentity**は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに SERVICE_NO_PRIMARY_IDENTITY フラグが設定されたメッセージサービスを指定しようとしました。</span><span class="sxs-lookup"><span data-stu-id="58caf-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58caf-116">注釈</span><span class="sxs-lookup"><span data-stu-id="58caf-116">Remarks</span></span>

<span data-ttu-id="58caf-117">**IMsgServiceAdmin:: setprimaryidentity**メソッドは、プロファイルのプライマリ id のサプライヤーとしてメッセージサービスを確立します。</span><span class="sxs-lookup"><span data-stu-id="58caf-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="58caf-118">プライマリ id は、通常、メッセージサービスにログオンしているユーザーです。</span><span class="sxs-lookup"><span data-stu-id="58caf-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="58caf-119">次の3つのプロパティで表されます。</span><span class="sxs-lookup"><span data-stu-id="58caf-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="58caf-120">**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="58caf-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="58caf-121">**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="58caf-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="58caf-122">**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="58caf-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="58caf-123">指定したメッセージサービスのすべてのサービスプロバイダーは、これら3つのプロパティを、プライマリ id を提供するメッセージングユーザーの表示名、エントリ識別子、および検索キーに設定します。</span><span class="sxs-lookup"><span data-stu-id="58caf-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="58caf-124">クライアントは、 [imapisession:: queryidentity](imapisession-queryidentity.md)メソッドを呼び出すことによって、プライマリ id のエントリ id を取得できます。</span><span class="sxs-lookup"><span data-stu-id="58caf-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="58caf-125">**PR_RESOURCE_FLAGS**プロパティは、プライマリ id を提供するメッセージサービスのメンバーであるすべてのプロバイダーの STATUS_PRIMARY_IDENTITY、およびメッセージサービスの SERVICE_PRIMARY_IDENTITY に設定されます。</span><span class="sxs-lookup"><span data-stu-id="58caf-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="58caf-126">サービスプロバイダーがメッセージサービスのプライマリ id を提供できない場合、 **PR_RESOURCE_FLAGS**は STATUS_NO_PRIMARY_IDENTITY に設定されます。</span><span class="sxs-lookup"><span data-stu-id="58caf-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="58caf-127">**setprimaryidentity**は、プライマリ id を指定していない各メッセージサービスの**PR_RESOURCE_FLAGS**プロパティを SERVICE_NO_PRIMARY_IDENTITY に設定します。</span><span class="sxs-lookup"><span data-stu-id="58caf-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="58caf-128">MAPI が情報を持っている各メッセージサービスプロバイダーは、クライアントがサービスにログオンしたときに、各ユーザーの id を確立できます。</span><span class="sxs-lookup"><span data-stu-id="58caf-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="58caf-129">ただし、mapi は各 mapi セッションに対して複数のサービスプロバイダーへの接続をサポートしているため、mapi セッション全体で特定のユーザーの id を定義することはありません。ユーザーの id は、関係するサービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="58caf-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="58caf-130">クライアントは**setprimaryidentity**を呼び出して、そのユーザーのプライマリ id として、メッセージサービスによってユーザーに対して確立された複数の id の1つを指定できます。</span><span class="sxs-lookup"><span data-stu-id="58caf-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58caf-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="58caf-131">See also</span></span>



[<span data-ttu-id="58caf-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="58caf-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="58caf-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="58caf-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="58caf-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58caf-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

