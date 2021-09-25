---
title: InfoPath XML 相互運用機能アセンブリについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml 相互運用機能 [infopath 2007],InfoPath 2007,XML プライマリ相互運用機能アセンブリ,InfoPath XML 相互運用機能アセンブリ
ms.localizationpriority: medium
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。
ms.openlocfilehash: bae183892569652a41e62b302518fb43b933a370
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572348"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>InfoPath XML 相互運用機能アセンブリについて

InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。

InfoPath **セットアップ プログラムの .NET プログラミング サポート** オプションは、3 つの相互運用機能アセンブリをインストールします。 相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 これらのアセンブリの 1 つである Microsoft.Office.Interop.InfoPath.Xml.dll は、マネージ コードを使用して[InfoPath](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external)を自動化する外部アプリケーションから Microsoft XML Core Services (MSXML) の COM サーバーによって公開されるメンバーを操作するために使用されるMicrosoft.Office.Interop.InfoPath.Xml名前空間のメンバーを提供します。 
  
> [!NOTE]
> InfoPath 外部オートメーション プロジェクトMicrosoft.Office.Interop.InfoPath.dll必要Microsoft.Office.Interop.InfoPath.Xml.dll相互運用機能アセンブリへの参照は、手動で確立する必要があります。 外部オートメーションの詳細については、「外部オートメーションの [シナリオと例」を参照してください](external-automation-scenarios-and-examples.md)。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

