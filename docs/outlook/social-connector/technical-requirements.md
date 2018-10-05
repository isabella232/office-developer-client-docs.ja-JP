---
title: 技術的要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: ここでサポートされているプログラミング言語について説明、COM の可視性とメソッドが型の要件、および Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能 DLL の詳細を返します。
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383115"
---
# <a name="technical-requirements"></a><span data-ttu-id="65de5-103">技術的要件</span><span class="sxs-lookup"><span data-stu-id="65de5-103">Technical requirements</span></span>

<span data-ttu-id="65de5-104">ここでサポートされているプログラミング言語について説明、COM の可視性とメソッドが型の要件、および Outlook ソーシャル コネクタ (OSC) プロバイダーの拡張機能 DLL の詳細を返します。</span><span class="sxs-lookup"><span data-stu-id="65de5-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="65de5-105">プログラミング言語や COM の要件</span><span class="sxs-lookup"><span data-stu-id="65de5-105">Programming language and COM requirements</span></span>

<span data-ttu-id="65de5-106">Visual C# または Visual Basic では、マネージ言語または Visual C++ などのアンマネージ言語を使用して、OSC プロバイダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="65de5-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="65de5-107">OSC プロバイダーを開発するのには COM 参照可能 DLL コンポーネントを作成できる任意のツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="65de5-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="65de5-108">プロバイダーを開発するのにはマネージ コードまたはアンマネージ言語を使用するかは、アカウントのダウンロードのサイズとプロバイダーのインストール パッケージの依存関係になりません。</span><span class="sxs-lookup"><span data-stu-id="65de5-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="65de5-109">OSC プロバイダーは、次のように定義されている COM 参照可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de5-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="65de5-110">インストールが完了したら、COM 登録または regsvr32 を使用して、OSC プロバイダーを登録してください。</span><span class="sxs-lookup"><span data-stu-id="65de5-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="65de5-111">OSC プロバイダー DLL の COM 登録は、HKCU または HKLM の下のプロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="65de5-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="65de5-112">プロバイダーの ProgID が登録されている`HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。</span><span class="sxs-lookup"><span data-stu-id="65de5-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="65de5-113">マネージ言語で開発された、OSC プロバイダーは、COM 参照可能です。</span><span class="sxs-lookup"><span data-stu-id="65de5-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="65de5-114">OSC プロバイダーは、プロバイダーの DLL には、シングル スレッド アパートメント (STA) とマルチ スレッド アパートメント (MTA) スレッド モデルの両方がサポートしていることを示す Windows のレジストリに値を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de5-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="65de5-115">COM スレッド モデルの詳細については、[説明および動作の OLE のスレッド化モデル](https://support.microsoft.com/kb/150777)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65de5-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="65de5-116">OSC プロバイダーの拡張機能のメソッドは、**文字列**または**ブール値**などのプリミティブ型を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de5-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="65de5-117">特定の**文字列**では、OSC プロバイダーの拡張機能のスキーマ定義に従うものと値を返します。</span><span class="sxs-lookup"><span data-stu-id="65de5-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="65de5-118">戻り値として XML のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="65de5-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="65de5-119">OSC プロバイダーの拡張機能 DLL の詳細</span><span class="sxs-lookup"><span data-stu-id="65de5-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="65de5-120">OSC プロバイダーの拡張機能をサポートしているコンポーネントは、OSC プロバイダーの拡張機能 DLL です。</span><span class="sxs-lookup"><span data-stu-id="65de5-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="65de5-121">サード パーティの開発者は、これらの機能拡張インターフェイスを使用して、OSC プロバイダー Dll を作成できます。</span><span class="sxs-lookup"><span data-stu-id="65de5-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="65de5-122">OSC プロバイダーの拡張機能 DLL の詳細を次に示します。</span><span class="sxs-lookup"><span data-stu-id="65de5-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="65de5-123">拡張機能 DLL のファイル名: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="65de5-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="65de5-124">拡張機能 DLL のフレンドリ名: Microsoft Outlook のイベント プロバイダーの拡張性</span><span class="sxs-lookup"><span data-stu-id="65de5-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="65de5-125">拡張機能 DLL のメジャー バージョン: 15.0</span><span class="sxs-lookup"><span data-stu-id="65de5-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="65de5-126">Extensibiilty DLL のタイプ ライブラリのバージョン: 1.1</span><span class="sxs-lookup"><span data-stu-id="65de5-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="65de5-127">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="65de5-127">Miscellaneous technical information</span></span>

<span data-ttu-id="65de5-128">OSC プロバイダーの機能拡張モデルでは、JavaScript オブジェクト表記法 (JSON) はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="65de5-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="65de5-129">XML パーサーでは、依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="65de5-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="65de5-130">OSC プロバイダー Office、Microsoft XML Core Services (MSXML) などに含まれている XML パーサーを使用して、Microsoft.NET Framework に組み込まれた機能を解析中の XML を使用したり、サード パーティ製の XML パーサーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="65de5-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65de5-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="65de5-131">See also</span></span>

- [<span data-ttu-id="65de5-132">プロバイダーを開発するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="65de5-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="65de5-133">プロバイダーを開発する学習のためのクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="65de5-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="65de5-134">プロバイダーを展開します。</span><span class="sxs-lookup"><span data-stu-id="65de5-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="65de5-135">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="65de5-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

