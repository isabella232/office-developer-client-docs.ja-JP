---
title: Visio のセキュリティ設定とコードの実行について (シェイプシート)
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
ms.localizationpriority: medium
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行する可能性をますます認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。
ms.openlocfilehash: c7cd3c22a2d6200a8d4c4f00a53bf27a189d726b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608740"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a>Visio のセキュリティ設定とコードの実行について (シェイプシート)

 セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行する可能性をますます認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。 
  
すべてのセキュリティ設定はOffice全体に設定され、セキュリティ センターで設定 **されます ([** ファイル] タブをクリックし、[オプション] をクリックし、[セキュリティ センター]**をクリックします**)。 影響を受ける設定には、次のものが含まれます。
  
- 信頼できるパブリッシャーの指定
    
- 信頼できる場所の指定
    
- COM アドインの読み込み 
    
- 発行され、パスが検出されたアドオンの読み込み
    
- VBA マクロの読み込み
    
以前のバージョンの Visio では、設定は [**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。 Office Visio 2007 年現在、これらのダイアログ ボックスは削除され、Microsoft Visio 2010 では、Visio ツールバーとメニューがリボンに置き換えされています。 
  
セキュリティ センターの設定の詳細については、「Office **ソリューション** 開発者向け [セキュリティ Microsoft Officeを参照してください](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa433259(v=office.12))。
  
 デジタル署名コードと信頼できるソースと発行元の詳細については、MSDN の web サイトで "コード署名" をMicrosoft Developer Networkしてください。 
  
適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。 
  
## <a name="additional-visio-resources"></a>Visio の追加リソース

- Visio アドオンと COM アドインの詳細については、MSDN の記事「Visio [2007](https://docs.microsoft.com/previous-versions/office/developer/office-2007/bb851468(v=office.12))のアドオンと COM アドインの概要」を参照してください。
    
- RUNADDON 関数と **AddonName** プロパティの詳細については、MSDN の記事「RUNADDON 関数の変更点」および「AddOnName プロパティ for Visio [2002」を参照](https://docs.microsoft.com/previous-versions/office/developer/office-xp/aa140368(v=office.10))してください。
    

