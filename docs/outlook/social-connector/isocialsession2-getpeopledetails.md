---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返します。
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404534"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="a800f-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="a800f-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="a800f-104">ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返し__ ます。</span><span class="sxs-lookup"><span data-stu-id="a800f-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="a800f-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a800f-105">Parameters</span></span>

<span data-ttu-id="a800f-106">_個人住所_</span><span class="sxs-lookup"><span data-stu-id="a800f-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="a800f-107">順番一連のユーザーのハッシュ化された SMTP アドレスを指定する XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="a800f-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="a800f-108">_個人コレクション_</span><span class="sxs-lookup"><span data-stu-id="a800f-108">_personsCollection_</span></span>
  
> <span data-ttu-id="a800f-109">読み上げ個人および画像の詳細のコレクションを含む XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="a800f-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a800f-110">注釈</span><span class="sxs-lookup"><span data-stu-id="a800f-110">Remarks</span></span>

<span data-ttu-id="a800f-111">.osc プロバイダーが友人および友人以外の**GetPeopleDetails**またはハイブリッド同期をサポートしている場合、Outlook Social Connector (.osc) はを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a800f-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="a800f-112">_個人住所_パラメーターは、プロバイダ拡張機能のスキーマで定義されているように、 **hashedAddresses**のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a800f-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="a800f-113">_個人_情報の文字列は、[人] ウィンドウに表示される各ユーザーのハッシュされた SMTP アドレスのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="a800f-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="a800f-114">ユーザーは、 [iLoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオンユーザーのフレンドである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a800f-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="a800f-115">ハッシュされた SMTP アドレスは、プロバイダーの**機能**XML の**hashfunction**要素によって指定されたハッシュ関数を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="a800f-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="a800f-116">.osc は、**キーワード**要素を使用して、_個人住所_コレクション内の各**hashedAddress**を識別します。</span><span class="sxs-lookup"><span data-stu-id="a800f-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="a800f-117">プロバイダーは、 **GetPeopleDetails**の**フレンド**xml を返すときに、受信者の**person** xml を識別するために、 **index**要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a800f-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="a800f-118">受信者がソーシャルネットワーク上の登録済みユーザーではない場合、プロバイダーはその受信者の**個人**XML を返さないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a800f-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="a800f-119">**person** XML で表される各ネットワークユーザーの**index**要素は、個人_住所_の受信者の**index**要素に対応します。</span><span class="sxs-lookup"><span data-stu-id="a800f-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="a800f-120">.osc は、_個人コレクション_パラメーターによって返される情報をメモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="a800f-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="a800f-121">_個人コレクション_XML 文字列は、プロバイダ拡張機能のスキーマで定義されているように、**フレンド**のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="a800f-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="a800f-122">.osc がメモリでこの情報を使用して更新する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a800f-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a800f-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="a800f-123">See also</span></span>

- [<span data-ttu-id="a800f-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a800f-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="a800f-125">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="a800f-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

