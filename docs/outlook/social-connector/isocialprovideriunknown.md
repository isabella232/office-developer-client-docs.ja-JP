---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Outlook ソーシャル コネクタ (OSC) プロバイダーのインスタンスを表します。
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804479"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="5b748-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b748-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="5b748-104">Outlook ソーシャル コネクタ (OSC) プロバイダーのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="5b748-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="5b748-105">Members</span><span class="sxs-lookup"><span data-stu-id="5b748-105">Members</span></span>

<span data-ttu-id="5b748-106">次の表は、 **ISocialProvider**インターフェイスで使用可能なメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="5b748-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="5b748-107">**名前**</span><span class="sxs-lookup"><span data-stu-id="5b748-107">**Name**</span></span>|<span data-ttu-id="5b748-108">**メンバーの種類**</span><span class="sxs-lookup"><span data-stu-id="5b748-108">**Member type**</span></span>|<span data-ttu-id="5b748-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b748-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5b748-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="5b748-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="5b748-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b748-111">Property</span></span>  <br/> |<span data-ttu-id="5b748-112">OSC プロバイダーのサイトの Url を指定する文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b748-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="5b748-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="5b748-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="5b748-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b748-114">Method</span></span>  <br/> |<span data-ttu-id="5b748-115">自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5b748-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="5b748-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="5b748-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="5b748-117">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b748-117">Method</span></span>  <br/> |<span data-ttu-id="5b748-118">プロバイダーの機能を説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="5b748-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="5b748-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="5b748-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="5b748-120">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b748-120">Method</span></span>  <br/> |<span data-ttu-id="5b748-121">[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5b748-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="5b748-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="5b748-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="5b748-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b748-123">Method</span></span>  <br/> |<span data-ttu-id="5b748-124">このメソッドは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5b748-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="5b748-125">Load</span><span class="sxs-lookup"><span data-stu-id="5b748-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="5b748-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b748-126">Method</span></span>  <br/> |<span data-ttu-id="5b748-127">OSC プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5b748-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="5b748-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="5b748-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="5b748-129">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b748-129">Property</span></span>  <br/> |<span data-ttu-id="5b748-130">ソーシャル ネットワークの一意の識別子を表す GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="5b748-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="5b748-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="5b748-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="5b748-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b748-132">Property</span></span>  <br/> |<span data-ttu-id="5b748-133">ソーシャル ネットワークのアイコンを表すバイトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b748-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="5b748-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="5b748-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="5b748-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b748-135">Property</span></span>  <br/> |<span data-ttu-id="5b748-136">ソーシャル ネットワーク名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b748-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="5b748-137">バージョン</span><span class="sxs-lookup"><span data-stu-id="5b748-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="5b748-138">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5b748-138">Property</span></span>  <br/> |<span data-ttu-id="5b748-139">このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b748-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b748-140">注釈</span><span class="sxs-lookup"><span data-stu-id="5b748-140">Remarks</span></span>

<span data-ttu-id="5b748-141">OSC プロバイダーでは、OSC と通信するには、このインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b748-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b748-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b748-142">See also</span></span>

- [<span data-ttu-id="5b748-143">Outlook ソーシャル コネクタ プロバイダー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="5b748-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

