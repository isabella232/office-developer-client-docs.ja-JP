---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: personsAddresses パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404534"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="42e08-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="42e08-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="42e08-104">_personsAddresses_ パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="42e08-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="42e08-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="42e08-105">Parameters</span></span>

<span data-ttu-id="42e08-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="42e08-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="42e08-107">[in]一連のユーザーのハッシュ化された SMTP アドレスを指定する XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="42e08-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="42e08-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="42e08-108">_personsCollection_</span></span>
  
> <span data-ttu-id="42e08-109">[out]人物と画像の詳細のコレクションを含む XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="42e08-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42e08-110">注釈</span><span class="sxs-lookup"><span data-stu-id="42e08-110">Remarks</span></span>

<span data-ttu-id="42e08-111">OUTLOOK Social Connector (OSC) は、OSC プロバイダーがフレンドとフレンド以外のオンデマンドまたはハイブリッド同期をサポートしている場合に **GetPeopleDetails** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="42e08-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="42e08-112">_personsAddresses パラメーター_ は、OSC プロバイダーの拡張性のスキーマで定義されている **hashedAddresses** のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="42e08-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="42e08-113">_personsAddresses 文字列_ は、People Pane に表示される各ユーザーのハッシュ化された SMTP アドレスのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="42e08-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="42e08-114">ユーザーは [、ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) プロパティで表されるログオン ユーザーのフレンドである必要があります。</span><span class="sxs-lookup"><span data-stu-id="42e08-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="42e08-115">ハッシュされた SMTP アドレスは、プロバイダーの機能 XML の **hashFunction** 要素で指定されたハッシュ関数を **使用して暗号化** されます。</span><span class="sxs-lookup"><span data-stu-id="42e08-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="42e08-116">OSC は **、personAddresses** コレクション内の各ハッシュされた  _Addressを index_ 要素で **識別** します。</span><span class="sxs-lookup"><span data-stu-id="42e08-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="42e08-117">プロバイダーは **、GetPeopleDetails** のフレンド **XML** を返す際に、index 要素を使用して受信者 **の個人** XML を識別する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="42e08-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="42e08-118">受信者がソーシャル ネットワーク上の登録ユーザーではない場合、プロバイダーは、その受信者 **の任意の** ユーザー XML を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="42e08-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="42e08-119">ユーザー **XML で** 表される各ネットワークユーザーの index 要素は _、personsAddresses_ の受信者の **index** 要素に対応します。</span><span class="sxs-lookup"><span data-stu-id="42e08-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="42e08-120">OSC は  _、personsCollection_ パラメーターによって返される情報をメモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="42e08-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="42e08-121">_personsCollection_ XML 文字列は、OSC プロバイダーの拡張性のスキーマで定義されているフレンドのスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="42e08-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="42e08-122">OSC がメモリ内でこの情報を使用して更新する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="42e08-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42e08-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="42e08-123">See also</span></span>

- [<span data-ttu-id="42e08-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42e08-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="42e08-125">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="42e08-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

