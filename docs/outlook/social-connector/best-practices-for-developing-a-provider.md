---
title: プロバイダーを開発するためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: Outlook ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、以下のプラクティスに従う必要があります。
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804327"
---
# <a name="best-practices-for-developing-a-provider"></a>プロバイダーを開発するためのベスト プラクティス

Outlook ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、以下のプラクティスに従う必要があります。
  
- セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、(ハイパー テキスト転送プロトコル (HTTP) をセキュリティで保護されたソケット レイヤー (SSL)) を HTTPS プロトコルを使用する必要があります。 それ以外の場合は、リスクそのメール アドレス、ソーシャル ネットワーク活動、およびその他のユーザーのデータを傍受または送信中に公開される可能性があります。
    
- OSC プロバイダーのサード パーティ製のソーシャル ネットワークを開発する場合、プロバイダーがサービスのソーシャル ネットワークの条項に従う必要があります。
    
- プロバイダーのダウンロード パッケージのサイズを最小限に抑えるには、C++ または COM コンポーネントを作成することができますが、他のツールなどのネイティブ コンパイラを使用してプロバイダーを構築します。
    
- 、プロバイダーでは、ソーシャル ネットワーク プロバイダーからの呼び出しを追跡するためにソーシャル ネットワークに送信される一意のユーザー エージェントを作成します。
    
- [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するのにはインターネット経由でソーシャル ネットワークを呼び出すことに依存させないでください。 など、ユーザーが Outlook をオフラインで起動します。OSC は、 **GetCapabilities**を呼び出して、ネットワークが接続されていない場合は、 **GetCapabilities**の呼び出しには、有効な XML**の機能**は返されません。 プロバイダーでリソースとして XML の**機能**を格納することをお勧めします。 
    
- OSC プロバイダーでは、ソーシャル ネットワークへの呼び出しの膨大な量を生成できます。 によって、ソーシャル ネットワークのサービスの条件によって、キャッシュ プロバイダーに OSC からと、さらに、ソーシャル ネットワーク プロバイダーからの呼び出しの数を減らすために、Outlook フォルダーに友人を検討します。
    
- Office 2013 は、32 ビットと 64 ビットの両方のバージョンで使用できます。 Office 2010 の前に Office のバージョンは、32 ビット バージョンでのみ使用します。 Office 2013 の 64 ビット Windows での既定のインストールは、32 ビットです。 64 ビットの Office 2013 がインストールされている OSC の 64 ビット バージョンをサポートする場合は、プロバイダーの 64 ビット バージョンをリリースする必要がありますもします。 
    
## <a name="see-also"></a>関連項目

- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)  
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)  
- [プロバイダーを展開します。](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

