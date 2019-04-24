---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックでは、Outlook Social Connector (.osc) プロバイダーの開発について学ぶためのいくつかの手順について説明します。
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329219"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>プロバイダー開発方法を学習するためのクイック手順

.osc プロバイダーを開発するには、次の一般的な手順を完了する必要があります。
  
- 次の4つの必須インターフェイスを実装します。 [i、alprovider](isocialprovideriunknown.md)、 [i入力 alsession](isocialsessioniunknown.md)、 [i入力 alprofile](isocialprofileisocialperson.md)、および iな省略[alperson](isocialpersoniunknown.md)。 ソーシャルネットワークがログオン資格情報のキャッシュ、ソーシャルネットワーク上のユーザーのフォロー、またはフレンドとそのアクティビティの動的な同期をサポートしているかどうかに応じて、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装することをお勧めします。 
    
- インターフェイスの実装と並行して、.osc プロバイダーをテストしてデバッグします。 

- .osc プロバイダーを展開します。  

- 最終的なテストは、リリース前に行います。
    
## <a name="step-a-implementing-interfaces"></a>手順 A: インターフェイスを実装する

.osc プロバイダーはインターフェイスを実装するので、.osc はこれらのインターフェイスを使用して、.osc プロバイダーを経由して、ソーシャルネットワークに関する必要な情報を取得できます。 このような情報には、次のようなものがあります。
  
- [アカウントログオン] ダイアログボックスをユーザーに表示する方法について説明します。    
- ソーシャルネットワークに表示されているように、プロバイダーが友人または活動を表示するかどうか。    
- 連絡先カードまたは Outlook の [ユーザー] ウィンドウで友人や活動を表示する方法について説明します。     
- 連絡先カードまたはユーザーウィンドウのフレンドまたは活動情報を更新するタイミング。
    
通常、この情報は、プロバイダーから .osc に渡され、インターフェイスメソッドの出力パラメーターとして XML 文字列の形式になります。 .osc プロバイダーと .osc プロバイダーの両方が、.osc プロバイダ XML スキーマに準拠しています。 そのため、インターフェイスを実装するときに、XML スキーマによって、上記のように情報を指定する方法を十分に理解する必要があります。 

以下のリソースでは、プロバイダーの機能、フレンド、およびアクティビティの XML を指定する方法について説明します。
  
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)    
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)    
- [機能 XML の例](capabilities-xml-example.md)   
- [機能の XML](xml-for-capabilities.md)    
- [Friends XML の例](friends-xml-example.md)    
- [Friends の XML](xml-for-friends.md)   
- [アクティビティフィード XML の例](activity-feed-xml-example.md)   
- [アクティビティの XML](xml-for-activities.md)
    
実装を開始する前に、次のトピックを参照して、後からデバッグプロセスで時間を節約してください。
  
- [技術的な要件](technical-requirements.md)    
- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md)    
- [.osc サンプルテンプレート](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>手順 B: デバッグ

「[プロバイダーをデバッグ](debugging-a-provider.md)する」では、.osc プロバイダーの開発時に使用できるデバッグ手順について説明します。 
  
開発中に、特定のシナリオで想定される動作をより深く理解するために、 [.osc プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)をすることもできます (たとえば、基本認証とフォームベース認証)。 
  
## <a name="step-c-deploying"></a>手順 C: 展開

展開の要件については、以下のトピックを参照してください。
  
- [プロバイダーを展開する](deploying-a-provider.md)    
- [プロバイダーの登録](registering-a-provider.md)   
- [インストールチェックリスト](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>手順 D: リリース前の最終テスト

ソーシャルネットワークと .osc プロバイダーによっては、プロバイダーをリリースする前に実行する必要があるプロバイダー固有のテストが通常あります。 推奨されるテストの一覧については、「 [.osc プロバイダーを解放する準備](getting-ready-to-release-an-osc-provider.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

