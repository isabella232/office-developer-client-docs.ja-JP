---
title: プロファイルとメッセージサービスを管理する
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
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="16dd0-103">プロファイルとメッセージサービスを管理する</span><span class="sxs-lookup"><span data-stu-id="16dd0-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="16dd0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16dd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16dd0-105">プロファイルとメッセージサービスの管理には、新しいプロファイルを作成したり、古いプロファイルを削除したり、既存のプロファイルの内容を変更したりすることが含まれます。その中に含まれるメッセージサービスとサービスプロバイダーを変更します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="16dd0-106">すべてのクライアントが、プロファイルとメッセージサービスの管理を標準的な機能としてサポートするわけではありません。</span><span class="sxs-lookup"><span data-stu-id="16dd0-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="16dd0-107">クライアントによっては、ユーザーがログオン時に1つを選択できるというよりもプロファイルを使用することができません。</span><span class="sxs-lookup"><span data-stu-id="16dd0-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="16dd0-108">プロファイルまたはメッセージサービスの管理をサポートしている場合は、MAPI で実装されている次のインターフェイスを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="16dd0-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="16dd0-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)を使用して、プロファイル内のメッセージサービスを管理します。 [imapisession:: adminservices](imapisession-adminservices.md)または[IProfAdmin:: adminservices](iprofadmin-adminservices.md)のどちらかを通じてアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="16dd0-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="16dd0-110">メッセージングクライアントは、通常、構成クライアント、またはメッセージの送受信が行われないクライアントの間に**imapisession**を呼び出します。 **IProfAdmin**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="16dd0-111">可能な限り、 **IProfAdmin**メソッドを呼び出すと、メッセージサービスは開始されません。</span><span class="sxs-lookup"><span data-stu-id="16dd0-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="16dd0-112">**IMsgServiceAdmin**インターフェイスの使用方法の詳細については、「message service の[構成](configuring-a-message-service.md)」、「[メッセージサービスのコピー](copying-a-message-service.md)」、および「[メッセージサービスの削除](deleting-a-message-service.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16dd0-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="16dd0-113">[IProfAdmin:](iprofadminiunknown.md) [MAPIAdminProfiles](mapiadminprofiles.md)関数を通じてアクセスできる、プロファイルを管理する IUnknown。</span><span class="sxs-lookup"><span data-stu-id="16dd0-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="16dd0-114">**IProfAdmin**インターフェイスの使用の詳細については、以下のトピックを参照してください。[カスタムコードを使用したプロファイルの作成](creating-a-profile-by-using-custom-code.md)、プロファイルの[コピー](copying-a-profile.md)、プロファイルの[削除](deleting-a-profile.md)、[プロファイル名の検索](finding-a-profile-name.md)、および[の設定既定のプロファイル](setting-a-default-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="16dd0-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="16dd0-115">[IProfSect: imapiprop](iprofsectimapiprop.md)を使用して、プロファイルセクションのプロパティを維持します。これには、 [imapiprop:: openprofile](imapisession-openprofilesection.md)または[IProviderAdmin:: openprofile](iprovideradmin-openprofilesection.md)のセクションメソッドを通じてアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="16dd0-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="16dd0-116">プロファイルセクションの詳細については、「 [MAPI プロファイル](mapi-profiles.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16dd0-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="16dd0-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md)を使用して、メッセージサービスのサービスプロバイダーを管理します。 [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)を通じてアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="16dd0-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="16dd0-118">**IProviderAdmin**インターフェイスの使用の詳細については、「[メッセージサービスでプロバイダーを追加または削除](adding-or-deleting-providers-in-a-message-service.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16dd0-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="16dd0-119">プロファイルとメッセージサービスの管理のサポートに注意してください。</span><span class="sxs-lookup"><span data-stu-id="16dd0-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="16dd0-120">使用されているプロファイルの悪影響から保護する対策はありません。</span><span class="sxs-lookup"><span data-stu-id="16dd0-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="16dd0-121">MAPI を使用すると、使用中のプロファイルを削除することはできませんが、すべてのメッセージサービスを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="16dd0-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="16dd0-122">プロファイル内のすべてのメッセージサービスを削除すると、これらのサービスのすべてのサービスプロバイダーが停止し、予期しない結果が発生する原因になります。</span><span class="sxs-lookup"><span data-stu-id="16dd0-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="16dd0-123">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="16dd0-123">In this section</span></span>

[<span data-ttu-id="16dd0-124">プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="16dd0-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="16dd0-125">プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="16dd0-126">プロファイルのコピー</span><span class="sxs-lookup"><span data-stu-id="16dd0-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="16dd0-127">プロファイルをコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="16dd0-128">プロファイルの削除</span><span class="sxs-lookup"><span data-stu-id="16dd0-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="16dd0-129">プロファイルを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="16dd0-130">既定のプロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="16dd0-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="16dd0-131">既定のプロファイルを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="16dd0-132">プロファイル名の検索</span><span class="sxs-lookup"><span data-stu-id="16dd0-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="16dd0-133">プロファイルの名前を検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="16dd0-134">メッセージサービスを追加する</span><span class="sxs-lookup"><span data-stu-id="16dd0-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="16dd0-135">メッセージサービスを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="16dd0-136">メッセージサービスの構成</span><span class="sxs-lookup"><span data-stu-id="16dd0-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="16dd0-137">メッセージサービスを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="16dd0-138">メッセージサービスのコピー</span><span class="sxs-lookup"><span data-stu-id="16dd0-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="16dd0-139">メッセージサービスをプロファイルにコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="16dd0-140">メッセージサービスの削除</span><span class="sxs-lookup"><span data-stu-id="16dd0-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="16dd0-141">メッセージサービスを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="16dd0-142">メッセージサービスでのプロバイダーの追加または削除</span><span class="sxs-lookup"><span data-stu-id="16dd0-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="16dd0-143">メッセージサービスでプロバイダーを追加または削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16dd0-143">Describes how to add or delete providers in a message service.</span></span>
    

