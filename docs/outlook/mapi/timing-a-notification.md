---
title: 通知のタイミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411149"
---
# <a name="timing-a-notification"></a>通知のタイミング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知は非同期プロセスなので、いつでもイベントが発生した直後に通知することはできません。
  
 [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドの呼び出しのタイミングは、アドバイズソースを実装するサービスプロバイダーによって異なります。 サービスプロバイダーは、クライアントに次のいずれかを通知できます。 
  
- イベントと同時に実行します。
    
- イベントの直後。
    
- 後で、**アドバイズ**中止呼び出しの後に、イベントをフォローすることがあります。 
    
ほとんどのサービスプロバイダーは、イベントを担当する MAPI メソッドが発信者に返された後に、 **onnotify**を呼び出します。 たとえば、メッセージに対する変更が保存されたとき、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しの後、またはメッセージが解放されたときに、 **IUnknown:: Release**呼び出しの後にメッセージの通知が送信されます。 通知が送信されるまで、メッセージストアに変更は表示されません。 
  
**アドバイズ**中止を呼び出して登録をキャンセルした後、アドバイズソースから通知を受け取ることができます。 アドバイズシンクは、その参照カウントが0に落ちた後にのみリリースし、**アドバイズ**中止の呼び出しが成功していないことを確認してください。 アドバイズシンクが不要になったため、**アドバイズ**中止を呼び出していることを前提としていません。 
  

