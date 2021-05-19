---
title: プロファイルとメッセージ サービスの管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410561"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="0a9a7-103">プロファイルとメッセージ サービスの管理</span><span class="sxs-lookup"><span data-stu-id="0a9a7-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="0a9a7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a9a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a9a7-105">プロファイルとメッセージ サービスの管理には、新しいプロファイルの作成、古いプロファイルの削除、および既存のプロファイルに含まれるメッセージ サービスとサービス プロバイダーの変更による既存のプロファイルの内容の変更が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="0a9a7-106">一部のクライアントがプロファイルとメッセージ サービスの管理を標準機能としてサポートしている場合ではありません。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="0a9a7-107">一部のクライアントは、ユーザーがログオン時にプロファイルを選択できる以上の関係を持っていません。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="0a9a7-108">プロファイルまたはメッセージ サービスの管理をサポートしている場合は、MAPI によって実装されている次のインターフェイスを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="0a9a7-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) は [、IMAPISession::AdminServices](imapisession-adminservices.md) または [IProfAdmin::AdminServices](iprofadmin-adminservices.md)のいずれかを介してアクセスできるプロファイルでメッセージ サービスを管理します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="0a9a7-110">メッセージング クライアントは、通常 **、IMAPISession** を呼び出しますが、構成クライアント、またはメッセージを送受信しないクライアントは **、IProfAdmin を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="0a9a7-111">可能な限り、メッセージ サービスが開始されないので **、IProfAdmin** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="0a9a7-112">**IMsgServiceAdmin** インターフェイスの使用の詳細については、「メッセージ サービスの構成 [](configuring-a-message-service.md)、メッセージ サービスのコピー [](copying-a-message-service.md)、およびメッセージ サービスの削除」を [参照してください](deleting-a-message-service.md)。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="0a9a7-113">[IProfAdmin : MAPIAdminProfiles](iprofadminiunknown.md)関数からアクセスできるプロファイルを管理する[IUnknown。](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="0a9a7-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="0a9a7-114">**IProfAdmin** インターフェイスの使用の詳細については、「カスタム コードを使用 [](creating-a-profile-by-using-custom-code.md)したプロファイルの作成、プロファイルのコピー、プロファイルの削除、[](deleting-a-profile.md)プロファイル名の検索、[](finding-a-profile-name.md)および既定のプロファイルの設定 [](setting-a-default-profile.md)」を参照してください。 [](copying-a-profile.md)</span><span class="sxs-lookup"><span data-stu-id="0a9a7-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="0a9a7-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) を使用して [、IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) メソッドまたは [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) メソッドからアクセスできる、プロファイル セクションのプロパティを維持します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="0a9a7-116">プロファイル セクションの詳細については [、「MAPI プロファイル」を参照してください](mapi-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="0a9a7-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) は [、IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を介してアクセス可能なメッセージ サービスでサービス プロバイダーを管理します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="0a9a7-118">**IProviderAdmin** インターフェイスの使用の詳細については、「メッセージ サービスでのプロバイダーの追加または削除」[を参照してください](adding-or-deleting-providers-in-a-message-service.md)。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="0a9a7-119">プロファイルとメッセージ サービスの管理のサポートに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="0a9a7-120">使用されているプロファイルを悪影響を及ぼす変更から保護するための保護手段はありません。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="0a9a7-121">MAPI では、使用されているプロファイルを削除することはできませんが、その中のすべてのメッセージ サービスを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="0a9a7-122">プロファイル内のすべてのメッセージ サービスを削除すると、これらのサービスのすべてのサービス プロバイダーが停止し、予期しない結果が発生します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="0a9a7-123">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="0a9a7-123">In this section</span></span>

[<span data-ttu-id="0a9a7-124">プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="0a9a7-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="0a9a7-125">プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="0a9a7-126">プロファイルのコピー</span><span class="sxs-lookup"><span data-stu-id="0a9a7-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="0a9a7-127">プロファイルをコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="0a9a7-128">プロファイルの削除</span><span class="sxs-lookup"><span data-stu-id="0a9a7-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="0a9a7-129">プロファイルを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="0a9a7-130">既定のプロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="0a9a7-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="0a9a7-131">既定のプロファイルを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="0a9a7-132">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="0a9a7-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="0a9a7-133">プロファイルの名前を検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="0a9a7-134">メッセージ サービスの追加</span><span class="sxs-lookup"><span data-stu-id="0a9a7-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="0a9a7-135">メッセージ サービスを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="0a9a7-136">メッセージ サービスの構成</span><span class="sxs-lookup"><span data-stu-id="0a9a7-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="0a9a7-137">メッセージ サービスを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="0a9a7-138">メッセージ サービスのコピー</span><span class="sxs-lookup"><span data-stu-id="0a9a7-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="0a9a7-139">メッセージ サービスをプロファイルにコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="0a9a7-140">メッセージ サービスの削除</span><span class="sxs-lookup"><span data-stu-id="0a9a7-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="0a9a7-141">メッセージ サービスを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="0a9a7-142">メッセージ サービスでのプロバイダーの追加または削除</span><span class="sxs-lookup"><span data-stu-id="0a9a7-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="0a9a7-143">メッセージ サービスでプロバイダーを追加または削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0a9a7-143">Describes how to add or delete providers in a message service.</span></span>
    

