---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: PersonsAddresses パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804377"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="7f4ce-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="7f4ce-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="7f4ce-104">_PersonsAddresses_パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="7f4ce-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="7f4ce-105">Parameters</span></span>

<span data-ttu-id="7f4ce-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="7f4ce-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="7f4ce-107">[in]ハッシュ化された一連のユーザーの SMTP アドレスを指定する XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="7f4ce-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="7f4ce-108">_personsCollection_</span></span>
  
> <span data-ttu-id="7f4ce-109">[out]人と画像の詳細のコレクションを格納する XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f4ce-110">備考</span><span class="sxs-lookup"><span data-stu-id="7f4ce-110">Remarks</span></span>

<span data-ttu-id="7f4ce-111">OSC プロバイダー以外の友人や友人のオン ・ デマンドまたはハイブリッドの同期をサポートしている場合、Outlook ソーシャル コネクタ (OSC) は**GetPeopleDetails**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="7f4ce-112">_PersonsAddresses_パラメーターは、OSC プロバイダーの拡張機能のスキーマで定義されている**hashedAddresses**のスキーマ定義に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="7f4ce-113">_PersonsAddresses_文字列は、人物情報ウィンドウに表示される各ユーザーの SMTP アドレスをハッシュのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="7f4ce-114">ユーザーは、 [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオン中のユーザーのフレンドではありません。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="7f4ce-115">ハッシュの SMTP アドレスは、プロバイダーの**機能**XML で**実装しています。** 要素で指定するハッシュ関数を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="7f4ce-116">OSC では、**インデックス**の要素を持つ_personAddresses_コレクション内の各**hashedAddress**を識別します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="7f4ce-117">プロバイダーは、 **GetPeopleDetails**の**友人**XML が返されるときに、XML の受信者の**ユーザー**を識別するのに**インデックス**の要素を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="7f4ce-118">受信者がソーシャル ネットワークに登録されているユーザーでない場合、プロバイダーはその受信者の**人**XML を返さなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="7f4ce-119">**人**XML で表されるネットワークのユーザーごとに**インデックス**の要素は、 _personsAddresses_内の受信者の**インデックス**の要素に対応しています。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="7f4ce-120">OSC では、メモリ内の_personsCollection_パラメーターによって返される情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="7f4ce-121">_PersonsCollection_ XML 文字列は、OSC プロバイダーの拡張機能のスキーマで定義されている、**友人**のスキーマ定義に従ってください。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="7f4ce-122">OSC を使用してメモリ内には、この情報を更新する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f4ce-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f4ce-123">See also</span></span>

- [<span data-ttu-id="7f4ce-124">ISocialSession2: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f4ce-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="7f4ce-125">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="7f4ce-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

