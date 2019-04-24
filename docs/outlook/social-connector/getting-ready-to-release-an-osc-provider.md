---
title: .osc プロバイダーをリリースする準備をする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: このセクションでは、Outlook Social Connector (.osc) プロバイダーを解放する前に実行できるテストを示します。
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327154"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>.osc プロバイダーをリリースする準備をする

このセクションでは、Outlook Social Connector (.osc) プロバイダーを解放する前に実行できるテストを示します。 このセクションのトピックを参照して、開発フェーズとテストフェーズでこれらのテストの一部を実行することができますが、リリースするまでにこれらのテストを完了しておく必要があります。 

これらのテストは、.osc プロバイダインターフェイスの実装の基本的な機能を、.osc プロバイダーに対して指定した機能に関して確認します。 また、.osc は複数の Office クライアントアプリケーションによって共有されている機能ですが、これらのテストでは、クライアントとして Outlook を使用して基本的な機能をテストします。 プロバイダー固有の機能に他のテストが必要かどうかを判断する必要があります。
  
## <a name="in-this-section"></a>このセクションの内容

- [展開のテスト](testing-deployment.md): .osc プロバイダーのインストールとアンインストールに関してテストする必要があるシナリオについて説明します。
    
- [機能、認証、および構成をテスト](testing-capabilities-authentication-and-configuration.md)する: 機能を取得するためのテスト、およびソーシャルネットワークのアカウントの構成とユーザーの認証に関するシナリオについて説明します。
    
- [フォローおよび停止し](testing-following-and-stop-following-persons.md)ているユーザーのテスト: ユーザーをフレンドとして追加したり、ソーシャルネットワークから友人を削除したりするための、.osc プロバイダーの機能をテストするシナリオについて説明します。 
    
- [友人をテスト](testing-friends.md)する: プロバイダーがサポートする同期モードに応じて、.osc プロバイダーがフレンドおよび非友人のデータを適切に返すことを確認するためのテストとシナリオについて説明します。
    
- [アクティビティのテスト](testing-activities.md): プロバイダーがサポートする同期モードに応じて、.osc プロバイダーがフレンドおよび非友人のアクティビティを適切に返すことを確認するためのテストとシナリオについて説明します。
    
## <a name="reference"></a>リファレンス

- [Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>関連情報

- [.osc サンプルテンプレート](osc-sample-templates.md)
  
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)
  
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)
  
- [プロバイダーをデバッグする](debugging-a-provider.md)
  
- [プロバイダーを展開する](deploying-a-provider.md)
  

