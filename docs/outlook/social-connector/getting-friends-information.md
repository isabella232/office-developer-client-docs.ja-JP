---
title: 友だち情報の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Outlook social Connector (.osc) は、imethod alprovider:: getcapabilities メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428796"
---
# <a name="getting-friends-information"></a><span data-ttu-id="f008d-103">友だち情報の取得</span><span class="sxs-lookup"><span data-stu-id="f008d-103">Getting friends information</span></span>

<span data-ttu-id="f008d-104">Outlook social Connector (.osc) は、 [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出して、ソーシャルネットワークの .osc プロバイダーの機能を判別します。</span><span class="sxs-lookup"><span data-stu-id="f008d-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="f008d-105">返された**機能**XML の**getfriends**要素と**cacheFriends**要素が、.osc プロバイダーが、対応する連絡先フォルダーにある Outlook の連絡先アイテムとしてフレンドをキャッシュすることをサポートしていることを示している場合は、.osc次の呼び出しシーケンス。</span><span class="sxs-lookup"><span data-stu-id="f008d-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="f008d-106">.osc は、このシーケンスのメソッドを呼び出して、ソーシャルネットワーク上のフレンドの情報と画像 ( [isocial alperson](isocialpersoniunknown.md)インターフェイスでサポートされる) を取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f008d-107">.osc は、既定の間隔でキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="f008d-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="f008d-108">キャッシュ更新中にエラーが発生した場合、.osc は別の事前設定された間隔で再試行を行います。これは、 **capabilities** XML の**contactsyncrestartinterval**要素を指定することによって制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="f008d-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="f008d-109">連絡先キャッシュの更新の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f008d-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="f008d-110">[iLoggedOnUserID alsession::](isocialsession-loggedonuserid.md) — .osc は、ソーシャルネットワークにログオンしている Office ユーザーのユーザー ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="f008d-111">i入力された[セッション:: getperson](isocialsession-getperson.md) -Office ユーザーのユーザー ID を使用して、.osc はそのユーザーの**isocialsession**オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="f008d-112">[iGetFriendsAndColleagues:](isocialperson-getfriendsandcolleagues.md) .osc は、ソーシャルネットワーク上のユーザーのフレンドリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="f008d-113">[iGetFriendsAndColleagues alsession:: getperson](isocialsession-getperson.md) — \*\*\*\* によって返される XML 内の各ユーザーについて、.osc は**i alperson**インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="f008d-114">[ichanged alperson:: getpicture](isocialperson-getpicture.md) — **GetFriendsAndColleagues**によって返される XML 内の各ユーザーについて、.osc が画像リソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="f008d-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f008d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f008d-115">See also</span></span>

- [<span data-ttu-id="f008d-116">機能の XML</span><span class="sxs-lookup"><span data-stu-id="f008d-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="f008d-117">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="f008d-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

