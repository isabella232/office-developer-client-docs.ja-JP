---
title: MAPI クライアント オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb37c15e6544798a956e865e6c8c6d62bee44d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801342"
---
# <a name="mapi-client-objects"></a>MAPI クライアント オブジェクト
  
**適用対象**: Outlook 
  
メッセージング クライアント アプリケーションの標準的な実装の 1 つのオブジェクト、アドバイズ シンクします。 シンクの継承からのアドバイス、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェースおよび MAPI によってし、イベント通知のためのプロバイダーのサービスを提供します。 一部のクライアントでは、進行状況ダイアログ ボックスの表示をサポートするために進行中のオブジェクトも実装します。 
  
複雑なクライアントのサポートのユーザー設定フォームが別のアドバイスを実装するオブジェクトとメッセージ サイト オブジェクトから継承するなど、他のいくつかのオブジェクトのシンク、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インタ フェースとビュー コンテキスト オブジェクトから継承する、[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)インタ フェースです。 追加のアドバイズ シンク オブジェクトの継承、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インタ フェースです。 
  
次の表は、標準メッセージング クライアントとユーザー設定フォームの表示をサポートするクライアントによって実装される MAPI オブジェクトをまとめたものです。
  
|**クライアント オブジェクト**|**説明**|
|:-----|:-----|
|アドバイズ シンク  <br/> |メッセージ ・ ストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。  <br/> |
|メッセージ サイト  <br/> |フォーム オブジェクトの操作を処理します。  <br/> |
|Progress  <br/> |操作の進行状況を表示するダイアログ ボックスが表示されます。  <br/> |
|ビューのアドバイズ シンク  <br/> |フォームで発生するイベントのコールバック関数を提供します。  <br/> |
|ビュー コンテキスト  <br/> |印刷、フォームを保存し、フォーム間を移動するには、コマンドをサポートしています。  <br/> |
   
次の図は、これらのさまざまなクライアント オブジェクト、継承、インターフェイスおよびそれらを使用する MAPI コンポーネント間の関係を示します。 
  
![[クライアント オブジェクトおよび対応するインターフェイス](media/amapi_65.gif "[クライアント オブジェクトおよび対応するインターフェイス")
  
クライアントは、実装するよりも多くのより多くのオブジェクトを使用します。 すべてのクライアントは、さまざまなサービス ・ プロバイダーのオブジェクトや MAPI を実装するオブジェクトへのアクセスを得るために、セッション オブジェクトを使用します。 クライアントは、セッション、アドレス帳、または MAPI が提供する状態オブジェクトを介して間接的に、または特定のサービス プロバイダーを実装するオブジェクトのさまざまなを使用して直接のいずれかのサービス プロバイダーと対話します。 アドレス帳プロバイダーへの直接連絡をするためは、クライアントは、ユーザー、および配布リストのメッセージ、アドレス帳コンテナーで使用します。 メッセージ ストア プロバイダーにアクセスするのには、直接クライアントを使用してメッセージ ストアのオブジェクト、フォルダー、メッセージ、および添付ファイルです。 サービス プロバイダーは、状態オブジェクトをサポート、すると、クライアントはサービス プロバイダーの状態を監視するのに状態オブジェクトを使用できます。
  
サービス プロバイダーとサービスのメッセージの構成をサポートするクライアントが MAPI を実装する 3 つのオブジェクトを使用して: メッセージ サービスの管理オブジェクト、管理、および、プロバイダーの管理オブジェクトです。 カスタム フォームを表示するクライアントは、フォーム ライブラリのプロバイダーまたはフォーム サーバーを実装するいくつかのフォーム オブジェクトを使用します。
  
## <a name="see-also"></a>関連項目

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

