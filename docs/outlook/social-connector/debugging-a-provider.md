---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Outlook Social Connector (OSC) プロバイダーをデバッグするには、いくつかの方法があります。
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281070"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="f6fcf-103">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="f6fcf-103">Debugging a provider</span></span>

<span data-ttu-id="f6fcf-104">Outlook Social Connector (OSC) プロバイダーをデバッグするには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="f6fcf-105">Outlook の Office Fluent ユーザー インターフェイスのリボン コンポーネントまたはサポートされている Office クライアント アプリケーションのリボン コンポーネントでデバッグ コマンドを使用して、OSC がさまざまなアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="f6fcf-106">Fiddler を使用してソーシャル ネットワークとその OSC プロバイダー間で送信される API 呼び出しと XML を追跡する</span><span class="sxs-lookup"><span data-stu-id="f6fcf-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="f6fcf-107">デバッグ ボタン</span><span class="sxs-lookup"><span data-stu-id="f6fcf-107">Debug buttons</span></span>

<span data-ttu-id="f6fcf-108">OSC プロバイダーの機能拡張により、OSC プロバイダーをデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="f6fcf-109">プロバイダーをデバッグするには、キーの下の Windows レジストリに DWORD 型の値を作成し (次の行に示すように)、値を  `DebugProviders`  `SocialConnector`  `DebugProviders` 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="f6fcf-110">既定では、プロバイダーのデバッグはオフです。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-110">By default, provider debugging is off.</span></span> <span data-ttu-id="f6fcf-111">値が存在しない場合、または値が存在し、値 0 に設定されている場合、プロバイダー  `DebugProviders` のデバッグは無効になります。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="f6fcf-112">プロバイダーのデバッグが有効になっている場合、エラーが発生した場合、OSC は詳細なエラー情報を含む警告ダイアログ ボックスを表示し、OSC プロバイダー XML スキーマに対して OSC プロバイダー XML を検証します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="f6fcf-113">XML 文字列に指定された名前空間に基づいて、OSC 1.0 を使用して開発された OSC プロバイダーは、OSC 1.0 スキーマ ファイル OutlookSocialProvider.xsd に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="f6fcf-114">OSC 1.1 以降を使用して開発された OSC プロバイダーは、スキーマ ファイル OutlookSocialProvider_1.1.xsd に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="f6fcf-115">この値を使用すると、特定のプロバイダーではなく、読み込まれたすべてのプロバイダーに対してデバッグ  `DebugProviders` アラートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="f6fcf-116">プロバイダーのデバッグに役立つデバッグ ボタンを表示するには、キーの下の Windows レジストリに DWORD 型の値を作成し、値を  `ShowDebugButtons`  `SocialConnector`  `ShowDebugButtons` 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="f6fcf-117">デバッグ コマンド バー ボタンを非表示にする場合は、値  `ShowDebugButtons` を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="f6fcf-118">Outlook 2010 および Office 2013以降のクライアント アプリケーションでは、エクスプローラー リボンの [アドイン] タブにデバッグ ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="f6fcf-119">Outlook 2007 および Outlook 2003 では、Outlook エクスプローラー ウィンドウの標準コマンド バーにデバッグ ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="f6fcf-120">次の表に、デバッグ ボタンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="f6fcf-121">**[デバッグ] ボタン**</span><span class="sxs-lookup"><span data-stu-id="f6fcf-121">**Debug button**</span></span>|<span data-ttu-id="f6fcf-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6fcf-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6fcf-123">連絡先の同期</span><span class="sxs-lookup"><span data-stu-id="f6fcf-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="f6fcf-124">OSC がキャッシュされた連絡先のみを OSC プロバイダーに求める原因です。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="f6fcf-125">GAL 同期</span><span class="sxs-lookup"><span data-stu-id="f6fcf-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="f6fcf-126">OSC が Exchange グローバル アドレス一覧から Outlook 連絡先にデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="f6fcf-127">カテゴリ キャッシュの無効化</span><span class="sxs-lookup"><span data-stu-id="f6fcf-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="f6fcf-128">アクティビティ フィードの更新時に、OSC が各ストアのカテゴリ リストを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="f6fcf-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="f6fcf-129">Fiddler</span></span>

<span data-ttu-id="f6fcf-130">Fiddler は、プロバイダーからソーシャル ネットワークに送信される API 呼び出し、およびソーシャル ネットワークからプロバイダーに送信される XML を確認する、ネットワーク上のデバッグ ツールです。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="f6fcf-131">Fiddler は [Fiddler Web デバッグ プロキシでダウンロードできます](https://www.fiddler2.com/fiddler2/version.asp)。</span><span class="sxs-lookup"><span data-stu-id="f6fcf-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6fcf-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6fcf-132">See also</span></span>

- [<span data-ttu-id="f6fcf-133">プロバイダーを開発するための学習のクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="f6fcf-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="f6fcf-134">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="f6fcf-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="f6fcf-135">プロバイダーの開発に関するベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f6fcf-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="f6fcf-136">OSC の一般的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="f6fcf-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="f6fcf-137">OSC XML スキーマを使用したプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="f6fcf-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="f6fcf-138">OSC プロバイダーをリリースする準備</span><span class="sxs-lookup"><span data-stu-id="f6fcf-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

