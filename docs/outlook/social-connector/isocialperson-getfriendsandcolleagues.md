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
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804348"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="d1561-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="d1561-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="d1561-104">ユーザーのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="d1561-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="d1561-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1561-105">Parameters</span></span>

<span data-ttu-id="d1561-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="d1561-106">_personsCollection_</span></span>
  
> <span data-ttu-id="d1561-107">[out]XML 文字列をユーザーの友人のセットを表し、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張用の XML スキーマで定義されている、**友人**の定義に準拠しています。</span><span class="sxs-lookup"><span data-stu-id="d1561-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d1561-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d1561-108">Remarks</span></span>

<span data-ttu-id="d1561-109">OSC は、ソーシャル ネットワーク上の**GetFriendsAndColleagues** OSC プロバイダーをサポートしていますがキャッシュされている場合、またはハイブリッドの同期の友人を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1561-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="d1561-110">OSC 最初にメソッドを呼び出して、 **GetFriendsAndColleagues** **GetFriendsAndColleagues** 、ソーシャル ネットワークにログオンしている Outlook ユーザーのソーシャル ネットワークにログオン中のユーザーの友人を表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d1561-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="d1561-111">XML 文字列では、**友人**の XML スキーマ定義に準拠し、各フレンドの**人**の要素 (OSC プロバイダーのスキーマ定義に準拠しても) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1561-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="d1561-112">**GetFriendsAndColleagues**が返されるとき、友人にログオンしたユーザーの情報、OSC は、連絡先フォルダーに情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="d1561-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="d1561-113">このフォルダーでは、ソーシャル ネットワークに固有では、ログオンしているユーザーの既定の Outlook ストアに存在します。</span><span class="sxs-lookup"><span data-stu-id="d1561-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="d1561-114">OSC が連絡先フォルダー内の友人の情報をキャッシュする方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1561-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="d1561-115">_PersonsCollection_パラメーターで返される各フレンドの情報は、**ユーザー**の XML スキーマ定義に準拠します。</span><span class="sxs-lookup"><span data-stu-id="d1561-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="d1561-116">**人**要素情報の多くの部分をサポートして、SMTP 電子メール アドレス ( **emailAddress**、 **emailAddress2**、および**emailAddress3**の要素にマップする) を含む、各フレンドのフレンドを指定する、ソーシャル ネットワーク、および、ユーザー ID (**ユーザー Id**の要素にマップする)、ソーシャル ネットワーク上の友人を識別します。</span><span class="sxs-lookup"><span data-stu-id="d1561-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="d1561-117">人物情報ウィンドウで選択されている Outlook のユーザーのアクティビティを表示するには、OSC は、 **GetFriendsAndColleagues**から返されるそれぞれの友人とのユーザーの一致を試みます。</span><span class="sxs-lookup"><span data-stu-id="d1561-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="d1561-118">OSC 各友人がソーシャル ネットワークに指定した電子メール アドレスを選択した Outlook のユーザーの SMTP アドレスを照合することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="d1561-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="d1561-119">OSC では、一致する SMTP 電子メール アドレスを検出した場合、OSC は[ISocialSession::GetPerson](isocialsession-getperson.md)メソッドを呼び出す、友人の対応する**ユーザー Id**を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1561-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="d1561-120">これは、その友人は、ソーシャル ネットワークの活動とその友人の画像を取得するのには OSC を有効にし、 [ISocialPerson](isocialpersoniunknown.md)オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d1561-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="d1561-121">ただし、選択した Outlook ユーザーは、ソーシャル ネットワーク上のアカウントで同じ SMTP アドレスを指定しない場合、または Outlook のユーザーはソーシャル ネットワークのアカウントを持っていない場合は、OSC ユーザーの一致を検索することはできませんし、activiti は表示されません。es ソーシャル ネットワークのユーザーにします。</span><span class="sxs-lookup"><span data-stu-id="d1561-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1561-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1561-122">See also</span></span>

- [<span data-ttu-id="d1561-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1561-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="d1561-124">フレンド情報の取得</span><span class="sxs-lookup"><span data-stu-id="d1561-124">Getting Friends Information</span></span>](getting-friends-information.md)

