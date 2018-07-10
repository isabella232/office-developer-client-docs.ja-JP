---
title: MAPI サービス プロバイダー オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 505b27b469a4ab197b41058ea5b933608818f0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801444"
---
# <a name="mapi-service-provider-objects"></a>MAPI サービス プロバイダー オブジェクト

  
  
**適用されます**: Outlook 
  
サービス プロバイダーは、多くのオブジェクトを実装します。 MAPI によって主に使用される、いくつかと、クライアント アプリケーションによって使用されます。 サービス ・ プロバイダーのすべての種類によって、いくつかのオブジェクトの実装します。残りの部分は、1 つのプロバイダーの種類に固有です。 次の表では、すべてのサービス プロバイダー オブジェクトについて説明します。
  
|**サービス プロバイダー オブジェクト**|**説明**|
|:-----|:-----|
|アドレス帳コンテナー  <br/> |アクティブなプロファイルに 1 つのアドレス帳プロバイダーに受信者の情報が含まれていますアドレス帳プロバイダーは、1 つまたは複数のアドレス帳コンテナーを持つことができます。  <br/> |
|Attachment  <br/> |ファイルまたはメッセージに関連する、OLE オブジェクトなどの追加データが含まれています。  <br/> |
|コントロール  <br/> |またはボタンを無効にでき、ボタンがクリックされたときの処理を開始します。  <br/> |
|配布リスト  <br/> |個々 のメッセージの受信者のグループ化をについて説明します。  <br/> |
|Folder  <br/> |メッセージおよびその他のメッセージのコンテナーが含まれています。  <br/> |
|ログオン  <br/> |ハンドルは、プロバイダーのイベントの通知とクライアントの要求をサービスします。  <br/> |
|メッセージング ユーザー  <br/> |メッセージの各受信者をについて説明します。  <br/> |
|Message  <br/> |1 つまたは複数の受信者に送信できる情報が含まれています。  <br/> |
|メッセージ ・ ストア  <br/> |メッセージの階層構造のデータベースとして機能します。  <br/> |
|プロバイダー  <br/> |ハンドルはサービス プロバイダーの起動とシャット ダウンします。  <br/> |
|スプーラーのフック  <br/> |受信および送信メッセージに対して特別な処理を実行します。  <br/> |
|Status  <br/> |サービス プロバイダーの状態へのアクセスを提供します。  <br/> |
|テーブル  <br/> |行と列の形式でデータベース テーブルのようなオブジェクトのデータの概要ビューへのアクセスを提供します。  <br/> |
   
すべてのサービス プロバイダーは、プロバイダーのオブジェクトとログオン オブジェクトを実装します。 プロバイダー オブジェクトは厳密に管理します。スタートアップおよびシャット ダウンの処理を制御するのには MAPI によって使用されます。 ログオン オブジェクト サービスを提供しないクライアント要求をいくつか直接。 たとえば、メッセージは、プロバイダーのログオン オブジェクト ハンドル通知の登録とメッセージ ストアのオブジェクトを開く要求を格納します。 
  
プロバイダーおよびログオン オブジェクトでは、実装を提供するサービス プロバイダーの種類によって異なるインターフェイスを実装します。 メッセージ ストア プロバイダーを実装して、 [IMSProvider: IUnknown](imsprovideriunknown.md)と[IMSLogon: IUnknown](imslogoniunknown.md)インターフェイスは、プロバイダーおよびログオン オブジェクトは、アドレスがプロバイダーの実装を予約、 [IABProvider: IUnknown](iabprovideriunknown.md)と[IABLogon: IUnknown](iablogoniunknown.md)インターフェイス、およびトランスポート プロバイダーを実装して、 [IXPProvider: IUnknown](ixpprovideriunknown.md)と[IXPLogon: IUnknown](ixplogoniunknown.md)インタ フェースです。 
  
メッセージ フック プロバイダーでは、スプーラーのフックのオブジェクト、または受信メッセージと送信メッセージにフィルターを適用するオブジェクトを実装します。
  
サービス プロバイダーは、通常、いくつかのオブジェクトのみを使用します。 最も頻繁に、MAPI は、クライアントの要求を助けるために提供するサポート オブジェクトを使用します。 サポート オブジェクトは、それを使用するプロバイダーの種類をカスタマイズします。 すべてのサービス プロバイダーのサポート オブジェクトには、イベント通知の処理、構成のプロパティ、オブジェクトのオープン、およびエラー処理を表示するためのメソッドが含まれています。 メソッドの残りの部分は特定の使用です。アドレス帳、メッセージ ストア、およびトランスポート プロバイダー、および構成をサポートするためのカスタマイズされたバージョンがあります。 たとえば、アドレス帳のサポート オブジェクトには、詳細およびカスタム受信者ダイアログ ボックスが表示されます。 メッセージ ・ ストアでは、オブジェクトのサポートのコピーをサポートし、フォルダーとメッセージの操作を移動します。 トランスポート プロバイダーのサポートのオブジェクトには、MAPI スプーラーとの対話を促進するためのメソッドが含まれています。 
  
サービス プロバイダーによっては、テーブルのデータとプロパティのデータ オブジェクトを使用して、MAPI が実装しているユーティリティ オブジェクトです。 テーブルのデータ オブジェクトは、基になるテーブルのデータを管理するサービス プロバイダーを有効にします。 データ オブジェクトのプロパティは、オブジェクトとプロパティのアクセスを設定するのにはサービス ・ プロバイダーを有効にします。 
  
プロパティを転送するためにトランスポート ニュートラル カプセル化形式 (TNEF) をサポートするトランスポート プロバイダーは、MAPI をサポートするために実装する TNEF オブジェクトを使用して、 [ITnef: IUnknown](itnefiunknown.md)インタ フェースです。 詳細については、 [TNEF-Enabled トランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[ITnef: IUnknown](itnefiunknown.md)
  
[IMSProvider: IUnknown](imsprovideriunknown.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)
  
[IABProvider: IUnknown](iabprovideriunknown.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)
  
[IXPProvider: IUnknown](ixpprovideriunknown.md)
  
[IXPLogon: IUnknown](ixplogoniunknown.md)


[TNEF を有効にしたトランスポート プロバイダーの開発](developing-a-tnef-enabled-transport-provider.md)
