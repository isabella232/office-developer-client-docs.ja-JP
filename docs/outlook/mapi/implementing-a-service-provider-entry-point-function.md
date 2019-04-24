---
title: サービスプロバイダーエントリポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332992"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>サービスプロバイダーエントリポイント関数の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのサービスプロバイダー DLL には、MAPI が呼び出しを読み込むためのエントリポイント関数があります。 このエントリポイント関数は[DllMain](https://msdn.microsoft.com/library/ms682583.aspx)と同じではないことに注意してください。 Win32 DLL エントリポイント関数です。
  
プロバイダーの種類によっては、プロバイダーのエントリポイント関数が異なるプロトタイプに準拠しています。 MAPI は、サービスプロバイダー用のさまざまなエントリポイント関数プロトタイプを定義します。
  
|**Provider**|**エントリポイント関数プロトタイプ**|
|:-----|:-----|
|メッセージストアプロバイダー  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|トランスポートプロバイダー  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|アドレス帳プロバイダー  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
これらのプロトタイプの機能の多くは、すべてのサービスプロバイダーの種類で同じです。 
  
アドレス帳、メッセージストア、およびトランスポートプロバイダーは、エントリポイント関数で次の2つの主要なタスクを実行します。
  
1. サービスプロバイダインターフェイス (SPI) のバージョンを調べて、MAPI がサービスプロバイダーが使用しているバージョンと互換性のあるバージョンを使用していることを確認します。 MAPI spi バージョンを含む_lpulMAPIVer_パラメーターと、SPI バージョンを含む_lアウト providerver_パラメーターを使用して、チェックを実行します。 これらのパラメーターは、次の3つの部分で構成される32ビットの符号なし整数です。 
    
  - ビット 24 ~ 31 は、メジャーバージョンを表します。
    
  - ビット 16 ~ 23 は、マイナーバージョンを表します。
    
  - ビット 0 ~ 15 は、更新識別子を表します。 メジャーバージョン番号はほとんど変更されませんが、MAPI が解放されて SPI が変更されるたびにマイナーバージョン番号が変更されます。 更新識別子は、Microsoft の内部ビルドバージョンです。これは、開発プロセス中の変更を追跡するために使用されます。 MAPI は、Mapispi ヘッダーファイルに記録されている CURRENT_SPI_VERSION 定数を定義して、現在の SPI バージョンを示します。 MAPI が使用しているバージョンより新しいバージョンの SPI を使用している場合は、エラー MAPI_E_VERSION でチェックに失敗します。
    
2. プロバイダオブジェクトのインスタンスを作成します。 プロバイダーは複数回開始および初期化される可能性があるため、この処理が行われるたびに新しいインスタンスを作成する必要があります。 1つ以上のクライアントによって同時に使用されている複数のプロファイルにプロバイダーが表示されている場合、または1つのプロファイル内に複数回表示されている場合は、プロバイダーが複数回開始されます。 エントリポイント関数のプロトタイプはプロバイダーの種類によって異なるため、プロバイダーオブジェクトの種類も異なります。 
    
    アドレス帳プロバイダーを記述している場合は、 [IABProvider: IUnknown](iabprovideriunknown.md)を実装します。 メッセージストアプロバイダーを記述している場合は、 [IMSProvider: IUnknown](imsprovideriunknown.md)を実装します。 詳細については、「[メッセージストアプロバイダーの読み込み](loading-message-store-providers.md)」を参照してください。
    
    トランスポートプロバイダーを記述している場合は、 [ixpprovider: IUnknown](ixpprovideriunknown.md)を実装します。 詳細については、「[トランスポートプロバイダーの初期化](initializing-the-transport-provider.md)」を参照してください。
    
## <a name="see-also"></a>関連項目



[サービスプロバイダーの開始](starting-a-service-provider.md)

