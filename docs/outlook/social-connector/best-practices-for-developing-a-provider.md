---
title: プロバイダー開発のためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: Outlook Social Connector 2013 (.osc) プロバイダーを開発するときは、以下の手順に従う必要があります。
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281238"
---
# <a name="best-practices-for-developing-a-provider"></a>プロバイダー開発のためのベスト プラクティス

Outlook Social Connector 2013 (.osc) プロバイダーを開発するときは、以下の手順に従う必要があります。
  
- セキュリティ上の理由から、インターネットを介してサーバーと通信するプロバイダーは HTTPS (ハイパーテキスト転送プロトコル (HTTP) with Secure Socket Layer (SSL) プロトコル) を使用する必要があります。 そうしないと、送信中に電子メールアドレス、ソーシャルネットワークアクティビティ、およびその他のユーザーデータが傍受または公開される危険性があります。
    
- サードパーティのソーシャルネットワーク用の .osc プロバイダーを開発している場合は、プロバイダーがソーシャルネットワークのサービス利用規約に準拠している必要があります。
    
- プロバイダーダウンロードパッケージのサイズを最小にするには、C++ などのネイティブコンパイラ、または COM コンポーネントを構築できる他のツールを使用して、プロバイダーを構築します。
    
- プロバイダーで、ソーシャルネットワークに送信される一意のユーザーエージェントを作成し、プロバイダーがソーシャルネットワークに対して行った呼び出しを追跡します。
    
- [imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するためにインターネット経由でソーシャルネットワークを呼び出すことに依存しないようにしてください。 たとえば、ユーザーは Outlook をオフラインで起動できます。.osc が**getcapabilities**を呼び出し、ネットワーク接続がない場合、 **getcapabilities**呼び出しは有効な**機能**XML を返しません。 ベストプラクティスとして、プロバイダーのリソースとして**機能**XML を格納することをお勧めします。 
    
- .osc プロバイダーは、ソーシャルネットワークへの大量の呼び出しを生成することができます。 ソーシャルネットワークのサービス条件によっては、友人を Outlook フォルダーにキャッシュして、.osc からプロバイダーへの呼び出し回数を減らし、プロバイダーからソーシャルネットワークに変換することを検討してください。
    
- Office 2013 は、32ビットと64ビットの両方のバージョンで利用できます。 office 2010 より前のバージョンの office は、32ビット版でのみ使用できます。 64ビット Windows 上の Office 2013 の既定のインストールは、32ビットです。 64ビットの Office 2013 でインストールされた64ビットバージョンの .osc をサポートする予定の場合は、プロバイダーの64ビットバージョンもリリースする必要があります。 
    
## <a name="see-also"></a>関連項目

- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)  
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)  
- [プロバイダーを展開する](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

