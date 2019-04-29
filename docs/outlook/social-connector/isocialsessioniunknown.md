---
title: i、alsession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fe423d7-b044-479b-89ad-c39620eedd65
description: ソーシャルネットワークサイトへの接続を表します。
ms.openlocfilehash: c60fab1c27d2f761db28ed06bb45080857630e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437827"
---
# <a name="isocialsession--iunknown"></a><span data-ttu-id="f5930-103">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5930-103">ISocialSession : IUnknown</span></span>

<span data-ttu-id="f5930-104">ソーシャルネットワークサイトへの接続を表します。</span><span class="sxs-lookup"><span data-stu-id="f5930-104">Represents a connection to a social network site.</span></span>
  
## <a name="members"></a><span data-ttu-id="f5930-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="f5930-105">Members</span></span>

<span data-ttu-id="f5930-106">次の表に、 **iare alsession**インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="f5930-106">The following table shows the members that are available on the **ISocialSession** interface.</span></span> 
  
|<span data-ttu-id="f5930-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="f5930-107">**Name**</span></span>|<span data-ttu-id="f5930-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="f5930-108">**Member type**</span></span>|<span data-ttu-id="f5930-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="f5930-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5930-110">findperson</span><span class="sxs-lookup"><span data-stu-id="f5930-110">FindPerson</span></span>](isocialsession-findperson.md) <br/> |<span data-ttu-id="f5930-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-111">Method</span></span>  <br/> |<span data-ttu-id="f5930-112">_userID_パラメーターに一致する1人以上の人物を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5930-112">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="f5930-113">ユーザー</span><span class="sxs-lookup"><span data-stu-id="f5930-113">FollowPerson</span></span>](isocialsession-followperson.md) <br/> |<span data-ttu-id="f5930-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-114">Method</span></span>  <br/> |<span data-ttu-id="f5930-115">ソーシャルネットワークにログオンしているユーザーのフレンドとして、 _emailAddress_パラメーターによって識別された人物を追加します。</span><span class="sxs-lookup"><span data-stu-id="f5930-115">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="f5930-116">getactivities</span><span class="sxs-lookup"><span data-stu-id="f5930-116">GetActivities</span></span>](isocialsession-getactivities.md) <br/> |<span data-ttu-id="f5930-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-117">Method</span></span>  <br/> |<span data-ttu-id="f5930-118">このメソッドは、Outlook Social Connector (.osc) 1.1 で廃止されました。</span><span class="sxs-lookup"><span data-stu-id="f5930-118">This method has been deprecated in Outlook Social Connector (OSC) 1.1.</span></span>  <br/> |
|[<span data-ttu-id="f5930-119">GetLoggedOnUser</span><span class="sxs-lookup"><span data-stu-id="f5930-119">GetLoggedOnUser</span></span>](isocialsession-getloggedonuser.md) <br/> |<span data-ttu-id="f5930-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-120">Method</span></span>  <br/> |<span data-ttu-id="f5930-121">ログオンユーザーを表す[isocialprofile](isocialprofileisocialperson.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5930-121">Gets an [ISocialProfile](isocialprofileisocialperson.md) interface that represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="f5930-122">getlogonurl</span><span class="sxs-lookup"><span data-stu-id="f5930-122">GetLogonUrl</span></span>](isocialsession-getlogonurl.md) <br/> |<span data-ttu-id="f5930-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-123">Method</span></span>  <br/> |<span data-ttu-id="f5930-124">web 認証中にブラウザーベースのフォームをユーザーに提示するために使用される URL を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5930-124">Gets a string that represents a URL that is used for presenting a browser-based form to the user during web authentication.</span></span>  <br/> |
|[<span data-ttu-id="f5930-125">getnetworkidentifier</span><span class="sxs-lookup"><span data-stu-id="f5930-125">GetNetworkIdentifier</span></span>](isocialsession-getnetworkidentifier.md) <br/> |<span data-ttu-id="f5930-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-126">Method</span></span>  <br/> |<span data-ttu-id="f5930-127">特定のソーシャルネットワーク接続の一意のソーシャルネットワーク識別子を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5930-127">Gets a string that represents a unique social network identifier for a given social network connection.</span></span>  <br/> |
|[<span data-ttu-id="f5930-128">getperson</span><span class="sxs-lookup"><span data-stu-id="f5930-128">GetPerson</span></span>](isocialsession-getperson.md) <br/> |<span data-ttu-id="f5930-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-129">Method</span></span>  <br/> |<span data-ttu-id="f5930-130">_userID_パラメーターに基づいて[isocialperson](isocialpersoniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5930-130">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="f5930-131">LoggedOnUserID</span><span class="sxs-lookup"><span data-stu-id="f5930-131">LoggedOnUserID</span></span>](isocialsession-loggedonuserid.md) <br/> |<span data-ttu-id="f5930-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5930-132">Property</span></span>  <br/> |<span data-ttu-id="f5930-133">現在ログオンしているユーザーのソーシャルネットワークユーザー ID を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f5930-133">Returns a string that represents the social network user ID of the user who is currently logged on.</span></span>  <br/> |
|[<span data-ttu-id="f5930-134">LoggedOnUserName</span><span class="sxs-lookup"><span data-stu-id="f5930-134">LoggedOnUserName</span></span>](isocialsession-loggedonusername.md) <br/> |<span data-ttu-id="f5930-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5930-135">Property</span></span>  <br/> |<span data-ttu-id="f5930-136">ログオン時に使用されるユーザー名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f5930-136">Returns a string that represents the user name that is used when logging on.</span></span>  <br/> |
|[<span data-ttu-id="f5930-137">Logon</span><span class="sxs-lookup"><span data-stu-id="f5930-137">Logon</span></span>](isocialsession-logon.md) <br/> |<span data-ttu-id="f5930-138">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-138">Method</span></span>  <br/> |<span data-ttu-id="f5930-139">指定したユーザー名とパスワードを使用して、ソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f5930-139">Logs on to the social network site by using the specified user name and password.</span></span>  <br/> |
|[<span data-ttu-id="f5930-140">logonweb</span><span class="sxs-lookup"><span data-stu-id="f5930-140">LogonWeb</span></span>](isocialsession-logonweb.md) <br/> |<span data-ttu-id="f5930-141">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-141">Method</span></span>  <br/> |<span data-ttu-id="f5930-142">フォームベース認証を使用してソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f5930-142">Logs on to the social network site by using forms-based authentication.</span></span>  <br/> |
|[<span data-ttu-id="f5930-143">SiteUrl</span><span class="sxs-lookup"><span data-stu-id="f5930-143">SiteUrl</span></span>](isocialsession-siteurl.md) <br/> |<span data-ttu-id="f5930-144">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5930-144">Property</span></span>  <br/> |<span data-ttu-id="f5930-145">ソーシャルネットワークサイトの URL を設定します。</span><span class="sxs-lookup"><span data-stu-id="f5930-145">Sets the social network site URL.</span></span>  <br/> |
|[<span data-ttu-id="f5930-146">個人</span><span class="sxs-lookup"><span data-stu-id="f5930-146">UnFollowPerson</span></span>](isocialsession-unfollowperson.md) <br/> |<span data-ttu-id="f5930-147">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5930-147">Method</span></span>  <br/> |<span data-ttu-id="f5930-148">_userID_パラメーターで指定された人物をソーシャルネットワーク上のフレンドとして削除します。</span><span class="sxs-lookup"><span data-stu-id="f5930-148">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5930-149">注釈</span><span class="sxs-lookup"><span data-stu-id="f5930-149">Remarks</span></span>

<span data-ttu-id="f5930-150">.osc プロバイダーは、このインターフェイスを実装して、.osc と通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5930-150">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5930-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5930-151">See also</span></span>

- [<span data-ttu-id="f5930-152">Outlook Social Connector プロバイダーインターフェイス</span><span class="sxs-lookup"><span data-stu-id="f5930-152">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

