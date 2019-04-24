---
title: InfoPath XML 相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml 相互運用機能 [infopath 2007], infopath 2007, xml プライマリ相互運用機能アセンブリ, infopath xml 相互運用機能アセンブリ
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303781"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="ac3f6-104">InfoPath XML 相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="ac3f6-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="ac3f6-105">InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="ac3f6-106">InfoPath セットアッププログラムの **.net プログラミングサポート**オプションは、3つの相互運用機能アセンブリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="ac3f6-107">相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="ac3f6-108">これらのアセンブリの1つには、microsoft xml Core Services (MSXML) の COM サーバーによって[](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external)公開されているメンバーを操作するために使用される、名前空間のメンバーが含まれています。マネージコードを使用して InfoPath を自動化する外部アプリケーションから。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ac3f6-109">infopath 外部オートメーションプロジェクトに必要な、microsoft office との相互運用機能アセンブリへの参照は、手動で設定する必要があります (これについては、「」を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="ac3f6-110">外部オートメーションの詳細については、「[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac3f6-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac3f6-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac3f6-111">See also</span></span>

- [<span data-ttu-id="ac3f6-112">InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する</span><span class="sxs-lookup"><span data-stu-id="ac3f6-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

