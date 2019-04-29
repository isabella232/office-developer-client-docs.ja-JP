---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: フレンドのフレンド、オンデマンドまたはハイブリッド同期の追加、アクティビティのオンデマンド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートしています。
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408832"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="51a5a-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51a5a-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="51a5a-104">フレンドのフレンド、オンデマンドまたはハイブリッド同期の追加、アクティビティのオンデマンド同期、またはキャッシュされた資格情報を使用したソーシャルネットワークへのログオンをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="51a5a-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="51a5a-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="51a5a-105">Members</span></span>

<span data-ttu-id="51a5a-106">次の表に、 **ISocialSession2**インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="51a5a-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="51a5a-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="51a5a-107">**Name**</span></span>|<span data-ttu-id="51a5a-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="51a5a-108">**Member type**</span></span>|<span data-ttu-id="51a5a-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="51a5a-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="51a5a-110">この例</span><span class="sxs-lookup"><span data-stu-id="51a5a-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="51a5a-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="51a5a-111">Method</span></span>  <br/> |<span data-ttu-id="51a5a-112">_emailaddresses_および_displayName_パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="51a5a-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="51a5a-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="51a5a-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="51a5a-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="51a5a-114">Method</span></span>  <br/> |<span data-ttu-id="51a5a-115">_hashedAddresses_パラメーターによって指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="51a5a-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="51a5a-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="51a5a-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="51a5a-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="51a5a-117">Method</span></span>  <br/> |<span data-ttu-id="51a5a-118">ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返し__ ます。</span><span class="sxs-lookup"><span data-stu-id="51a5a-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="51a5a-119">logoncached</span><span class="sxs-lookup"><span data-stu-id="51a5a-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="51a5a-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="51a5a-120">Method</span></span>  <br/> |<span data-ttu-id="51a5a-121">キャッシュされた資格情報を使用してソーシャルネットワークサイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="51a5a-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51a5a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="51a5a-122">Remarks</span></span>

<span data-ttu-id="51a5a-123">Outlook Social Connector (.osc) プロバイダーは、このインターフェイスを実装することができます。プロバイダーが、フレンドのオンデマンド同期、またはアクティビティのオンデマンド同期をサポートしている場合、またはキャッシュされた資格情報を使用してソーシャルネットワークにログオンしている場合です。</span><span class="sxs-lookup"><span data-stu-id="51a5a-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="51a5a-124">.osc プロバイダーが**ISocialSession2**を実装し、ソーシャルネットワークでフォローしているユーザーをサポートしている場合、.osc は i [alsession:: olperson](isocialsession-followperson.md)の代わりに[ISocialSession2:: olperson ex](isocialsession2-followpersonex.md)を呼び出し、プロバイダーが実装する必要があります。**ISocialSession2::** ということもあります。</span><span class="sxs-lookup"><span data-stu-id="51a5a-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51a5a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="51a5a-125">See also</span></span>

- [<span data-ttu-id="51a5a-126">Outlook Social Connector プロバイダーインターフェイス</span><span class="sxs-lookup"><span data-stu-id="51a5a-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

