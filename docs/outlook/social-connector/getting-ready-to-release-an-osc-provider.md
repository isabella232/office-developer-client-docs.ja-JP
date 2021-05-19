---
title: OSC プロバイダーをリリースする準備
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、ソーシャル コネクタ (OSC) プロバイダーをリリースする前Outlookテストについて説明します。
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414663"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>OSC プロバイダーをリリースする準備

このセクションでは、ソーシャル コネクタ (OSC) プロバイダーをリリースする前Outlookテストについて説明します。 このセクションのトピックの参照を開始し、開発およびテストの段階でこれらのテストの一部を実行できますが、リリース時にはこれらのテストを完了している必要があります。 

これらのテストでは、OSC プロバイダーに指定する機能に関して、OSC プロバイダー インターフェイスの実装の基本的な機能を確認します。 また、OSC は複数の Office クライアント アプリケーションで共有される機能ですが、これらのテストでは、Outlook をクライアントとして使用して、基本的な機能をテストします。 プロバイダー固有の機能に他のテストが必要かどうかを判断する必要があります。
  
## <a name="in-this-section"></a>このセクションの内容

- [展開の](testing-deployment.md)テスト: OSC プロバイダーのインストールとアンインストールについてテストする必要があるシナリオについて説明します。
    
- [機能、認証、](testing-capabilities-authentication-and-configuration.md)および構成のテスト: 機能を取得するためのテストと、アカウントの構成とソーシャル ネットワークのユーザー認証に関するシナリオについて説明します。
    
- [[次のユーザーStop-Followingテスト](testing-following-and-stop-following-persons.md)]: OSC プロバイダーがユーザーを友人として追加したり、ソーシャル ネットワークから友人を削除したりする機能をテストするシナリオについて説明します。 
    
- [友人の](testing-friends.md)テスト: OSC プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合はフレンドとフレンド以外のデータが適切に返されるのを確認するテストとシナリオについて説明します。
    
- [テストアクティビティ](testing-activities.md): OSC プロバイダーが、プロバイダーがサポートする同期モードに応じて、該当する場合は友人や友人以外のアクティビティが適切に返されるのを確認するテストとシナリオについて説明します。
    
## <a name="reference"></a>参照

- [Outlookソーシャル コネクタ プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [OSC サンプル テンプレート](osc-sample-templates.md)
  
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)
  
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーのデバッグ](debugging-a-provider.md)
  
- [プロバイダーの展開](deploying-a-provider.md)
  

