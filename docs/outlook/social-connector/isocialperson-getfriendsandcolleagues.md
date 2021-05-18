---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: ユーザーのコレクションを表す文字列を取得します。
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407656"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="12006-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="12006-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="12006-104">ユーザーのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="12006-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="12006-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="12006-105">Parameters</span></span>

<span data-ttu-id="12006-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="12006-106">_personsCollection_</span></span>
  
> <span data-ttu-id="12006-107">[out]ユーザーのフレンドのセットを表し、Outlook Social Connector (OSC) プロバイダーの機能拡張の XML スキーマで定義されているフレンドの定義に準拠する XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="12006-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="12006-108">注釈</span><span class="sxs-lookup"><span data-stu-id="12006-108">Remarks</span></span>

<span data-ttu-id="12006-109">OSC プロバイダーがソーシャル ネットワーク上の友人のキャッシュまたはハイブリッド同期をサポートしている場合、OSC は **GetFriendsAndColleagues** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="12006-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="12006-110">OSC が最初に、ソーシャル ネットワークにログオンしている Outlook ユーザーの **GetFriendsAndColleagues** メソッドを呼び出す場合 **、GetFriendsAndColleagues** は、ソーシャル ネットワーク上でログオンしているユーザーの友人を表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="12006-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="12006-111">XML 文字列はフレンド **XML** スキーマ定義に準拠し、各フレンドの person 要素 (OSC プロバイダー スキーマ定義にも準拠) を指定します。</span><span class="sxs-lookup"><span data-stu-id="12006-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="12006-112">**GetFriendsAndColleagues** がログオンしているユーザーのフレンド情報を返す場合、OSC は連絡先フォルダーにその情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="12006-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="12006-113">このフォルダーはソーシャル ネットワークに固有のフォルダーで、ログオンしているユーザーの既定のユーザー ストアにOutlookされます。</span><span class="sxs-lookup"><span data-stu-id="12006-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="12006-114">OSC が連絡先フォルダーに友人の情報をキャッシュする方法の詳細については、「友人とアクティビティの同期」 [を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="12006-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="12006-115">_personsCollection_ パラメーターで返される各フレンドの情報は、ユーザーの XML スキーマ定義に準拠 **しています**。</span><span class="sxs-lookup"><span data-stu-id="12006-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="12006-116">person要素は、フレンドがソーシャル ネットワークで指定した SMTP メール アドレス (emailAddress、emailAddress2、emailAddress3 要素にマップされる) や、ソーシャル ネットワーク上のそのフレンドを識別するユーザー ID **(userID** 要素にマップされる) など、各フレンドの多くの情報をサポートします。   </span><span class="sxs-lookup"><span data-stu-id="12006-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="12006-117">ユーザー ウィンドウで選択された Outlook ユーザーのアクティビティを表示するには、OSC は **GetFriendsAndColleagues** から返された各フレンドとユーザーの一致を試行します。</span><span class="sxs-lookup"><span data-stu-id="12006-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="12006-118">OSC は、選択したユーザーの SMTP アドレスOutlook、各フレンドがソーシャル ネットワークで指定した電子メール アドレスと照合します。</span><span class="sxs-lookup"><span data-stu-id="12006-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="12006-119">OSC が一致する SMTP 電子メール アドレスを見つけた場合、OSC はフレンドの対応する **userID** を使用して [ISocialSession::GetPerson](isocialsession-getperson.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="12006-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="12006-120">これは、そのフレンドの [ISocialPerson](isocialpersoniunknown.md) オブジェクトを取得するために行います。これにより、OSC はソーシャル ネットワークからその友人のアクティビティと写真を取得できます。</span><span class="sxs-lookup"><span data-stu-id="12006-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="12006-121">ただし、選択した Outlook ユーザーがソーシャル ネットワーク上のアカウントで同じ SMTP アドレスを指定しない場合、または Outlook ユーザーがそのソーシャル ネットワーク上のアカウントを持ってない場合、OSC は、そのユーザーに一致する一致を見つけ、そのユーザーのアクティビティをソーシャル ネットワーク上に表示しません。</span><span class="sxs-lookup"><span data-stu-id="12006-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12006-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="12006-122">See also</span></span>

- [<span data-ttu-id="12006-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12006-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="12006-124">フレンド情報の取得</span><span class="sxs-lookup"><span data-stu-id="12006-124">Getting Friends Information</span></span>](getting-friends-information.md)

