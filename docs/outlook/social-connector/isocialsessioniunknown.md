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
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437827"
---
# <a name="isocialsession--iunknown"></a><span data-ttu-id="74114-103">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="74114-103">ISocialSession : IUnknown</span></span>

<span data-ttu-id="74114-104">ソーシャル ネットワーク サイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="74114-104">Represents a connection to a social network site.</span></span>
  
## <a name="members"></a><span data-ttu-id="74114-105">Members</span><span class="sxs-lookup"><span data-stu-id="74114-105">Members</span></span>

<span data-ttu-id="74114-106">次の表に **、ISocialSession** インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="74114-106">The following table shows the members that are available on the **ISocialSession** interface.</span></span> 
  
|<span data-ttu-id="74114-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="74114-107">**Name**</span></span>|<span data-ttu-id="74114-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="74114-108">**Member type**</span></span>|<span data-ttu-id="74114-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="74114-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="74114-110">FindPerson</span><span class="sxs-lookup"><span data-stu-id="74114-110">FindPerson</span></span>](isocialsession-findperson.md) <br/> |<span data-ttu-id="74114-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-111">Method</span></span>  <br/> |<span data-ttu-id="74114-112">userID パラメーターに一致する 1 人または複数のユーザーを表す  _文字列を取得_ します。</span><span class="sxs-lookup"><span data-stu-id="74114-112">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="74114-113">FollowPerson</span><span class="sxs-lookup"><span data-stu-id="74114-113">FollowPerson</span></span>](isocialsession-followperson.md) <br/> |<span data-ttu-id="74114-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-114">Method</span></span>  <br/> |<span data-ttu-id="74114-115">_emailAddress_ パラメーターで識別されたユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="74114-115">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="74114-116">GetActivities</span><span class="sxs-lookup"><span data-stu-id="74114-116">GetActivities</span></span>](isocialsession-getactivities.md) <br/> |<span data-ttu-id="74114-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-117">Method</span></span>  <br/> |<span data-ttu-id="74114-118">このメソッドは、ソーシャル Outlook (OSC) 1.1 で廃止されました。</span><span class="sxs-lookup"><span data-stu-id="74114-118">This method has been deprecated in Outlook Social Connector (OSC) 1.1.</span></span>  <br/> |
|[<span data-ttu-id="74114-119">GetLoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="74114-119">GetLoggedOnUser</span></span>](isocialsession-getloggedonuser.md) <br/> |<span data-ttu-id="74114-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-120">Method</span></span>  <br/> |<span data-ttu-id="74114-121">ログオンしている [ユーザーを表す ISocialProfile](isocialprofileisocialperson.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="74114-121">Gets an [ISocialProfile](isocialprofileisocialperson.md) interface that represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="74114-122">GetLogonUrl</span><span class="sxs-lookup"><span data-stu-id="74114-122">GetLogonUrl</span></span>](isocialsession-getlogonurl.md) <br/> |<span data-ttu-id="74114-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-123">Method</span></span>  <br/> |<span data-ttu-id="74114-124">Web 認証中にブラウザー ベースのフォームをユーザーに表示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="74114-124">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>  <br/> |
|[<span data-ttu-id="74114-125">GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="74114-125">GetNetworkIdentifier</span></span>](isocialsession-getnetworkidentifier.md) <br/> |<span data-ttu-id="74114-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-126">Method</span></span>  <br/> |<span data-ttu-id="74114-127">特定のソーシャル ネットワーク接続の一意のソーシャル ネットワーク識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="74114-127">Gets a string that represents a unique social network identifier for a given social network connection.</span></span>  <br/> |
|[<span data-ttu-id="74114-128">GetPerson</span><span class="sxs-lookup"><span data-stu-id="74114-128">GetPerson</span></span>](isocialsession-getperson.md) <br/> |<span data-ttu-id="74114-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-129">Method</span></span>  <br/> |<span data-ttu-id="74114-130">userID [パラメーターに基づいて ISocialPerson](isocialpersoniunknown.md) インターフェイス  _を取得_ します。</span><span class="sxs-lookup"><span data-stu-id="74114-130">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="74114-131">LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="74114-131">LoggedOnUserID</span></span>](isocialsession-loggedonuserid.md) <br/> |<span data-ttu-id="74114-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="74114-132">Property</span></span>  <br/> |<span data-ttu-id="74114-133">現在ログオンしているユーザーのソーシャル ネットワーク ユーザー ID を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="74114-133">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span>  <br/> |
|[<span data-ttu-id="74114-134">LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="74114-134">LoggedOnUserName</span></span>](isocialsession-loggedonusername.md) <br/> |<span data-ttu-id="74114-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="74114-135">Property</span></span>  <br/> |<span data-ttu-id="74114-136">ログオン時に使用されるユーザー名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="74114-136">Returns a string that represents the user name that is used when logging on.</span></span>  <br/> |
|[<span data-ttu-id="74114-137">Logon</span><span class="sxs-lookup"><span data-stu-id="74114-137">Logon</span></span>](isocialsession-logon.md) <br/> |<span data-ttu-id="74114-138">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-138">Method</span></span>  <br/> |<span data-ttu-id="74114-139">指定したユーザー名とパスワードを使用してソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="74114-139">Logs on to the social network site by using the specified user name and password.</span></span>  <br/> |
|[<span data-ttu-id="74114-140">LogonWeb</span><span class="sxs-lookup"><span data-stu-id="74114-140">LogonWeb</span></span>](isocialsession-logonweb.md) <br/> |<span data-ttu-id="74114-141">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-141">Method</span></span>  <br/> |<span data-ttu-id="74114-142">フォーム ベース認証を使用してソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="74114-142">Logs on to the social network site by using forms-based authentication.</span></span>  <br/> |
|[<span data-ttu-id="74114-143">SiteUrl</span><span class="sxs-lookup"><span data-stu-id="74114-143">SiteUrl</span></span>](isocialsession-siteurl.md) <br/> |<span data-ttu-id="74114-144">プロパティ</span><span class="sxs-lookup"><span data-stu-id="74114-144">Property</span></span>  <br/> |<span data-ttu-id="74114-145">ソーシャル ネットワーク サイトの URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="74114-145">Sets the social network site URL.</span></span>  <br/> |
|[<span data-ttu-id="74114-146">UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="74114-146">UnFollowPerson</span></span>](isocialsession-unfollowperson.md) <br/> |<span data-ttu-id="74114-147">メソッド</span><span class="sxs-lookup"><span data-stu-id="74114-147">Method</span></span>  <br/> |<span data-ttu-id="74114-148">ソーシャル ネットワーク上のフレンドとして  _userID_ パラメーターによって識別されたユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="74114-148">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74114-149">注釈</span><span class="sxs-lookup"><span data-stu-id="74114-149">Remarks</span></span>

<span data-ttu-id="74114-150">OSC プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74114-150">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="74114-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="74114-151">See also</span></span>

- [<span data-ttu-id="74114-152">Outlookソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="74114-152">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

