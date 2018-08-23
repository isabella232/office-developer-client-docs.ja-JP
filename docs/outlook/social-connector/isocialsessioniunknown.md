---
title: ISocialSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: ソーシャル ネットワーク サイトへの接続を表します。
ms.openlocfilehash: ee3a8aa72ea187b4c211bc7a49e8a2dbe170adad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804381"
---
# <a name="isocialsession--iunknown"></a><span data-ttu-id="3df58-103">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3df58-103">ISocialSession : IUnknown</span></span>

<span data-ttu-id="3df58-104">ソーシャル ネットワーク サイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="3df58-104">Represents a connection to a social network site.</span></span>
  
## <a name="members"></a><span data-ttu-id="3df58-105">Members</span><span class="sxs-lookup"><span data-stu-id="3df58-105">Members</span></span>

<span data-ttu-id="3df58-106">次の表は、 **ISocialSession**インターフェイスで使用可能なメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="3df58-106">The following table shows the members that are available on the **ISocialSession** interface.</span></span> 
  
|<span data-ttu-id="3df58-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="3df58-107">**Name**</span></span>|<span data-ttu-id="3df58-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="3df58-108">**Member type**</span></span>|<span data-ttu-id="3df58-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="3df58-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3df58-110">FindPerson</span><span class="sxs-lookup"><span data-stu-id="3df58-110">FindPerson</span></span>](isocialsession-findperson.md) <br/> |<span data-ttu-id="3df58-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-111">Method</span></span>  <br/> |<span data-ttu-id="3df58-112">_ユーザー Id_パラメーターに一致する 1 つまたは複数の人物を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3df58-112">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="3df58-113">FollowPerson</span><span class="sxs-lookup"><span data-stu-id="3df58-113">FollowPerson</span></span>](isocialsession-followperson.md) <br/> |<span data-ttu-id="3df58-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-114">Method</span></span>  <br/> |<span data-ttu-id="3df58-115">ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddress_パラメーターで識別されるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="3df58-115">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="3df58-116">GetActivities</span><span class="sxs-lookup"><span data-stu-id="3df58-116">GetActivities</span></span>](isocialsession-getactivities.md) <br/> |<span data-ttu-id="3df58-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-117">Method</span></span>  <br/> |<span data-ttu-id="3df58-118">この方法で Outlook ソーシャル コネクタ (OSC) 1.1 は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="3df58-118">This method has been deprecated in Outlook Social Connector (OSC) 1.1.</span></span>  <br/> |
|[<span data-ttu-id="3df58-119">GetLoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="3df58-119">GetLoggedOnUser</span></span>](isocialsession-getloggedonuser.md) <br/> |<span data-ttu-id="3df58-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-120">Method</span></span>  <br/> |<span data-ttu-id="3df58-121">ログオン中のユーザーを表す[ISocialProfile](isocialprofileisocialperson.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="3df58-121">Gets an [ISocialProfile](isocialprofileisocialperson.md) interface that represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="3df58-122">GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="3df58-122">GetLogonUrl</span></span>](isocialsession-getlogonurl.md) <br/> |<span data-ttu-id="3df58-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-123">Method</span></span>  <br/> |<span data-ttu-id="3df58-124">Web 認証時にユーザーにブラウザー ベースのフォームを表示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3df58-124">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>  <br/> |
|[<span data-ttu-id="3df58-125">GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="3df58-125">GetNetworkIdentifier</span></span>](isocialsession-getnetworkidentifier.md) <br/> |<span data-ttu-id="3df58-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-126">Method</span></span>  <br/> |<span data-ttu-id="3df58-127">特定のソーシャル ネットワークの接続のソーシャル ネットワークの一意の識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3df58-127">Gets a string that represents a unique social network identifier for a given social network connection.</span></span>  <br/> |
|[<span data-ttu-id="3df58-128">GetPerson</span><span class="sxs-lookup"><span data-stu-id="3df58-128">GetPerson</span></span>](isocialsession-getperson.md) <br/> |<span data-ttu-id="3df58-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-129">Method</span></span>  <br/> |<span data-ttu-id="3df58-130">_ユーザー Id_のパラメーターに基づいて、 [ISocialPerson](isocialpersoniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="3df58-130">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="3df58-131">LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="3df58-131">LoggedOnUserID</span></span>](isocialsession-loggedonuserid.md) <br/> |<span data-ttu-id="3df58-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3df58-132">Property</span></span>  <br/> |<span data-ttu-id="3df58-133">現在ログオンしているユーザーのソーシャル ネットワークのユーザー ID を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="3df58-133">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span>  <br/> |
|[<span data-ttu-id="3df58-134">LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="3df58-134">LoggedOnUserName</span></span>](isocialsession-loggedonusername.md) <br/> |<span data-ttu-id="3df58-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3df58-135">Property</span></span>  <br/> |<span data-ttu-id="3df58-136">ログオン時に使用されるユーザー名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="3df58-136">Returns a string that represents the user name that is used when logging on.</span></span>  <br/> |
|[<span data-ttu-id="3df58-137">Logon</span><span class="sxs-lookup"><span data-stu-id="3df58-137">Logon</span></span>](isocialsession-logon.md) <br/> |<span data-ttu-id="3df58-138">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-138">Method</span></span>  <br/> |<span data-ttu-id="3df58-139">指定されたユーザー名とパスワードを使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="3df58-139">Logs on to the social network site by using the specified user name and password.</span></span>  <br/> |
|[<span data-ttu-id="3df58-140">LogonWeb</span><span class="sxs-lookup"><span data-stu-id="3df58-140">LogonWeb</span></span>](isocialsession-logonweb.md) <br/> |<span data-ttu-id="3df58-141">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-141">Method</span></span>  <br/> |<span data-ttu-id="3df58-142">フォーム ベース認証を使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="3df58-142">Logs on to the social network site by using forms-based authentication.</span></span>  <br/> |
|[<span data-ttu-id="3df58-143">SiteUrl</span><span class="sxs-lookup"><span data-stu-id="3df58-143">SiteUrl</span></span>](isocialsession-siteurl.md) <br/> |<span data-ttu-id="3df58-144">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3df58-144">Property</span></span>  <br/> |<span data-ttu-id="3df58-145">ソーシャル ネットワーク サイトの URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="3df58-145">Sets the social network site URL.</span></span>  <br/> |
|[<span data-ttu-id="3df58-146">UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="3df58-146">UnFollowPerson</span></span>](isocialsession-unfollowperson.md) <br/> |<span data-ttu-id="3df58-147">メソッド</span><span class="sxs-lookup"><span data-stu-id="3df58-147">Method</span></span>  <br/> |<span data-ttu-id="3df58-148">ソーシャル ネットワークの友人として、_ユーザー Id_のパラメーターで識別されるユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="3df58-148">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3df58-149">注釈</span><span class="sxs-lookup"><span data-stu-id="3df58-149">Remarks</span></span>

<span data-ttu-id="3df58-150">OSC プロバイダーでは、OSC と通信するには、このインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3df58-150">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3df58-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="3df58-151">See also</span></span>

- [<span data-ttu-id="3df58-152">Outlook ソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3df58-152">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

