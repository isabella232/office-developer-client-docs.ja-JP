---
title: サービス プロバイダーエントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4a315c0d3ec4ebb32cf337d7c10009c2736c67d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567320"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>サービス プロバイダーエントリ ポイント関数の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのサービス プロバイダー DLL には、MAPI が呼び出して読み込むエントリ ポイント関数があります。 このエントリ ポイント関数は [、Win32](https://msdn.microsoft.com/library/ms682583.aspx)DLL エントリ ポイント関数である DllMain と同じではありません。
  
プロバイダーの種類に応じて、プロバイダーエントリ ポイント関数は別のプロトタイプに準拠します。 MAPI では、サービス プロバイダー用に異なるエントリ ポイント関数プロトタイプを定義します。
  
|**Provider**|**エントリ ポイント関数のプロトタイプ**|
|:-----|:-----|
|メッセージ ストア プロバイダー  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|トランスポート プロバイダー  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|アドレス帳プロバイダー  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
これらのプロトタイプの機能の多くが、すべてのサービス プロバイダーの種類で同じです。 
  
アドレス帳、メッセージ ストア、およびトランスポート プロバイダーは、エントリ ポイント関数で次の 2 つの主要なタスクを実行します。
  
1. サービス プロバイダー インターフェイス (SPI) のバージョンを確認して、MAPI がサービス プロバイダーが使用しているバージョンと互換性のあるバージョンを使用している必要があります。 チェックを実行するには、MAPI SPI バージョンを含む  _lpulMAPIVer_ パラメーターと、SPI バージョンを含む  _lpulProviderVer_ パラメーターを使用します。 これらのパラメーターは、3 つの部分で構成される 32 ビット符号なし整数です。 
    
  - ビット 24 ~ 31 はメジャー バージョンを表します。
    
  - ビット 16 ~ 23 はマイナー バージョンを表します。
    
  - ビット 0 ~ 15 は更新識別子を表します。 メジャー バージョン番号はほとんど変更されませんが、MAPI がリリースされ、SPI が変更されるたびにマイナー バージョン番号が変更されます。 更新プログラムの識別子は、Microsoft の内部ビルド バージョンです。開発プロセス中の変更を追跡するために使用されます。 MAPI は、現在CURRENT_SPI_VERSION SPI バージョンを示すために Mapispi.h ヘッダー ファイルに記載されている定数を定義します。 MAPI が使用しているバージョンMAPI_E_VERSIONバージョンの SPI を使用している場合は、エラー メッセージを表示してチェックを失敗します。
    
2. プロバイダー オブジェクトのインスタンスを作成します。 プロバイダーを複数回開始および初期化することができますので、これが発生する度に新しいインスタンスを作成する必要があります。 プロバイダーは、1 つ以上のクライアントが同時に使用している複数のプロファイルに表示される場合、または 1 つのプロファイルに複数回表示される場合に複数回開始されます。 エントリ ポイント関数のプロトタイプがプロバイダーの種類によって異なるのと同様に、プロバイダー オブジェクトの種類も異なります。 
    
    アドレス帳プロバイダーを作成する場合は [、IABProvider : IUnknown を実装します](iabprovideriunknown.md)。 メッセージ ストア プロバイダーを作成する場合は [、IMSProvider : IUnknown を実装します](imsprovideriunknown.md)。 詳細については、「メッセージ ストア プロバイダー [の読み込み」を参照してください](loading-message-store-providers.md)。
    
    トランスポート プロバイダーを作成する場合は [、IXPProvider : IUnknown を実装します](ixpprovideriunknown.md)。 詳細については、「トランスポート プロバイダーの [初期化」を参照してください](initializing-the-transport-provider.md)。
    
## <a name="see-also"></a>関連項目



[サービス プロバイダーの開始](starting-a-service-provider.md)

