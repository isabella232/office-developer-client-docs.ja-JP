---
title: 技術的要件
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: このトピックでは、サポートされているプログラミング言語、COM の可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (.osc) プロバイダ拡張 DLL の詳細について説明します。
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329156"
---
# <a name="technical-requirements"></a><span data-ttu-id="ab300-103">技術的要件</span><span class="sxs-lookup"><span data-stu-id="ab300-103">Technical requirements</span></span>

<span data-ttu-id="ab300-104">このトピックでは、サポートされているプログラミング言語、COM の可視性とメソッドの戻り値の型の要件、および Outlook Social Connector (.osc) プロバイダ拡張 DLL の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab300-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="ab300-105">プログラミング言語と COM の要件</span><span class="sxs-lookup"><span data-stu-id="ab300-105">Programming language and COM requirements</span></span>

<span data-ttu-id="ab300-106">.osc プロバイダーを作成するには、visual C# または visual Basic などのマネージ言語または visual C++ などのアンマネージ言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab300-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="ab300-107">COM で認識可能な DLL コンポーネントを作成できる任意のツールを使用して、.osc プロバイダーを開発できます。</span><span class="sxs-lookup"><span data-stu-id="ab300-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="ab300-108">マネージ言語またはアンマネージ言語を使用してプロバイダーを開発する場合は、プロバイダーインストールパッケージのダウンロードサイズと依存関係を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab300-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="ab300-109">.osc プロバイダーは、次のように定義されているように、COM から参照可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab300-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="ab300-110">インストール後は、COM の自己登録または regsvr32 を使用して、.osc プロバイダーを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab300-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="ab300-111">.osc プロバイダ DLL の COM 登録は、そのプロバイダーを HKCU または HKLM の下に登録します。</span><span class="sxs-lookup"><span data-stu-id="ab300-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="ab300-112">プロバイダーの ProgID は、に登録`HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`されています。</span><span class="sxs-lookup"><span data-stu-id="ab300-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="ab300-113">マネージ言語で開発された .osc プロバイダーは、COM に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab300-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="ab300-114">.osc プロバイダーは、Windows レジストリに値を追加する必要があります。これは、プロバイダー DLL がシングルスレッドアパートメント (STA) とマルチスレッドアパートメント (MTA) スレッドモデルの両方をサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab300-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="ab300-115">COM スレッドモデルの詳細については、「 [OLE スレッディングモデルの説明と働き](https://support.microsoft.com/kb/150777)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab300-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="ab300-116">.osc プロバイダ拡張性のメソッドは、 **string**や**bool**などのプリミティブ型を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab300-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="ab300-117">**文字列**の戻り値は、そのプロバイダー拡張機能のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab300-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="ab300-118">戻り値としてサポートされているのは XML のみです。</span><span class="sxs-lookup"><span data-stu-id="ab300-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="ab300-119">.osc プロバイダ拡張 DLL の詳細</span><span class="sxs-lookup"><span data-stu-id="ab300-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="ab300-120">.osc プロバイダ拡張機能をサポートするコンポーネントは、.osc プロバイダ拡張 DLL です。</span><span class="sxs-lookup"><span data-stu-id="ab300-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="ab300-121">サードパーティの開発者は、これらの機能拡張インターフェイスを使用して、.osc プロバイダ dll を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ab300-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="ab300-122">次のリストは、.osc プロバイダ拡張 DLL の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab300-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="ab300-123">機能拡張 DLL ファイル名: 指定した dll</span><span class="sxs-lookup"><span data-stu-id="ab300-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="ab300-124">機能拡張 DLL のフレンドリ名: Microsoft Outlook Social Provider の拡張性</span><span class="sxs-lookup"><span data-stu-id="ab300-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="ab300-125">機能拡張 DLL のメジャーバージョン: 15.0</span><span class="sxs-lookup"><span data-stu-id="ab300-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="ab300-126">Extensibiilty DLL TypeLib バージョン: 1.1</span><span class="sxs-lookup"><span data-stu-id="ab300-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="ab300-127">その他の技術情報</span><span class="sxs-lookup"><span data-stu-id="ab300-127">Miscellaneous technical information</span></span>

<span data-ttu-id="ab300-128">JavaScript Object Notation (JSON) は、.osc プロバイダ拡張モデルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ab300-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="ab300-129">XML パーサーに依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="ab300-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="ab300-130">.osc プロバイダーは、microsoft xml Core Services (MSXML) などの Office に付属する xml パーサーを使用して、microsoft .net Framework に組み込まれている xml 解析機能を使用するか、サードパーティの xml パーサーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab300-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab300-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab300-131">See also</span></span>

- [<span data-ttu-id="ab300-132">プロバイダーを開発するためのベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="ab300-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="ab300-133">プロバイダーを開発するための簡単な手順</span><span class="sxs-lookup"><span data-stu-id="ab300-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="ab300-134">プロバイダーを展開する</span><span class="sxs-lookup"><span data-stu-id="ab300-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="ab300-135">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="ab300-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

