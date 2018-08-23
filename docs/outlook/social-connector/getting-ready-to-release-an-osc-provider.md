---
title: OSC プロバイダーをリリースする準備をします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、Outlook ソーシャル コネクタ (OSC) は、プロバイダーをリリースする前に行うことができますテストをお勧めします。
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804338"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>OSC プロバイダーをリリースする準備をします。

このセクションでは、Outlook ソーシャル コネクタ (OSC) は、プロバイダーをリリースする前に行うことができますテストをお勧めします。 このセクションのトピックを参照するを起動し、開発とテストのフェーズの中にいくつかのこれらのテストを実行しますが、リリースした時点でこれらのテストを完了する必要があります。 

OSC プロバイダーを指定する機能に関して、OSC プロバイダーのインターフェイスの実装の基本的な機能を検証します。 また、複数の Office クライアント アプリケーションで共有する機能ですが、OSC、これらのテスト Outlook を使用クライアントとして基本的な機能をテストします。 その他のテストは、プロバイダーに固有の機能に必要かどうかを決定する必要があります。
  
## <a name="in-this-section"></a>このセクションの内容

- [展開テスト](testing-deployment.md): をインストールすると、OSC プロバイダーをアンインストールするをテストする必要があるシナリオについて説明します。
    
- [機能のテスト、認証、および構成](testing-capabilities-authentication-and-configuration.md): 機能、およびアカウントの構成とソーシャル ネットワークのユーザーの認証のシナリオを取得するためのテストを説明します。
    
- [次のテストと停止次の人](testing-following-and-stop-following-persons.md): 友人としてユーザーを追加する機能やソーシャル ネットワークからフレンドを削除するのには、OSC プロバイダーの機能をテストするシナリオについて説明します。 
    
- [友人のテスト](testing-friends.md): テストおよび該当する場合、プロバイダーがサポートする同期モードに応じて、OSC プロバイダーがその友人や、友人以外のデータを適切に返すことを確認するシナリオについて説明します。
    
- [活動のテスト](testing-activities.md): テストおよび該当する場合、プロバイダーがサポートする同期モードに応じて、OSC プロバイダーがその友人や、友人以外の活動を適切に返すことを確認するシナリオについて説明します。
    
## <a name="reference"></a>リファレンス

- [Outlook ソーシャル コネクタ プロバイダーの参照](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)
  
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーを展開します。](deploying-a-provider.md)
  

