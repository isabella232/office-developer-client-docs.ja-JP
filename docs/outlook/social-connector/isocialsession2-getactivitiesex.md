---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: hashedAddresses パラメーターで指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404338"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="3162b-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="3162b-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="3162b-104">_hashedAddresses_ パラメーターで指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="3162b-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="3162b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3162b-105">Parameters</span></span>

<span data-ttu-id="3162b-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="3162b-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="3162b-107">[in]一連のユーザーのハッシュ化された SMTP アドレスの配列を指定する構造体。</span><span class="sxs-lookup"><span data-stu-id="3162b-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="3162b-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="3162b-108">_startTime_</span></span>
  
> <span data-ttu-id="3162b-109">[in]作成されたアクティビティが返される時間。</span><span class="sxs-lookup"><span data-stu-id="3162b-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="3162b-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="3162b-110">_activities_</span></span>
  
> <span data-ttu-id="3162b-111">[out]_startTime_ 以降のソーシャル ネットワーク上の _hashedAddresses_ で指定されたユーザーのアクティビティのセットを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="3162b-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3162b-112">注釈</span><span class="sxs-lookup"><span data-stu-id="3162b-112">Remarks</span></span>

<span data-ttu-id="3162b-113">OSC プロバイダーがアクティビティのオンデマンド同期をサポートしている場合、OSC は **GetActivitiesEx** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3162b-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="3162b-114">OSC は、アクティビティに返される情報を  _メモリに_ 格納します。</span><span class="sxs-lookup"><span data-stu-id="3162b-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="3162b-115">OSC がメモリ内でこの情報を使用して更新する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="3162b-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="3162b-116">Outlook Social Connector 2013 から、OSC はアクティビティのオンデマンド同期のみをサポートし、アクティビティを取得するために **GetActivitiesEx** のみを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3162b-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="3162b-117">オンデマンド アクティビティの参照をサポートするには **、cacheActivities** **を** false に設定し **、getActivities および dynamicActivitiesLookupEx** を **true** に設定し、OSC は **GetActivitiesEx** を呼び出します。 </span><span class="sxs-lookup"><span data-stu-id="3162b-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="3162b-118">返される XML 文字列は、OSC プロバイダーの機能拡張のスキーマで定義されている **activityFeed** のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3162b-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="3162b-119">_hashedAddresses sring_ は、People Pane に表示される各ユーザーのハッシュされたアドレスのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="3162b-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="3162b-120">ハッシュされた SMTP アドレスは、プロバイダーの機能 XML の **hashFunction** 要素で指定されたハッシュ関数を **使用して暗号化** されます。</span><span class="sxs-lookup"><span data-stu-id="3162b-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="3162b-121">ユーザーは [、ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) プロパティで表されるログオン ユーザーのフレンドである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3162b-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="3162b-122">_startTime パラメーター_ は、**協定世界時**(UTC) の Date 値です。</span><span class="sxs-lookup"><span data-stu-id="3162b-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3162b-123">現地時間の値は UTC 日付値に **変換する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="3162b-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="3162b-124">**GetActivitiesEx** メソッドが返すアクティビティには _、startTime_ より大きく、Now 以下の作成時間値が必要 **です**。</span><span class="sxs-lookup"><span data-stu-id="3162b-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="3162b-125">**startTime** と Now の間に変更が発生した **場合、プロバイダー** はエラーメッセージをOSC_E_NO_CHANGESがあります。</span><span class="sxs-lookup"><span data-stu-id="3162b-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3162b-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="3162b-126">See also</span></span>

- [<span data-ttu-id="3162b-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3162b-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="3162b-128">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="3162b-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

