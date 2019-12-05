---
title: Visio のセキュリティ設定とコードの実行について (シェイプシート)
manager: lindalu
ms.date: 12/03/2019
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm1042370
localization_priority: Normal
ms.assetid: 506b3d81-9c93-aeff-f5b2-3354ffd3e075
description: セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。
ms.openlocfilehash: 3ad2aef9096ad2ad344b2d6fb22ed610756916bb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819267"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a>Visio のセキュリティ設定とコードの実行について (シェイプシート)

 セキュリティで保護されたアプリケーションの作成は、ソリューション開発者が直面する基本的な課題の 1 つです。 ユーザー、管理者、および開発者は、コンピューターに悪影響を及ぼす可能性のあるコードを知らずに実行している可能性を徐々に認識しています。 アプリケーションの整合性を確保することはいっそう重要になっています。 
  
すべてのセキュリティ設定は Office 全体であり、セキュリティ**センター**で設定されます ([**ファイル**] タブをクリックし、[**オプション**] をクリックして、[セキュリティ**センター**] をクリックします)。 影響を受ける設定は次のとおりです。
  
- 信頼できるパブリッシャーの指定
    
- 信頼できる場所の指定
    
- COM アドインの読み込み 
    
- 発行され、パスが検出されたアドオンの読み込み
    
- VBA マクロの読み込み
    
以前のバージョンの Visio では、設定は [**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。 Office Visio 2007 では、これらのダイアログボックスは廃止され、Microsoft Visio 2010 の場合、Visio のツールバーとメニューはリボンに置き換えられました。 
  
Office**セキュリティセンター**の設定の詳細については、「 [Microsoft Office ソリューション開発者向けのセキュリティに関する注意事項](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa433259(v=office.12))」を参照してください。
  
 デジタル署名コード、信頼のおける発行元、発行元に関する情報については、MSDN (Microsoft Developer Network web サイト) の「コード署名」を検索してください。 
  
適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。 
  
## <a name="additional-visio-resources"></a>Visio の追加リソース

- Visio アドオンと COM アドインの詳細については、MSDN の記事「 [visio 2007 でのアドオンと Com アドインの概要](https://docs.microsoft.com/previous-versions/office/developer/office-2007/bb851468(v=office.12))」を参照してください。
    
- RUNADDON 関数と**AddonName**プロパティの詳細については、MSDN の記事「 [RUNADDON 関数での変更点」および「AddonName プロパティ (Visio 2002](https://docs.microsoft.com/previous-versions/office/developer/office-xp/aa140368(v=office.10)))」を参照してください。
    

