---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: hashedAddresses パラメーターによって指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336450"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="f78c5-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="f78c5-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="f78c5-104">_hashedAddresses_パラメーターによって指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="f78c5-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="f78c5-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f78c5-105">Parameters</span></span>

<span data-ttu-id="f78c5-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="f78c5-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="f78c5-107">順番一連のユーザーのハッシュ化された SMTP アドレスの配列を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="f78c5-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="f78c5-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="f78c5-108">_startTime_</span></span>
  
> <span data-ttu-id="f78c5-109">順番作成されたアクティビティが返されるまでの時間。</span><span class="sxs-lookup"><span data-stu-id="f78c5-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="f78c5-110">_アクティビティ_</span><span class="sxs-lookup"><span data-stu-id="f78c5-110">_activities_</span></span>
  
> <span data-ttu-id="f78c5-111">読み上げ_startTime_以降にソーシャルネットワーク上の_hashedAddresses_によって指定されたユーザーのアクティビティのセットを表す XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="f78c5-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f78c5-112">解説</span><span class="sxs-lookup"><span data-stu-id="f78c5-112">Remarks</span></span>

<span data-ttu-id="f78c5-113">.osc プロバイダーがアクティビティのオンデマンド同期をサポートしている場合、.osc 呼び出しは**GetActivitiesEx**です。</span><span class="sxs-lookup"><span data-stu-id="f78c5-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="f78c5-114">.osc は、_アクティビティ_で返された情報をメモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="f78c5-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="f78c5-115">.osc がメモリでこの情報を使用して更新する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f78c5-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="f78c5-116">Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートし、 **GetActivitiesEx**のみを呼び出してアクティビティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f78c5-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="f78c5-117">オンデマンドアクティビティ検索をサポートするには、 **cacheactivities**を**false**に、 **getactivities**と**dynamicActivitiesLookupEx**を**true**として設定し、.osc は**GetActivitiesEx**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f78c5-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="f78c5-118">返される XML 文字列は、プロバイダ拡張機能のスキーマで定義されているように、 **activityfeed**のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78c5-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="f78c5-119">_hashedAddresses_ sring は、People ウィンドウに表示される各ユーザーの一連のハッシュアドレスを表します。</span><span class="sxs-lookup"><span data-stu-id="f78c5-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="f78c5-120">ハッシュされた SMTP アドレスは、プロバイダーの**機能**XML の**hashfunction**要素によって指定されたハッシュ関数を使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="f78c5-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="f78c5-121">ユーザーは、 [iLoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオンユーザーのフレンドである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f78c5-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="f78c5-122">_startTime_パラメーターは、世界協定時刻 (UTC) の**日付**値です。</span><span class="sxs-lookup"><span data-stu-id="f78c5-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f78c5-123">現地時刻の値を UTC**日付**の値に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78c5-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="f78c5-124">**GetActivitiesEx**メソッドが返すアクティビティは、**開始**時刻の値が_startTime_よりも大きく、またはそれより小さいか等しい必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78c5-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="f78c5-125">**startTime**間で変更が行われて\*\*\*\* いない場合、プロバイダーは OSC_E_NO_CHANGES エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f78c5-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f78c5-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f78c5-126">See also</span></span>

- [<span data-ttu-id="f78c5-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f78c5-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="f78c5-128">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="f78c5-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

