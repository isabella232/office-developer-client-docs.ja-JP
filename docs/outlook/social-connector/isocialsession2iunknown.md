---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408832"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="fc155-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc155-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="fc155-104">キャッシュされた資格情報を使用して、フレンドの追加、フレンドのオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、またはソーシャル ネットワークへのログオンをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc155-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="fc155-105">Members</span><span class="sxs-lookup"><span data-stu-id="fc155-105">Members</span></span>

<span data-ttu-id="fc155-106">次の表に **、ISocialSession2** インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="fc155-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="fc155-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="fc155-107">**Name**</span></span>|<span data-ttu-id="fc155-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="fc155-108">**Member type**</span></span>|<span data-ttu-id="fc155-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="fc155-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc155-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="fc155-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="fc155-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="fc155-111">Method</span></span>  <br/> |<span data-ttu-id="fc155-112">_emailAddresses_ パラメーターと _displayName_ パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。</span><span class="sxs-lookup"><span data-stu-id="fc155-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="fc155-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="fc155-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="fc155-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="fc155-114">Method</span></span>  <br/> |<span data-ttu-id="fc155-115">_hashedAddresses_ パラメーターで指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fc155-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="fc155-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="fc155-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="fc155-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="fc155-117">Method</span></span>  <br/> |<span data-ttu-id="fc155-118">_personsAddresses_ パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fc155-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="fc155-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="fc155-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="fc155-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="fc155-120">Method</span></span>  <br/> |<span data-ttu-id="fc155-121">キャッシュされた資格情報を使用してソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="fc155-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc155-122">注釈</span><span class="sxs-lookup"><span data-stu-id="fc155-122">Remarks</span></span>

<span data-ttu-id="fc155-123">Outlook ソーシャル コネクタ (OSC) プロバイダーは、プロバイダーが友人のオンデマンドまたはハイブリッド同期、アクティビティのオンデマンド同期、キャッシュされた資格情報を使用してソーシャル ネットワークにログオンする場合に、このインターフェイスを実装できます。</span><span class="sxs-lookup"><span data-stu-id="fc155-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="fc155-124">OSC プロバイダーが **ISocialSession2** を実装し、ソーシャル ネットワーク上で次のユーザーをサポートしている場合、OSC は [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出し、プロバイダーは **ISocialSession2::FollowPersonEx** も実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc155-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc155-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc155-125">See also</span></span>

- [<span data-ttu-id="fc155-126">Outlookソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="fc155-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

