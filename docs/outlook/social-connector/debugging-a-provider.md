---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Outlook ソーシャル コネクタ (OSC) プロバイダーをデバッグするいくつかの方法があります。
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386853"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="ae734-103">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="ae734-103">Debugging a provider</span></span>

<span data-ttu-id="ae734-104">Outlook ソーシャル コネクタ (OSC) プロバイダーをデバッグするいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="ae734-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="ae734-105">さまざまなアクションを実行するのには OSC が発生する Outlook またはサポートしている Office クライアント アプリケーションに Office Fluent ユーザー インターフェイスのリボン コンポーネントのデバッグ コマンドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="ae734-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="ae734-106">トレース API 呼び出しとソーシャル ネットワークと OSC プロバイダーの間で送信される XML に Fiddler を使用して、</span><span class="sxs-lookup"><span data-stu-id="ae734-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="ae734-107">デバッグ ボタン</span><span class="sxs-lookup"><span data-stu-id="ae734-107">Debug buttons</span></span>

<span data-ttu-id="ae734-108">OSC プロバイダーの拡張機能は、デバッグ、OSC プロバイダーの機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ae734-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="ae734-109">プロバイダーをデバッグするには、作成、`DebugProviders`の下の Windows レジストリに DWORD 型の値、 `SocialConnector` (のように、次の行)、キーし、設定、`DebugProviders`値を 1。</span><span class="sxs-lookup"><span data-stu-id="ae734-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="ae734-110">既定では、プロバイダーのデバッグはオフです。</span><span class="sxs-lookup"><span data-stu-id="ae734-110">By default, provider debugging is off.</span></span> <span data-ttu-id="ae734-111">場合、`DebugProviders`の値が存在しないか、存在していて値が 0 では、プロバイダーのデバッグの設定がオフになっています。</span><span class="sxs-lookup"><span data-stu-id="ae734-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="ae734-112">プロバイダーのデバッグを有効にする場合、OSC は、エラーが発生し、OSC プロバイダーの XML スキーマに対しては、OSC プロバイダーの XML を検証するときに詳細なエラー情報を使用して警告ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ae734-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="ae734-113">OSC 1.0 を使用して開発された、OSC プロバイダーは XML 文字列に指定した名前空間に基づいて、OSC 1.0 スキーマ ファイルで、OutlookSocialProvider.xsd に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="ae734-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="ae734-114">OSC プロバイダーは、OSC 1.1 を使用して開発されたまたは後で、スキーマ ファイル、OutlookSocialProvider_1.1.xsd に対して検証します。</span><span class="sxs-lookup"><span data-stu-id="ae734-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="ae734-115">使用する場合、`DebugProviders`の値を特定のプロバイダーではなくプロバイダーが読み込まれているすべてのデバッグの警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae734-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="ae734-116">プロバイダーをデバッグするために役立つデバッグ ボタンを表示するには、次のように作成します。、`ShowDebugButtons`の下の Windows レジストリに DWORD 型の値、`SocialConnector`キー、および設定、 `ShowDebugButtons` 1 の値です。</span><span class="sxs-lookup"><span data-stu-id="ae734-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="ae734-117">デバッグのコマンド バー ボタンを非表示に設定、`ShowDebugButtons`値を 0 にします。</span><span class="sxs-lookup"><span data-stu-id="ae734-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="ae734-118">Outlook 2010 と Office 2013 以降のクライアント アプリケーションでは、エクスプ ローラーのリボンの **[アドイン**] タブで、デバッグ ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae734-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="ae734-119">Outlook 2007 および Outlook 2003 の Outlook エクスプ ローラー ウィンドウの標準的なコマンド バーのデバッグ ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae734-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="ae734-120">次の表では、デバッグ ボタンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ae734-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="ae734-121">**デバッグ ボタン**</span><span class="sxs-lookup"><span data-stu-id="ae734-121">**Debug button**</span></span>|<span data-ttu-id="ae734-122">**関数**</span><span class="sxs-lookup"><span data-stu-id="ae734-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae734-123">連絡先を同期します。</span><span class="sxs-lookup"><span data-stu-id="ae734-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="ae734-124">キャッシュされた取引先担当者の OSC プロバイダーに確認するのには OSC が発生します。</span><span class="sxs-lookup"><span data-stu-id="ae734-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="ae734-125">グローバル アドレス一覧の同期</span><span class="sxs-lookup"><span data-stu-id="ae734-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="ae734-126">Exchange のグローバル アドレス一覧から Outlook の連絡先にデータを設定するのには OSC が発生します。</span><span class="sxs-lookup"><span data-stu-id="ae734-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="ae734-127">カテゴリのキャッシュを無効に</span><span class="sxs-lookup"><span data-stu-id="ae734-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="ae734-128">アクティビティ フィードが更新されたときに各店舗のカテゴリの一覧を再読み込みするのには OSC が発生します。</span><span class="sxs-lookup"><span data-stu-id="ae734-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="ae734-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="ae734-129">Fiddler</span></span>

<span data-ttu-id="ae734-130">Fiddler は、API の呼び出しは、プロバイダーから、ソーシャル ネットワークに送信されると、プロバイダー、ソーシャル ネットワークから送信された XML を確認するのには、ワイヤ上のデバッグ ツールです。</span><span class="sxs-lookup"><span data-stu-id="ae734-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="ae734-131">Fiddler では、 [Fiddler Web デバッグ プロキシ](https://www.fiddler2.com/fiddler2/version.asp)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="ae734-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae734-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae734-132">See also</span></span>

- [<span data-ttu-id="ae734-133">プロバイダーを開発する学習のためのクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="ae734-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="ae734-134">友人や活動を同期します。</span><span class="sxs-lookup"><span data-stu-id="ae734-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="ae734-135">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="ae734-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="ae734-136">OSC の典型的な呼び出しシーケンス</span><span class="sxs-lookup"><span data-stu-id="ae734-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="ae734-137">OSC の XML スキーマを使用してプロバイダーの開発</span><span class="sxs-lookup"><span data-stu-id="ae734-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="ae734-138">OSC プロバイダーをリリースする準備をします。</span><span class="sxs-lookup"><span data-stu-id="ae734-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

