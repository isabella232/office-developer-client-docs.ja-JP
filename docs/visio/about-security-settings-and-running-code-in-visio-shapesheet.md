---
title: Visio のセキュリティ設定とコードの実行について (シェイプシート)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
localization_priority: Normal
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。
ms.openlocfilehash: 72b4a45faa46778b7a369cfe458ee4e0e9ea71bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345025"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a>Visio のセキュリティ設定とコードの実行について (シェイプシート)

 セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。 
  
すべてのセキュリティ設定は Office 全体であり、セキュリティ**センター**で設定されます ([**ファイル**] タブをクリックし、[**オプション**] をクリックして、[セキュリティ**センター**] をクリックします)。 影響を受ける設定は次のとおりです。
  
- 信頼できるパブリッシャーの指定
    
- 信頼できる場所の指定
    
- COM アドインの読み込み 
    
- 発行され、パスが検出されたアドオンの読み込み
    
- VBA マクロの読み込み
    
以前のバージョンの Visio では、設定は [**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。 Office visio 2007 では、これらのダイアログボックスは廃止され、Microsoft visio 2010 の場合、visio のツールバーとメニューはリボンに置き換えられました。 
  
Office**セキュリティセンター**の設定の詳細については、「 [Microsoft office ソリューション開発者向けのセキュリティに関する注意事項](https://msdn.microsoft.com/en-us/library/aa433259.aspx)」を参照してください。
  
 デジタル署名コード、信頼のおける発行元、発行元に関する情報については、MSDN (Microsoft Developer Network web サイト) の「コード署名」を検索してください。 
  
適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。 
  
## <a name="additional-visio-resources"></a>Visio の追加リソース

- visio アドオンと com アドインの詳細については、MSDN の記事「 [visio 2007 でのアドオンと com アドインの概要](https://msdn.microsoft.com/library/bb851468.aspx)」を参照してください。
    
- RUNADDON 関数と**AddonName**プロパティの詳細については、MSDN の記事「 [RUNADDON 関数での変更点」および「AddonName プロパティ (Visio 2002](https://msdn.microsoft.com/library/aa140368%28office.10%29.aspx))」を参照してください。
    

