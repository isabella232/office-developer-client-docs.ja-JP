---
title: サンプルプロバイダテンプレートを適用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'サンプルの Outlook Social Connector (.osc) プロバイダテンプレートには、.osc プロバイダーを実装するためのフレームワークが用意されています。 '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425912"
---
# <a name="applying-a-sample-provider-template"></a>サンプルプロバイダテンプレートを適用する

サンプルの Outlook Social Connector (.osc) プロバイダテンプレートには、.osc プロバイダーを実装するためのフレームワークが用意されています。 プロバイダーテンプレートは、C++、C#、および Visual Basic で使用できます。 これらのテンプレートは、プロバイダー開発の出発点にすぎません。テンプレートは、プロバイダーの実装コードの記述と、プロバイダーのセットアップパッケージの作成には対応していません。 次の手順は、プロバイダーの開発を開始するときに、.osc プロバイダテンプレートを適用する方法を示しています。
  
### <a name="to-apply-an-osc-provider-template"></a>.osc プロバイダテンプレートを適用するには

1. [**スタート**] メニューで、[ **Microsoft Visual Studio 2010** ] を右クリックし、[**管理者として実行**] コマンドをクリックします。 メッセージが表示されたら、[**はい**] をクリックして、Visual Studio を管理者として実行します。 
    
2. テンプレート内のプロジェクト名と名前空間をプロジェクト名と名前空間識別子に変更します。
    
3. 適切なアセンブリ情報を指定するように、 **AssemblyInfo**クラスを変更します。 
    
4. do としてマークされたインターフェイスメンバーを実装し、必要**に**応じてさらに依存関係と参照を追加します。 
    
5. プロジェクトをビルドします。
    
6. プロバイダアセンブリ ProgID がのキーとしてリストされ`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`ていることを確認します。
    
7. セットアッププロジェクトを配布するには、Visual Studio または任意のセットアップツールでセットアッププロジェクトを作成します。
    
8. セットアッププロジェクトは、アセンブリの COM 登録を完了し、手順5に示されているように ProgID キーを作成する必要があります。
    
## <a name="see-also"></a>関連項目

- [サンプルのダウンロード](downloading-the-samples.md)
- [.osc サンプルテンプレート](osc-sample-templates.md)

