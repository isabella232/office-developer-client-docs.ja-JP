---
title: 技術的要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: このトピックでは、サポートされているプログラミング言語、COM 可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (OSC) プロバイダー拡張 DLL の詳細について説明します。
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329156"
---
# <a name="technical-requirements"></a><span data-ttu-id="e535b-103">技術的要件</span><span class="sxs-lookup"><span data-stu-id="e535b-103">Technical requirements</span></span>

<span data-ttu-id="e535b-104">このトピックでは、サポートされているプログラミング言語、COM 可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (OSC) プロバイダー拡張 DLL の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="e535b-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="e535b-105">プログラミング言語と COM の要件</span><span class="sxs-lookup"><span data-stu-id="e535b-105">Programming language and COM requirements</span></span>

<span data-ttu-id="e535b-106">OSC プロバイダーは、Visual C# や Visual Basic などの管理言語、または Visual C++ などの管理されていない言語を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="e535b-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="e535b-107">COM に表示される DLL コンポーネントを作成できる任意のツールを使用して、OSC プロバイダーを開発できます。</span><span class="sxs-lookup"><span data-stu-id="e535b-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="e535b-108">管理言語または管理されていない言語を使用してプロバイダーを開発する決定は、プロバイダー インストール パッケージのダウンロード サイズと依存関係を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e535b-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="e535b-109">OSC プロバイダーは、次の定義に従って COM に表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e535b-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="e535b-110">インストール後、COM 自己登録または regsvr32 を使用して OSC プロバイダーを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e535b-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="e535b-111">OSC プロバイダー DLL の COM 登録は、HKCU または HKLM の下でプロバイダーを登録します。</span><span class="sxs-lookup"><span data-stu-id="e535b-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="e535b-112">プロバイダーの ProgID は 、 の下に登録されています  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。</span><span class="sxs-lookup"><span data-stu-id="e535b-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="e535b-113">マネージ言語で開発された OSC プロバイダーは、COM に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e535b-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="e535b-114">OSC プロバイダーは、プロバイダー DLL がシングル スレッド アパートメント (STA) とマルチスレッド アパートメント (MTA) スレッド モデルの両方をサポートしているという値を Windows レジストリに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e535b-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="e535b-115">COM スレッド モデルの詳細については [、「DESCRIPTIONs and Workings of OLE Threading Models」を参照してください](https://support.microsoft.com/kb/150777)。</span><span class="sxs-lookup"><span data-stu-id="e535b-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="e535b-116">OSC プロバイダーの機能拡張のメソッドは、string や bool などのプリミティブ型 **を\*\*\*\*返す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e535b-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="e535b-117">特定 **の文字列** 戻り値は、OSC プロバイダーの機能拡張のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="e535b-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="e535b-118">戻り値としてサポートされているのは XML のみです。</span><span class="sxs-lookup"><span data-stu-id="e535b-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="e535b-119">OSC プロバイダー拡張 DLL の詳細</span><span class="sxs-lookup"><span data-stu-id="e535b-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="e535b-120">OSC プロバイダーの機能拡張をサポートするコンポーネントは、OSC プロバイダー拡張 DLL です。</span><span class="sxs-lookup"><span data-stu-id="e535b-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="e535b-121">サードパーティの開発者は、これらの機能拡張インターフェイスを使用して OSC プロバイダー DLL を構築できます。</span><span class="sxs-lookup"><span data-stu-id="e535b-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="e535b-122">次の一覧は、OSC プロバイダー拡張 DLL の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="e535b-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="e535b-123">拡張 DLL ファイル名: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="e535b-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="e535b-124">拡張 DLL の表示名: Microsoft Outlook ソーシャル プロバイダーの機能拡張</span><span class="sxs-lookup"><span data-stu-id="e535b-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="e535b-125">拡張 DLL メジャー バージョン: 15.0</span><span class="sxs-lookup"><span data-stu-id="e535b-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="e535b-126">Extensibiilty DLL TypeLib バージョン: 1.1</span><span class="sxs-lookup"><span data-stu-id="e535b-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="e535b-127">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="e535b-127">Miscellaneous technical information</span></span>

<span data-ttu-id="e535b-128">JAVAScript オブジェクト表記 (JSON) は、OSC プロバイダー拡張モデルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e535b-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="e535b-129">XML パーサーには依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="e535b-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="e535b-130">OSC プロバイダーは、Office MSXML (Microsoft XML Core Services )などの Office に含まれる XML パーサーを使用したり、Microsoft .NET Framework に組み込まれている XML 解析機能を使用したり、サードパーティの XML パーサーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e535b-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e535b-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e535b-131">See also</span></span>

- [<span data-ttu-id="e535b-132">プロバイダーの開発に関するベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e535b-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="e535b-133">プロバイダーを開発するための学習のクイック ステップ</span><span class="sxs-lookup"><span data-stu-id="e535b-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="e535b-134">プロバイダーの展開</span><span class="sxs-lookup"><span data-stu-id="e535b-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="e535b-135">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="e535b-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

