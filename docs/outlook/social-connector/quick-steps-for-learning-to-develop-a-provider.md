---
title: プロバイダー開発方法を学習するためのクイック手順
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: このトピックでは、ソーシャル コネクタ (OSC) プロバイダーの開発についてOutlook手順を示します。
ms.openlocfilehash: 3dbb4e40a3cfe3d2b37c7b2fb9ef60515640adc6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629061"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>プロバイダー開発方法を学習するためのクイック手順

OSC プロバイダーを開発するには、次の一般的な手順を実行する必要があります。
  
- [ISocialProvider、ISocialSession、ISocialProfile、](isocialprovideriunknown.md)[および ISocialPerson](isocialprofileisocialperson.md)の 4 つの必須インターフェイスを[実装します](isocialpersoniunknown.md)。 [](isocialsessioniunknown.md) ログオン資格情報のキャッシュ、ソーシャル ネットワーク上のユーザーの実行、友人とそのアクティビティの動的同期に関するソーシャル ネットワークのサポートに応じて [、ISocialSession2](isocialsession2iunknown.md) インターフェイスを実装できます。 
    
- インターフェイスの実装と並行して、OSC プロバイダーをテストおよびデバッグします。 

- OSC プロバイダーを展開します。  

- リリース前に最終テストを行います。
    
## <a name="step-a-implementing-interfaces"></a>手順 A: インターフェイスの実装

OSC プロバイダーは、OSC がこれらのインターフェイスを使用して、OSC プロバイダーを介してソーシャル ネットワークに関する必要な情報を取得したり、ソーシャル ネットワークから取得したりできるよう、インターフェイスを実装します。 このような情報には、次の情報が含まれます。
  
- ユーザーにアカウント ログオン ダイアログを表示する方法。    
- プロバイダーがソーシャル ネットワークに表示されるフレンドやアクティビティの表示をサポートするかどうか。    
- 連絡先カードまたはユーザー ウィンドウにフレンドやアクティビティOutlook表示する方法。     
- 連絡先カードまたはユーザー ウィンドウでフレンドやアクティビティの情報を更新する場合。
    
この情報は、通常、インターフェイス メソッドの出力パラメーターとして XML 文字列の形式でプロバイダーから OSC に渡されます。 OSC プロバイダーと OSC プロバイダーの両方が OSC プロバイダー XML スキーマに準拠しています。 したがって、インターフェイスを実装する過程で、XML スキーマで上記のように情報を指定する方法を理解する必要があります。 

次のリソースでは、プロバイダーの機能、友人、アクティビティに XML を指定する方法について説明します。
  
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)    
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)    
- [機能 XML の例](capabilities-xml-example.md)   
- [機能の XML](xml-for-capabilities.md)    
- [Friends XML の例](friends-xml-example.md)    
- [友人のための XML](xml-for-friends.md)   
- [アクティビティ フィード XML の例](activity-feed-xml-example.md)   
- [アクティビティの XML](xml-for-activities.md)
    
実装を開始する前に、デバッグ プロセスの後半で時間を節約するために、次のトピックも参照してください。
  
- [技術的な要件](technical-requirements.md)    
- [プロバイダーの開発に関するベスト プラクティス](best-practices-for-developing-a-provider.md)    
- [OSC サンプル テンプレート](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>手順 B: デバッグ

「 [プロバイダーのデバッグ」では、OSC](debugging-a-provider.md) プロバイダーの開発中に使用できるデバッグ手順について説明します。 
  
開発中は [、「OSC](getting-ready-to-release-an-osc-provider.md) プロバイダーをリリースする準備」を参照して、特定のシナリオ (基本認証やフォーム ベース認証など) で予期される動作をよりよく理解することもできます。 
  
## <a name="step-c-deploying"></a>手順 C: 展開

展開要件の詳細については、以下のトピックを参照してください。
  
- [プロバイダーの展開](deploying-a-provider.md)    
- [プロバイダーの登録](registering-a-provider.md)   
- [インストール チェックリスト](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>手順 D: リリース前の最終テスト

ソーシャル ネットワークと OSC プロバイダーに応じて、プロバイダーを解放する前に実行する必要があるプロバイダー固有のテストが通常行います。 テストの推奨リストについては [、「GETTING Ready to Release a OSC Provider 」を参照してください](getting-ready-to-release-an-osc-provider.md)。
  
## <a name="see-also"></a>関連項目

- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

