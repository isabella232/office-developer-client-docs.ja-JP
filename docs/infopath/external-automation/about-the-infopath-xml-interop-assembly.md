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
# <a name="about-the-infopath-xml-interop-assembly"></a>InfoPath XML 相互運用機能アセンブリについて

InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。

InfoPath セットアッププログラムの **.net プログラミングサポート**オプションは、3つの相互運用機能アセンブリをインストールします。 相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 これらのアセンブリの1つには、microsoft xml Core Services (MSXML) の COM サーバーによって[](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external)公開されているメンバーを操作するために使用される、名前空間のメンバーが含まれています。マネージコードを使用して InfoPath を自動化する外部アプリケーションから。 
  
> [!NOTE]
> infopath 外部オートメーションプロジェクトに必要な、microsoft office との相互運用機能アセンブリへの参照は、手動で設定する必要があります (これについては、「」を参照してください)。 外部オートメーションの詳細については、「[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

