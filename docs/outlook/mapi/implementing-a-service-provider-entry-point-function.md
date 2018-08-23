---
title: サービス プロバイダー エントリ ポイント関数の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 40bbe110c7453cf2360fc103710fbc3bcb7f1c67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572054"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>サービス プロバイダー エントリ ポイント関数の実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
すべてのサービス プロバイダーの DLL には、それをロードするのには MAPI を呼び出す関数をポイントするエントリがあります。 このエントリ ポイント関数は[DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx)、Win32 DLL エントリ ポイント関数の場合と同様に注意します。
  
、プロバイダーの種類によって、プロバイダーのエントリ ポイント関数は、別のプロトタイプに準拠しています。 MAPI では、サービス プロバイダーの別のエントリ ポイント関数のプロトタイプを定義します。
  
|**Provider**|**エントリ ポイント関数のプロトタイプ**|
|:-----|:-----|
|メッセージ ストア プロバイダー  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|トランスポート プロバイダー  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|アドレス帳プロバイダー  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
これらのプロトタイプ内の機能の多くは、すべてのサービス プロバイダーの種類に対して同じです。 
  
アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、そのエントリ ポイント関数で次の 2 つの主要なタスクを実行します。
  
1. MAPI が、サービス ・ プロバイダーを使用しているバージョンと互換性のあるバージョンを使用していることを確認するサービス プロバイダー インターフェイス (SPI) のバージョンを確認してください。 チェックを実行するのにには、SPI の MAPI のバージョンが含まれています、 _lpulMAPIVer_のパラメーターと、SPI のバージョンが含まれています、 _lpulProviderVer_のパラメーターを使用します。 これらのパラメーターは、32 ビット符号なし整数の 3 つの部分で構成されています。 
    
  - ビット 24 ~ 31 では、メジャー バージョンを表します。
    
  - ビット 16 ~ 23 では、マイナー バージョンを表します。
    
  - ビット 0 から 15 までは、更新プログラムの識別子を表します。 メジャー バージョン番号が変更されたことはほとんどありませんが MAPI が解放され、SPI が変更されたときにマイナー バージョン番号の変更を。 更新プログラム識別子は、Microsoft の内部ビルドのバージョンです。開発プロセス中に変更を追跡するために使用されます。 MAPI CURRENT_SPI_VERSION 定数を定義する SPI の現在のバージョンを示すために、Mapispi.h ヘッダー ファイルに記載されています。 バージョンの MAPI を使用しているバージョンより新しい SPI を使用している場合は、MAPI_E_VERSION のエラー チェックを失敗します。
    
2. プロバイダー オブジェクトのインスタンスを作成します。 プロバイダーを起動し、複数回の初期化、ために、この現象が発生するたびに新しいインスタンスを作成する必要があります。 プロバイダーが複数回開始、1 つまたは複数のクライアントによって同時に使用されている複数のプロファイルに表示されるとき、または 1 つのプロファイルで複数回表示されます。 同様にエントリ ポイント関数のプロトタイプは、プロバイダーの種類によって異なる場合は、プロバイダー オブジェクトの型をも。 
    
    アドレス帳プロバイダーを作成している場合は、実装[IABProvider: IUnknown](iabprovideriunknown.md)。 メッセージ ストア プロバイダーを作成している場合は、実装[IMSProvider: IUnknown](imsprovideriunknown.md)。 詳細については、[メッセージ ストア プロバイダーの読み込み](loading-message-store-providers.md)を参照してください。
    
    トランスポート プロバイダーを作成している場合は、実装[IXPProvider: IUnknown](ixpprovideriunknown.md)。 詳細については、[トランスポート プロバイダーの初期化](initializing-the-transport-provider.md)を参照してください。
    
## <a name="see-also"></a>関連項目



[サービス プロバイダーの開始](starting-a-service-provider.md)

