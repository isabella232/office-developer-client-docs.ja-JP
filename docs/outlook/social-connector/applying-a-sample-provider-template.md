---
title: サンプル プロバイダーのテンプレートを適用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Outlook ソーシャル コネクタ (OSC) のサンプル プロバイダー テンプレート フレームワークを提供、OSC プロバイダーを実装するためです。 '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804323"
---
# <a name="applying-a-sample-provider-template"></a>サンプル プロバイダーのテンプレートを適用します。

Outlook ソーシャル コネクタ (OSC) のサンプル プロバイダー テンプレート フレームワークを提供、OSC プロバイダーを実装するためです。 プロバイダー テンプレートは、C++、C# および Visual Basic で使用できます。 これらのテンプレートは、プロバイダーの開発の開始点に過ぎませんプロバイダーの実装コードを作成し、プロバイダーのセットアップ パッケージを作成する、テンプレートは対応していません。 次の手順では、プロバイダーの開発を開始するときに、OSC プロバイダーのテンプレートを適用する方法を示します。
  
### <a name="to-apply-an-osc-provider-template"></a>OSC プロバイダー テンプレートを適用するには

1. [**スタート**] メニューで、 **Microsoft Visual Studio 2010**を右クリックし、**管理者として実行**] コマンドをクリックします。 ダイアログ ボックスが表示されたら、 **[はい]** は、管理者として Visual Studio を実行するをクリックします。 
    
2. プロジェクトの名前と、テンプレート内の名前空間をプロジェクトの名前と名前空間の識別子に変更します。
    
3. 適切なアセンブリ情報を指定するのには、 **AssemblyInfo**クラスを変更します。 
    
4. **タスク**としてマークされているインターフェイス メンバーを実装し、必要に応じて複数の依存関係および参照を追加します。 
    
5. プロジェクトをビルドします。
    
6. プロバイダー アセンブリの ProgID が下のキーとして表示されていることを確認`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`。
    
7. セットアップ プロジェクトを配布するには、Visual Studio または任意のセットアップ ツールでセットアップ プロジェクトを作成します。
    
8. セットアップ プロジェクトは、アセンブリの COM の登録を完了し、も手順 5 に記載されている ProgID キーを作成する必要があります。
    
## <a name="see-also"></a>関連項目

- [サンプルのダウンロード](downloading-the-samples.md)
- [OSC サンプル テンプレート](osc-sample-templates.md)

