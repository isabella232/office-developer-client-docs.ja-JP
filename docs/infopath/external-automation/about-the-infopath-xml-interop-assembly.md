---
title: InfoPath XML 相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml の相互運用機能 [2007]、infopath InfoPath 2007 では、XML のプライマリ相互運用機能アセンブリ、InfoPath XML 相互運用機能アセンブリ
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。
ms.openlocfilehash: 8d3fb1c1de141fe23c655e82b77d83a8e2b11abd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798991"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="6e729-104">InfoPath XML 相互運用機能アセンブリについて</span><span class="sxs-lookup"><span data-stu-id="6e729-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="6e729-105">InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。</span><span class="sxs-lookup"><span data-stu-id="6e729-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="6e729-106">InfoPath セットアップ プログラムで [ **.NET プログラミング サポート**] オプションは、次の 3 つの相互運用機能アセンブリをインストールします。</span><span class="sxs-lookup"><span data-stu-id="6e729-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="6e729-107">相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。</span><span class="sxs-lookup"><span data-stu-id="6e729-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="6e729-108">Microsoft.Office.Interop.InfoPath.Xml.dll、それらのアセンブリのいずれかの Microsoft XML Core Services (MSXML) の COM サーバーによって公開されているメンバーと協力するために使用される[Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml)の名前空間のメンバーが用意されています外部アプリケーションからは、マネージ コードを使用して InfoPath を自動化します。</span><span class="sxs-lookup"><span data-stu-id="6e729-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6e729-109">InfoPath の外部オートメーション プロジェクトに必要な Microsoft.Office.Interop.InfoPath.dll と Microsoft.Office.Interop.InfoPath.Xml.dll の相互運用機能アセンブリへの参照を手動で確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e729-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="6e729-110">外部オートメーションの詳細については、[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e729-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e729-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e729-111">See also</span></span>

- [<span data-ttu-id="6e729-112">InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する</span><span class="sxs-lookup"><span data-stu-id="6e729-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

