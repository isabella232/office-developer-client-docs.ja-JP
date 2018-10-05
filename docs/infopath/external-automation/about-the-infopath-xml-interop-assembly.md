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
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386825"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>InfoPath XML 相互運用機能アセンブリについて

InfoPath XML 相互運用機能アセンブリは、マネージ コードと、InfoPath を自動化する外部のアプリケーションからの Microsoft XML Core Services (MSXML) が公開する COM サーバーとの間の相互運用性をサポートするために提供されます。

InfoPath セットアップ プログラムで [ **.NET プログラミング サポート**] オプションは、次の 3 つの相互運用機能アセンブリをインストールします。 相互運用アセンブリとは、マネージ コードとアンマネージ コードの仲介役として機能する .NET アセンブリで、COM オブジェクトのメンバーを、対応する .NET マネージ メンバーにマップします。 Microsoft.Office.Interop.InfoPath.Xml.dll、それらのアセンブリのいずれかの Microsoft XML Core Services (MSXML) の COM サーバーによって公開されているメンバーと協力するために使用される[Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external)の名前空間のメンバーが用意されています外部アプリケーションからは、マネージ コードを使用して InfoPath を自動化します。 
  
> [!NOTE]
> InfoPath の外部オートメーション プロジェクトに必要な Microsoft.Office.Interop.InfoPath.dll と Microsoft.Office.Interop.InfoPath.Xml.dll の相互運用機能アセンブリへの参照を手動で確立する必要があります。 外部オートメーションの詳細については、[外部オートメーションのシナリオと例](external-automation-scenarios-and-examples.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用して MSXML および System.Xml を操作する](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

