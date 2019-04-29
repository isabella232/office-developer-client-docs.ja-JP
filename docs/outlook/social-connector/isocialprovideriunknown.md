---
title: iこの alprovider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Outlook Social Connector (.osc) プロバイダーのインスタンスを表します。
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409959"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="50f37-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50f37-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="50f37-104">Outlook Social Connector (.osc) プロバイダーのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="50f37-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="50f37-105">メンバー</span><span class="sxs-lookup"><span data-stu-id="50f37-105">Members</span></span>

<span data-ttu-id="50f37-106">次の表に、 **iare alprovider**インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="50f37-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="50f37-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="50f37-107">**Name**</span></span>|<span data-ttu-id="50f37-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="50f37-108">**Member type**</span></span>|<span data-ttu-id="50f37-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="50f37-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50f37-110">defaultsiteurls</span><span class="sxs-lookup"><span data-stu-id="50f37-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="50f37-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50f37-111">Property</span></span>  <br/> |<span data-ttu-id="50f37-112">.osc プロバイダーのサイト url を指定する文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="50f37-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="50f37-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="50f37-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="50f37-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f37-114">Method</span></span>  <br/> |<span data-ttu-id="50f37-115">自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50f37-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="50f37-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="50f37-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="50f37-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f37-117">Method</span></span>  <br/> |<span data-ttu-id="50f37-118">プロバイダー機能について説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="50f37-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="50f37-119">getsession</span><span class="sxs-lookup"><span data-stu-id="50f37-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="50f37-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f37-120">Method</span></span>  <br/> |<span data-ttu-id="50f37-121">i式[alsession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50f37-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="50f37-122">getstatussettings</span><span class="sxs-lookup"><span data-stu-id="50f37-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="50f37-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f37-123">Method</span></span>  <br/> |<span data-ttu-id="50f37-124">このメソッドは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="50f37-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="50f37-125">Load</span><span class="sxs-lookup"><span data-stu-id="50f37-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="50f37-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="50f37-126">Method</span></span>  <br/> |<span data-ttu-id="50f37-127">.osc プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50f37-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="50f37-128">"/ネットワーク guid"</span><span class="sxs-lookup"><span data-stu-id="50f37-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="50f37-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50f37-129">Property</span></span>  <br/> |<span data-ttu-id="50f37-130">ソーシャルネットワークの一意の識別子を表す GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="50f37-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|<span data-ttu-id="50f37-131">["/ネットワーク] アイコン](isocialprovider-socialnetworkicon.md)</span><span class="sxs-lookup"><span data-stu-id="50f37-131">[SocialNetworkIcon](isocialprovider-socialnetworkicon.md)</span></span> <br/> |<span data-ttu-id="50f37-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50f37-132">Property</span></span>  <br/> |<span data-ttu-id="50f37-133">ソーシャルネットワークのアイコンを表すバイト配列を返します。</span><span class="sxs-lookup"><span data-stu-id="50f37-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="50f37-134">指定した仮のネットワーク名</span><span class="sxs-lookup"><span data-stu-id="50f37-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="50f37-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50f37-135">Property</span></span>  <br/> |<span data-ttu-id="50f37-136">ソーシャルネットワーク名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50f37-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="50f37-137">バージョン</span><span class="sxs-lookup"><span data-stu-id="50f37-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="50f37-138">プロパティ</span><span class="sxs-lookup"><span data-stu-id="50f37-138">Property</span></span>  <br/> |<span data-ttu-id="50f37-139">このソーシャルネットワークのプロバイダーのバージョン番号を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50f37-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50f37-140">注釈</span><span class="sxs-lookup"><span data-stu-id="50f37-140">Remarks</span></span>

<span data-ttu-id="50f37-141">.osc プロバイダーは、このインターフェイスを実装して、.osc と通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50f37-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50f37-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="50f37-142">See also</span></span>

- [<span data-ttu-id="50f37-143">Outlook Social Connector プロバイダーインターフェイス</span><span class="sxs-lookup"><span data-stu-id="50f37-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

