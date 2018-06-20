---
title: プロファイルとメッセージ サービスの管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799647"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="22972-103">プロファイルとメッセージ サービスの管理</span><span class="sxs-lookup"><span data-stu-id="22972-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="22972-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22972-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22972-105">プロファイルとメッセージのサービスの管理は、新しいプロファイルを作成する、古いプロファイルを削除して、メッセージ サービス、およびそれらに含まれているサービス ・ プロバイダーを変更することで既存のプロファイルの内容を変更することを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="22972-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="22972-106">すべてのクライアントは、標準的な機能としてのプロファイルとメッセージ サービスの管理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="22972-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="22972-107">一部のクライアントがある以外のユーザーは、ログオン時にいずれかの選択を許可するよりも、プロファイルを使用して操作を行います。</span><span class="sxs-lookup"><span data-stu-id="22972-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="22972-108">プロファイル、またはメッセージ サービスの管理をサポートする場合可能性は、次の MAPI によって実装されるインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="22972-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="22972-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) [IMAPISession::AdminServices](imapisession-adminservices.md)または[IProfAdmin::AdminServices](iprofadmin-adminservices.md)のいずれかを介してアクセスできるように、プロファイル内のメッセージ サービスを管理します。</span><span class="sxs-lookup"><span data-stu-id="22972-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="22972-110">メッセージング クライアントは、通常の構成のクライアント、またはクライアントの操作を行いますしない送信またはメッセージが表示される、 **IProfAdmin**を呼び出しているときに**IMAPISession**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="22972-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="22972-111">、可能な限りは、メッセージ サービスを開始するのには行われませんので、 **IProfAdmin**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="22972-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="22972-112">詳細については、 **IMsgServiceAdmin**インターフェイスを使用して、次のトピックを参照してください:[メッセージ サービスを構成する](configuring-a-message-service.md)、[メッセージ サービスのコピー](copying-a-message-service.md)、および[メッセージ サービスを削除](deleting-a-message-service.md)します。</span><span class="sxs-lookup"><span data-stu-id="22972-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="22972-113">[IProfAdmin: IUnknown](iprofadminiunknown.md)プロファイル、 [MAPIAdminProfiles](mapiadminprofiles.md)関数を使用してアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="22972-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="22972-114">詳細については、 **IProfAdmin**インターフェイスを使用して、次のトピックを参照してください:[カスタム コードを使用してプロファイルを作成する](creating-a-profile-by-using-custom-code.md)[プロファイルをコピーする](copying-a-profile.md)[プロファイルの削除](deleting-a-profile.md)、[プロファイル名の検索](finding-a-profile-name.md)、および[の設定、既定のプロファイル](setting-a-default-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="22972-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="22972-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) 、 [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを使用してアクセスのプロファイル セクションでプロパティを維持するためにします。</span><span class="sxs-lookup"><span data-stu-id="22972-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="22972-116">プロファイル セクションの詳細については、 [MAPI プロファイル](mapi-profiles.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22972-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="22972-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)経由でアクセスできる、メッセージ サービスのサービス プロバイダーを管理します。</span><span class="sxs-lookup"><span data-stu-id="22972-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="22972-118">詳細については、 **IProviderAdmin**インターフェイスを使用して、[追加、またはメッセージ サービスのプロバイダーを削除する](adding-or-deleting-providers-in-a-message-service.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22972-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="22972-119">プロファイルとメッセージ サービスの管理のサポートに注意が必要であります。</span><span class="sxs-lookup"><span data-stu-id="22972-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="22972-120">悪影響が使用されているプロファイルの変更から保護する保護機能はありません。</span><span class="sxs-lookup"><span data-stu-id="22972-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="22972-121">MAPI は、使用中のプロファイルを削除してからを防ぐことができますが、内のすべてのメッセージ サービスを削除するを防ぐことはできません。</span><span class="sxs-lookup"><span data-stu-id="22972-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="22972-122">プロファイル内のすべてのメッセージ サービスを削除すると、すべてのこれらのサービスのサービス プロバイダーが原因となり、発生する予期しない結果が停止します。</span><span class="sxs-lookup"><span data-stu-id="22972-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="22972-123">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="22972-123">In this section</span></span>

[<span data-ttu-id="22972-124">プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="22972-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="22972-125">プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="22972-126">プロファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="22972-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="22972-127">プロファイルをコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="22972-128">プロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="22972-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="22972-129">プロファイルを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="22972-130">既定のプロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="22972-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="22972-131">既定のプロファイルを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="22972-132">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="22972-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="22972-133">プロファイルの名前を検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="22972-134">メッセージ サービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="22972-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="22972-135">メッセージ サービスを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="22972-136">メッセージ サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="22972-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="22972-137">メッセージ サービスを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="22972-138">メッセージ サービスのコピー</span><span class="sxs-lookup"><span data-stu-id="22972-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="22972-139">メッセージ サービスをプロファイルにコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="22972-140">メッセージ サービスを削除します。</span><span class="sxs-lookup"><span data-stu-id="22972-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="22972-141">メッセージ サービスを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="22972-142">追加するか、メッセージ サービスのプロバイダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="22972-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="22972-143">メッセージ サービス内のプロバイダーを追加、削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="22972-143">Describes how to add or delete providers in a message service.</span></span>
    

