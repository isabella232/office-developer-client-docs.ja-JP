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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331662"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="7fc18-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="7fc18-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="7fc18-104">ユーザーのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="7fc18-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7fc18-105">Parameters</span></span>

<span data-ttu-id="7fc18-106">_個人コレクション_</span><span class="sxs-lookup"><span data-stu-id="7fc18-106">_personsCollection_</span></span>
  
> <span data-ttu-id="7fc18-107">読み上げ個人のフレンドのセットを表す xml 文字列。 Outlook Social Connector (.osc) プロバイダー拡張機能の XML スキーマで定義されているように、**フレンド**の定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="7fc18-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7fc18-108">解説</span><span class="sxs-lookup"><span data-stu-id="7fc18-108">Remarks</span></span>

<span data-ttu-id="7fc18-109">.osc プロバイダーがソーシャルネットワーク上で友人のキャッシュまたはハイブリッド同期をサポートしている場合、.osc 呼び出しは**GetFriendsAndColleagues**になります。</span><span class="sxs-lookup"><span data-stu-id="7fc18-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="7fc18-110">ソーシャルネットワークにログオンしている Outlook ユーザーの**GetFriendsAndColleagues**メソッドを最初に呼び出すときに、 **GetFriendsAndColleagues**は、ソーシャルネットワーク上でログオンしているユーザーのフレンドを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="7fc18-111">xml 文字列は、フレンド xml \*\*\*\* スキーマ定義に準拠しており、各フレンドの**person**要素 (.osc プロバイダースキーマ定義にも準拠) を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="7fc18-112">**GetFriendsAndColleagues**がログオンユーザーのフレンド情報を返すと、.osc は連絡先フォルダーにその情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="7fc18-113">このフォルダーは、ソーシャルネットワークに固有のものであり、ログオンしているユーザーの既定の Outlook ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="7fc18-114">.osc が連絡先フォルダー内のフレンド情報をキャッシュする方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7fc18-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="7fc18-115">個人_コレクション_パラメーターに返される各フレンドの情報は、 **person**の XML スキーマ定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="7fc18-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="7fc18-116">**person**要素は、各フレンドの多くの情報 ( **emailAddress**、 **emailAddress2**、および**emailAddress3**要素にマップされる) をサポートしており、その中で友人が指定したソーシャルネットワークと、ソーシャルネットワーク上でその友人を識別するユーザー ID ( **userID**要素にマップされます)。</span><span class="sxs-lookup"><span data-stu-id="7fc18-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="7fc18-117">[ユーザー] ウィンドウで選択された Outlook ユーザーのアクティビティを表示するために、.osc は、 **GetFriendsAndColleagues**から返された各フレンドに対してユーザーを照合しようとします。</span><span class="sxs-lookup"><span data-stu-id="7fc18-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="7fc18-118">.osc は、選択された Outlook ユーザーの SMTP アドレスを、各フレンドがソーシャルネットワーク上で指定した電子メールアドレスと照合することによって、これを行います。</span><span class="sxs-lookup"><span data-stu-id="7fc18-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="7fc18-119">一致する SMTP 電子メールアドレスを、.osc が検出した場合、.osc はフレンドの対応する**userID**を使用して、 [isocialsession:: getperson](isocialsession-getperson.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7fc18-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="7fc18-120">これにより、そのフレンドの[isocial alperson](isocialpersoniunknown.md)オブジェクトが取得されます。これにより、.osc がその友人のアクティビティと画像をソーシャルネットワークから取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7fc18-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="7fc18-121">ただし、選択した outlook ユーザーがソーシャルネットワーク上のアカウントで同じ SMTP アドレスを指定していない場合、または outlook ユーザーがそのソーシャルネットワークにアカウントを持っていない場合、そのユーザーに対して一致するものを検索することができず、activiti が表示されません。そのユーザーのソーシャルネットワーク上での es。</span><span class="sxs-lookup"><span data-stu-id="7fc18-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7fc18-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="7fc18-122">See also</span></span>

- [<span data-ttu-id="7fc18-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7fc18-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="7fc18-124">フレンド情報の取得</span><span class="sxs-lookup"><span data-stu-id="7fc18-124">Getting Friends Information</span></span>](getting-friends-information.md)

