---
title: プロバイダー開発のためのベスト プラクティス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、次Outlookに従う必要があります。
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425919"
---
# <a name="best-practices-for-developing-a-provider"></a>プロバイダー開発のためのベスト プラクティス

ソーシャル コネクタ 2013 (OSC) プロバイダーを開発する場合は、次Outlookに従う必要があります。
  
- セキュリティ上の理由から、インターネット経由でサーバーと通信するプロバイダーは、HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) プロトコルを使用する必要があります。 それ以外の場合、転送中に電子メール アドレス、ソーシャル ネットワークアクティビティ、その他のユーザー データが傍受または公開されるリスクがあります。
    
- サードパーティのソーシャル ネットワーク用の OSC プロバイダーを開発する場合、プロバイダーはソーシャル ネットワークのサービス条件に従う必要があります。
    
- プロバイダーダウンロード パッケージのサイズを最小限に抑えるために、C++ などのネイティブ コンパイラや、COM コンポーネントを構築できるその他のツールを使用してプロバイダーをビルドします。
    
- プロバイダーで、ソーシャル ネットワークに送信される一意のユーザー エージェントを作成して、プロバイダーがソーシャル ネットワークに対して行った通話を追跡します。
    
- [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)メソッドは、プロバイダーの機能を取得するためにインターネットを通してソーシャル ネットワークを呼び出す方法に依存しない必要があります。 たとえば、ユーザーはオフラインでOutlookできます。OSC が **GetCapabilities** を呼び出し、ネットワーク接続がない場合 **、GetCapabilities** 呼び出しは有効な機能 XML **を返しません**。 ベスト プラクティスは、機能 XML **を** プロバイダーにリソースとして格納する方法です。 
    
- OSC プロバイダーは、ソーシャル ネットワークへの呼び出しを大幅に生成できます。 ソーシャル ネットワークのサービス条件に応じて、友人を Outlook フォルダーにキャッシュして、OSC からプロバイダーへの呼び出しの数を減らし、プロバイダーからソーシャル ネットワークに移動します。
    
- Office 2013 は、32 ビットバージョンと 64 ビット バージョンの両方で使用できます。 2010 Office以前Officeバージョンは、32 ビット バージョンでのみ使用できます。 64 ビット Office 2013 の既定のインストールWindows 32 ビットです。 64 ビット Office 2013 でインストールされている OSC の 64 ビット バージョンをサポートする場合は、64 ビット バージョンのプロバイダーもリリースする必要があります。 
    
## <a name="see-also"></a>関連項目

- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)  
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)  
- [プロバイダーの展開](deploying-a-provider.md)  
- [Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)](getting-started-with-developing-an-outlook-social-connector-provider.md)

