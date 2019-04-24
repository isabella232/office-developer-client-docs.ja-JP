---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350919"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を処理するためのアドバイズシンクオブジェクトを実装します。 アドバイズシンクオブジェクトへのポインターは、サービスプロバイダーの**アドバイズ**メソッドへの呼び出しで渡されます。通知の登録に使用されるメカニズムです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |アドバイズシンクオブジェクト  <br/> |
|実装元:  <br/> |クライアントアプリケーションと MAPI  <br/> |
|呼び出し元:  <br/> |サービスプロバイダーと MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[onnotify](imapiadvisesink-onnotify.md) <br/> |1つまたは複数のタスクを実行して通知に応答します。 実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

