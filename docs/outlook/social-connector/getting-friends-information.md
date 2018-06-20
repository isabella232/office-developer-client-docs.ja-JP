---
title: フレンド情報の取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する ISocialProvider::GetCapabilities メソッドを呼び出します。
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804329"
---
# <a name="getting-friends-information"></a><span data-ttu-id="da92c-103">フレンド情報の取得</span><span class="sxs-lookup"><span data-stu-id="da92c-103">Getting friends information</span></span>

<span data-ttu-id="da92c-104">Outlook ソーシャル コネクタ (OSC) では、ソーシャル ネットワークの OSC プロバイダーの機能を決定する[ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="da92c-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="da92c-105">**機能**の返された XML 内の**getFriends**と**cacheFriends**の要素を示す OSC プロバイダーには、取得の友人がサポートしていることと、対応する連絡先フォルダー内のアイテムが Outlook とキャッシュの友人にお問い合わせください、OSC のことができます。次の呼び出しシーケンスです。</span><span class="sxs-lookup"><span data-stu-id="da92c-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="da92c-106">OSC では、取得する情報と画像 ( [ISocialPerson](isocialpersoniunknown.md)インターフェイスでサポートされている)、ソーシャル ネットワーク上の友人のこの順序でメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="da92c-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="da92c-107">OSC では、既定の間隔でキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="da92c-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="da92c-108">キャッシュ中にエラーが発生した場合を更新する XML の**機能**に**contactSyncRestartInterval**要素を指定することによって制御することも別のプリセットの間隔で OSC 再試行します。</span><span class="sxs-lookup"><span data-stu-id="da92c-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="da92c-109">連絡先のキャッシュの更新の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da92c-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="da92c-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) -「OSC は、ソーシャル ネットワークにログオンしている Office ユーザーのユーザー ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="da92c-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="da92c-111">[ISocialSession::GetPerson](isocialsession-getperson.md) -Office ユーザーのユーザー ID を使用すると、OSC **ISocialPerson**のオブジェクトを取得するユーザーです。</span><span class="sxs-lookup"><span data-stu-id="da92c-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="da92c-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -「OSC は、ソーシャル ネットワークのユーザーのフレンド リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="da92c-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="da92c-113">[ISocialSession::GetPerson](isocialsession-getperson.md) : XML の各メンバーは、 **GetFriendsAndColleagues**によって返される、ため、OSC は**ISocialPerson**インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="da92c-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="da92c-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) -、OSC が画像リソースを取得する XML の各メンバーは、 **GetFriendsAndColleagues**によって返される、ためです。</span><span class="sxs-lookup"><span data-stu-id="da92c-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da92c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="da92c-115">See also</span></span>

- [<span data-ttu-id="da92c-116">機能のための XML</span><span class="sxs-lookup"><span data-stu-id="da92c-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="da92c-117">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="da92c-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

