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
description: セキュリティで保護されたアプリケーションを作成すると、ソリューション開発者が直面する主な課題の 1 つです。 ユーザー、管理者、および開発者は、自分のコンピューターに問題を引き起こすことができるコードを無意識に実行する可能性を徐々 に認識します。 重要ですこれまでよりも、アプリケーションの整合性を確保することができます。
ms.openlocfilehash: e114fef650f31a6e0adf368d339f71e3a32113f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804730"
---
# <a name="about-security-settings-and-running-code-in-visio-shapesheet"></a>Visio のセキュリティ設定とコードの実行について (シェイプシート)

 セキュリティで保護されたアプリケーションを作成すると、ソリューション開発者が直面する主な課題の 1 つです。 ユーザー、管理者、および開発者は、自分のコンピューターに問題を引き起こすことができるコードを無意識に実行する可能性を徐々 に認識します。 重要ですこれまでよりも、アプリケーションの整合性を確保することができます。 
  
すべてのセキュリティ設定は**セキュリティ センター**の設定は、Office 全体 (、[**ファイル**] タブをクリックして、**オプション**] をクリックし、[**セキュリティ センター**] をクリック) します。 影響を受ける設定を以下に示します。
  
- 信頼できるパブリッシャーの指定
    
- 信頼できる場所の指定
    
- COM アドインの読み込み 
    
- 発行され、パスが検出されたアドオンの読み込み
    
- VBA マクロの読み込み
    
Visio の以前のバージョンでは、設定は、[**セキュリティ**] ダイアログ ボックスと、[**オプション**] ダイアログ ボックス ([**ツール**] メニュー) の [**セキュリティ**] タブで行っていました。 Office Visio 2007 では、現在これらのダイアログ ボックスが除去され、Microsoft Visio 2010 では、現在の Visio ツールバーとメニューに置き換えられているリボンです。 
  
Office**セキュリティ センター**の設定の詳細については、 [Microsoft Office ソリューション開発者向けのセキュリティ ノート](http://msdn2.microsoft.com/en-us/library/aa433259.aspx)を参照してください。
  
 デジタル署名コード、信頼のおける発行元、発行側に関する詳細については、MSDN (Microsoft Developer Network) Web サイト上で「コード署名」を検索してください。 
  
適切なセキュリティ設計の実践および技術に関する詳細については、MSDN 上で「セキュリティ」を検索してください。 
  
## <a name="additional-visio-resources"></a>Visio の追加リソース

- Visio アドオンおよび COM アドインに関する詳細については、[概要のアドオンおよび COM アドインで Visio 2007](http://msdn.microsoft.com/en-us/library/bb851468.aspx)は、MSDN の記事を参照してください。
    
- RUNADDON 関数および**AddonName**プロパティの詳細については、MSDN の記事[によって、RUNADDON 関数および AddOnName プロパティ Visio 2002 での変更](http://msdn.microsoft.com/en-us/library/aa140368%28office.10%29.aspx)を参照してください。
    

