---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックは、Outlook ソーシャル コネクタ (OSC) プロバイダーの開発について学習するのにはいくつかの手順をお勧めします。
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804458"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>プロバイダー開発方法を学習するためのクイック手順

OSC プロバイダーを開発するには、次の一般的な手順を完了する必要があります。
  
- 4 つの必須のインターフェイスを実装する: [ISocialProvider](isocialprovideriunknown.md)、 [ISocialSession](isocialsessioniunknown.md)、 [ISocialProfile](isocialprofileisocialperson.md)、および[ISocialPerson](isocialpersoniunknown.md)。 ソーシャル ネットワーク、または動的に同期の友人との活動では、[次のユーザーのログオン資格情報をキャッシュするためのソーシャル ネットワークのサポートによって[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装する場合があります。 
    
- インターフェイスを実装すると、並列でテストし、OSC プロバイダーをデバッグします。 

- OSC プロバイダーを展開します。  

- リリース前に、の最終テストを行います。
    
## <a name="step-a-implementing-interfaces"></a>手順 a: 実装インターフェイスします。

OSC プロバイダーはインターフェイスを実装する、OSC や OSC プロバイダーを通じて、ソーシャル ネットワークから、必要な情報を入手するのにはこれらのインタ フェースを使用できるようにします。 このような情報には次のものが含まれています。
  
- アカウントの [ログオン] ダイアログ ボックスをユーザーに提示する方法です。    
- かどうか、プロバイダーをサポートしている表示されている友人や活動ソーシャル ネットワークに表示されます。    
- 友人や活動を連絡先カードまたは Outlook 人物情報ウィンドウに表示する方法です。     
- 連絡先カードまたは人物情報ウィンドウの友人や活動の情報を更新する場合。
    
情報は、インターフェイス メソッドの出力パラメーターとしての XML 文字列の形式で、OSC を通常、プロバイダーから渡されます。 OSC と OSC プロバイダーの両方は、OSC プロバイダーの XML スキーマに準拠します。 したがって、インターフェイスを実装する過程で XML スキーマを使用するも上記の情報を指定する方法を十分に理解が必要。 

次のリソースには、プロバイダーの機能、友人、および活動の XML を指定する方法について説明します。
  
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)    
- [友人や活動を同期します。](synchronizing-friends-and-activities.md)    
- [機能の XML の例](capabilities-xml-example.md)   
- [機能のための XML](xml-for-capabilities.md)    
- [友人の XML の例](friends-xml-example.md)    
- [友人の XML](xml-for-friends.md)   
- [アクティビティ フィードの XML の例](activity-feed-xml-example.md)   
- [活動の XML](xml-for-activities.md)
    
実装を開始する前にも後のデバッグ プロセスで時間を節約するには、次のトピックを参照してください。
  
- [技術的な要件](technical-requirements.md)    
- [プロバイダーを開発するためのベスト プラクティス](best-practices-for-developing-a-provider.md)    
- [OSC サンプル テンプレート](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>手順 b: デバッグ

トピックは[、プロバイダーのデバッグ](debugging-a-provider.md)OSC プロバイダーを開発する際に使用することができますプロシージャのデバッグをお勧めします。 
  
開発しているときに、[準備 OSC プロバイダーを解放する](getting-ready-to-release-an-osc-provider.md)(たとえば、基本的なとフォーム ベース認証) は、特定のシナリオで予想される動作の理解を参照することも。 
  
## <a name="step-c-deploying"></a>手順 c: を展開します。

展開の要件の詳細については、次のトピックを参照してください。
  
- [プロバイダーを展開します。](deploying-a-provider.md)    
- [プロバイダーを登録します。](registering-a-provider.md)   
- [インストールのチェックリスト](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>手順 d: の最終リリース前にテスト

ソーシャル ネットワーク、OSC プロバイダーによっては、プロバイダーをリリースする前に実行する必要があります通常は、プロバイダー固有のテストがあります。 テストの候補の一覧[を取得する準備ができて OSC プロバイダーを解放する](getting-ready-to-release-an-osc-provider.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

