---
title: サンプル プロバイダー テンプレートの適用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'ソーシャル コネクタ (OSC) プロバイダー Outlookサンプルは、OSC プロバイダーを実装するためのフレームワークを提供します。 '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425912"
---
# <a name="applying-a-sample-provider-template"></a>サンプル プロバイダー テンプレートの適用

ソーシャル コネクタ (OSC) プロバイダー Outlookサンプルは、OSC プロバイダーを実装するためのフレームワークを提供します。 プロバイダー テンプレートは、C++、C#、およびVisual Basic。 これらのテンプレートは、プロバイダー開発の開始点にすすらなります。テンプレートは、プロバイダーの実装コードを記述し、プロバイダーのセットアップ パッケージを作成する方法には取り組む必要はありません。 次の手順は、プロバイダーの開発を開始するときに OSC プロバイダー テンプレートを適用する方法を示しています。
  
### <a name="to-apply-an-osc-provider-template"></a>OSC プロバイダー テンプレートを適用するには

1. [スタート]**メニュー** の **[2010** 年Microsoft Visual Studio右クリックし、[管理者として実行]**コマンドをクリック** します。 プロンプトが表示されたら、[**は** い] をクリックして管理者Visual Studio実行します。 
    
2. テンプレート内のプロジェクト名と名前空間をプロジェクト名と名前空間識別子に変更します。
    
3. **AssemblyInfo クラスを変更** して、適切なアセンブリ情報を指定します。 
    
4. 必要に応じて、To-Doとして **マークされた** インターフェイス メンバーを実装し、さらに依存関係と参照を追加します。 
    
5. プロジェクトをビルドします。
    
6. プロバイダー アセンブリ ProgID が [キー] の下に一覧表示されている必要があります  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` 。
    
7. セットアップ プロジェクトを配布するには、セットアップ プロジェクトを Visual Studioまたは選択したセットアップ ツールで作成します。
    
8. セットアップ プロジェクトは、アセンブリの COM 登録を完了し、手順 5 に示す ProgID キーも作成する必要があります。
    
## <a name="see-also"></a>関連項目

- [サンプルのダウンロード](downloading-the-samples.md)
- [OSC サンプル テンプレート](osc-sample-templates.md)

