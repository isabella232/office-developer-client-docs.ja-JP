---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Outlook Social Connector (.osc) プロバイダーをデバッグするには、いくつかの方法があります。
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281070"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="ddf52-103">プロバイダーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="ddf52-103">Debugging a provider</span></span>

<span data-ttu-id="ddf52-104">Outlook Social Connector (.osc) プロバイダーをデバッグするには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="ddf52-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="ddf52-105">Outlook の office Fluent ユーザーインターフェイスのリボンコンポーネントにあるデバッグコマンドを使用するか、office クライアントアプリケーションをサポートして、.osc にさまざまなアクションを実行させることができます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="ddf52-106">Fiddler を使用して、ソーシャルネットワークと .osc プロバイダーとの間で送信される API 呼び出しと XML をトレースする</span><span class="sxs-lookup"><span data-stu-id="ddf52-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="ddf52-107">デバッグボタン</span><span class="sxs-lookup"><span data-stu-id="ddf52-107">Debug buttons</span></span>

<span data-ttu-id="ddf52-108">.osc プロバイダー拡張機能は、.osc プロバイダーをデバッグする機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="ddf52-109">プロバイダーをデバッグするには、 `DebugProviders` Windows レジストリの`SocialConnector`キーの下にある (次の行に示すように) DWORD 型の値を作成`DebugProviders`し、値を1に設定します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="ddf52-110">既定では、プロバイダーデバッグはオフになっています。</span><span class="sxs-lookup"><span data-stu-id="ddf52-110">By default, provider debugging is off.</span></span> <span data-ttu-id="ddf52-111">`DebugProviders`値が存在しない場合、または存在し、値が0に設定されている場合は、プロバイダーデバッグがオフになります。</span><span class="sxs-lookup"><span data-stu-id="ddf52-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="ddf52-112">プロバイダーデバッグが有効になっている場合は、エラーが発生したときに詳細なエラー情報を含む警告ダイアログボックスが表示され、.osc プロバイダーの xml スキーマに対して、.osc プロバイダ xml を検証します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="ddf52-113">XML 文字列に対して指定された名前空間に基づいて、.osc 1.0 を使用して開発された .osc プロバイダーが、.osc 1.0 スキーマファイル、outlookの形式に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="ddf52-114">.osc 1.1 以降を使用して開発した .osc プロバイダーは、スキーマファイル outlooksocialprovider_ 1.1 に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="ddf52-115">`DebugProviders`値を使用すると、特定のプロバイダーではなく、読み込まれたすべてのプロバイダーのデバッグ警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="ddf52-116">プロバイダーをデバッグするのに役立つデバッグボタンを表示するには`ShowDebugButtons` 、 `SocialConnector`キーの下の Windows レジストリに DWORD 型の値を作成し`ShowDebugButtons` 、値を1に設定します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="ddf52-117">デバッグコマンドバーボタンを非表示にするに`ShowDebugButtons`は、値を0に設定します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="ddf52-118">Office 2013 以降の Outlook 2010 およびクライアントアプリケーションの場合、[デバッグ] ボタンはエクスプローラーリボンの [**アドイン**] タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="ddf52-119">outlook 2007 および outlook 2003 の場合、[デバッグ] ボタンは、outlook エクスプローラーウィンドウの標準のコマンドバーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="ddf52-120">次の表で、デバッグボタンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="ddf52-121">**[デバッグ] ボタン**</span><span class="sxs-lookup"><span data-stu-id="ddf52-121">**Debug button**</span></span>|<span data-ttu-id="ddf52-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="ddf52-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddf52-123">連絡先を同期する</span><span class="sxs-lookup"><span data-stu-id="ddf52-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="ddf52-124">.osc は、キャッシュされた連絡先のみを、.osc プロバイダーに要求します。</span><span class="sxs-lookup"><span data-stu-id="ddf52-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="ddf52-125">GAL 同期</span><span class="sxs-lookup"><span data-stu-id="ddf52-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="ddf52-126">.osc が Exchange のグローバルアドレス一覧から Outlook の連絡先にデータを設定するようにします。</span><span class="sxs-lookup"><span data-stu-id="ddf52-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="ddf52-127">カテゴリキャッシュを無効にする</span><span class="sxs-lookup"><span data-stu-id="ddf52-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="ddf52-128">アクティビティフィードが更新されたときに、.osc が各ストアのカテゴリリストを再読み込みするようにします。</span><span class="sxs-lookup"><span data-stu-id="ddf52-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="ddf52-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="ddf52-129">Fiddler</span></span>

<span data-ttu-id="ddf52-130">Fiddler は、プロバイダーからソーシャルネットワークに送信された API 呼び出しと、ソーシャルネットワークによってプロバイダーに送信される XML をチェックする、ネットワーク上のデバッグツールです。</span><span class="sxs-lookup"><span data-stu-id="ddf52-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="ddf52-131">Fiddler は、 [Fiddler Web デバッグプロキシ](https://www.fiddler2.com/fiddler2/version.asp)でダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="ddf52-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ddf52-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddf52-132">See also</span></span>

- [<span data-ttu-id="ddf52-133">プロバイダーを開発するための簡単な手順</span><span class="sxs-lookup"><span data-stu-id="ddf52-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="ddf52-134">フレンドとアクティビティの同期</span><span class="sxs-lookup"><span data-stu-id="ddf52-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="ddf52-135">プロバイダーを開発するためのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="ddf52-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="ddf52-136">通常の呼び出しシーケンスの .osc</span><span class="sxs-lookup"><span data-stu-id="ddf52-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="ddf52-137">.osc XML スキーマを使用してプロバイダーを開発する</span><span class="sxs-lookup"><span data-stu-id="ddf52-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="ddf52-138">.osc プロバイダーをリリースする準備をする</span><span class="sxs-lookup"><span data-stu-id="ddf52-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

