---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: キャッシュされた資格情報を使用して、友人、友人の同期をオン ・ デマンドまたはハイブリッド、活動、またはソーシャル ネットワークへのログオンのオンデマンドの同期を追加することをサポートします。
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804376"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="427b6-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="427b6-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="427b6-104">キャッシュされた資格情報を使用して、友人、友人の同期をオン ・ デマンドまたはハイブリッド、活動、またはソーシャル ネットワークへのログオンのオンデマンドの同期を追加することをサポートします。</span><span class="sxs-lookup"><span data-stu-id="427b6-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="427b6-105">Members</span><span class="sxs-lookup"><span data-stu-id="427b6-105">Members</span></span>

<span data-ttu-id="427b6-106">次の表は、 **ISocialSession2**インターフェイスで使用可能なメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="427b6-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="427b6-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="427b6-107">**Name**</span></span>|<span data-ttu-id="427b6-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="427b6-108">**Member type**</span></span>|<span data-ttu-id="427b6-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="427b6-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="427b6-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="427b6-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="427b6-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="427b6-111">Method</span></span>  <br/> |<span data-ttu-id="427b6-112">ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddresses_パラメーターと_displayName_パラメーターで識別されるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="427b6-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="427b6-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="427b6-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="427b6-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="427b6-114">Method</span></span>  <br/> |<span data-ttu-id="427b6-115">_HashedAddresses_パラメーターで指定されたユーザーのアクティビティのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="427b6-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="427b6-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="427b6-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="427b6-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="427b6-117">Method</span></span>  <br/> |<span data-ttu-id="427b6-118">_PersonsAddresses_パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="427b6-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="427b6-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="427b6-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="427b6-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="427b6-120">Method</span></span>  <br/> |<span data-ttu-id="427b6-121">キャッシュされた資格情報を使用して、ソーシャル ネットワーク サイトにログオンします。</span><span class="sxs-lookup"><span data-stu-id="427b6-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="427b6-122">注釈</span><span class="sxs-lookup"><span data-stu-id="427b6-122">Remarks</span></span>

<span data-ttu-id="427b6-123">プロバイダーがキャッシュされた資格情報を使用して、友人のオン ・ デマンドまたはハイブリッドの同期、オンデマンドの同期活動、またはソーシャル ネットワークへのログオンをサポートしている場合、このインターフェイスを実装するために、Outlook ソーシャル コネクタ (OSC) プロバイダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="427b6-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="427b6-124">OSC プロバイダーは、 **ISocialSession2**と次の人をソーシャル ネットワークのサポートを実装する場合は、OSC では、 [ISocialSession::FollowPerson](isocialsession-followperson.md)、代わりに[ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)を呼び出して、プロバイダーを実装する必要があります。**ISocialSession2::FollowPersonEx**も同様です。</span><span class="sxs-lookup"><span data-stu-id="427b6-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="427b6-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="427b6-125">See also</span></span>

- [<span data-ttu-id="427b6-126">Outlook ソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="427b6-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

