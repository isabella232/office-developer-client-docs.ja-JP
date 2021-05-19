---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409959"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="530a0-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="530a0-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="530a0-104">ソーシャル コネクタ (OSC) Outlookのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="530a0-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="530a0-105">Members</span><span class="sxs-lookup"><span data-stu-id="530a0-105">Members</span></span>

<span data-ttu-id="530a0-106">次の表に **、ISocialProvider** インターフェイスで使用できるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="530a0-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="530a0-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="530a0-107">**Name**</span></span>|<span data-ttu-id="530a0-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="530a0-108">**Member type**</span></span>|<span data-ttu-id="530a0-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="530a0-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="530a0-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="530a0-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="530a0-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="530a0-111">Property</span></span>  <br/> |<span data-ttu-id="530a0-112">OSC プロバイダーのサイト URL を指定する文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="530a0-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="530a0-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="530a0-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="530a0-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="530a0-114">Method</span></span>  <br/> |<span data-ttu-id="530a0-115">自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="530a0-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="530a0-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="530a0-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="530a0-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="530a0-117">Method</span></span>  <br/> |<span data-ttu-id="530a0-118">プロバイダーの機能を説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="530a0-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="530a0-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="530a0-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="530a0-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="530a0-120">Method</span></span>  <br/> |<span data-ttu-id="530a0-121">[ISocialSession インターフェイスを取得](isocialsessioniunknown.md)します。</span><span class="sxs-lookup"><span data-stu-id="530a0-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="530a0-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="530a0-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="530a0-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="530a0-123">Method</span></span>  <br/> |<span data-ttu-id="530a0-124">このメソッドは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="530a0-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="530a0-125">Load</span><span class="sxs-lookup"><span data-stu-id="530a0-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="530a0-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="530a0-126">Method</span></span>  <br/> |<span data-ttu-id="530a0-127">OSC プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="530a0-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="530a0-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="530a0-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="530a0-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="530a0-129">Property</span></span>  <br/> |<span data-ttu-id="530a0-130">ソーシャル ネットワークの一意の識別子を表す GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="530a0-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="530a0-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="530a0-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="530a0-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="530a0-132">Property</span></span>  <br/> |<span data-ttu-id="530a0-133">ソーシャル ネットワークのアイコンを表すバイトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="530a0-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="530a0-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="530a0-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="530a0-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="530a0-135">Property</span></span>  <br/> |<span data-ttu-id="530a0-136">ソーシャル ネットワーク名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="530a0-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="530a0-137">バージョン</span><span class="sxs-lookup"><span data-stu-id="530a0-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="530a0-138">プロパティ</span><span class="sxs-lookup"><span data-stu-id="530a0-138">Property</span></span>  <br/> |<span data-ttu-id="530a0-139">このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="530a0-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="530a0-140">注釈</span><span class="sxs-lookup"><span data-stu-id="530a0-140">Remarks</span></span>

<span data-ttu-id="530a0-141">OSC プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="530a0-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="530a0-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="530a0-142">See also</span></span>

- [<span data-ttu-id="530a0-143">Outlookソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="530a0-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

