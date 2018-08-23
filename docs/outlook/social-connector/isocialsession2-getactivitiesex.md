---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: HashedAddresses パラメーターで指定されたユーザーのそれぞれの活動のコレクションを表す文字列を取得します。
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804375"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="a0fb7-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="a0fb7-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="a0fb7-104">_HashedAddresses_パラメーターで指定されたユーザーのそれぞれの活動のコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="a0fb7-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0fb7-105">Parameters</span></span>

<span data-ttu-id="a0fb7-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="a0fb7-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="a0fb7-107">[in]ハッシュされた SMTP の配列を指定する構造体は、一連のユーザーに対応します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="a0fb7-108">_開始時刻_</span><span class="sxs-lookup"><span data-stu-id="a0fb7-108">_startTime_</span></span>
  
> <span data-ttu-id="a0fb7-109">[in]作成された活動項目が返されますになる時間です。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="a0fb7-110">_アクティビティ_</span><span class="sxs-lookup"><span data-stu-id="a0fb7-110">_activities_</span></span>
  
> <span data-ttu-id="a0fb7-111">[out]_開始時刻_以降に、ソーシャル ネットワーク上の_hashedAddresses_で指定されたユーザーのアクティビティのセットを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0fb7-112">注釈</span><span class="sxs-lookup"><span data-stu-id="a0fb7-112">Remarks</span></span>

<span data-ttu-id="a0fb7-113">OSC は、OSC プロバイダーには、活動のオン ・ デマンドの同期がサポートされている場合に**GetActivitiesEx**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="a0fb7-114">OSC では、メモリ内_のアクティビティ_に返される情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="a0fb7-115">OSC を使用してメモリ内には、この情報を更新する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="a0fb7-116">Outlook ソーシャル コネクタ 2013 で開始、OSC はだけオンデマンド同期アクティビティをサポートし、活動を取得するのには**GetActivitiesEx**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="a0fb7-117">オンデマンド アクティビティの参照をサポートするには、 **false**、および**getActivities**と**真**の**dynamicActivitiesLookupEx**と、OSC に**GetActivitiesEx**を呼び出すと**cacheActivities**を設定します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="a0fb7-118">返される XML 文字列は、OSC プロバイダーの拡張機能のスキーマで定義されている**activityFeed**のスキーマ定義に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="a0fb7-119">_HashedAddresses_ sring では、人物情報ウィンドウに表示される各ユーザーのハッシュ化されたアドレスのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="a0fb7-120">ハッシュの SMTP アドレスは、プロバイダーの**機能**XML で**実装しています。** 要素で指定するハッシュ関数を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="a0fb7-121">ユーザーは、 [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオン中のユーザーのフレンドではありません。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="a0fb7-122">_開始時刻_パラメーターは、世界協定時刻 (UTC) で**日付**値です。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a0fb7-123">現地時刻の値は、UTC**の日付**値に変換しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="a0fb7-124">**GetActivitiesEx**メソッドが返すアクティビティの作成時刻の値、_開始時刻_よりも大きい必要があり、**今すぐ**に小さい。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="a0fb7-125">**開始時刻**と**現在**の間で変更が発生していない、プロバイダーは、OSC_E_NO_CHANGES エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0fb7-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0fb7-126">See also</span></span>

- [<span data-ttu-id="a0fb7-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0fb7-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="a0fb7-128">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="a0fb7-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

