---
title: 通知のタイミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b4b0292ab16eabe30755fe84885a29fb8e3ce295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595196"
---
# <a name="timing-a-notification"></a>通知のタイミング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知は非同期処理であるため、通知が可能、いつでも必ずしもイベントが発生した後にすぐにします。
  
 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドの呼び出しのタイミングは、アドバイスのソースを実装するサービス プロバイダーによって異なります。 サービス プロバイダーか、クライアントに通知できます。 
  
- イベントと同時に。
    
- 直後のイベントです。
    
- ある後で時点で次のイベント可能性があります、 **Unadvise**の呼び出しの後です。 
    
ほとんどのサービス プロバイダーは、イベントを行う MAPI メソッドは、呼び出し元に返された後、 **OnNotify**を呼び出します。 などの**リ ス**を呼び出した後に、メッセージがリリースされたとき、またはメッセージへの変更を保存すると[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出しの後、メッセージの通知が送信されます。 通知が送信されるまで変更は表示されません、メッセージ ・ ストアにします。 
  
登録をキャンセルするのには**Unadvise**を呼び出した後、アドバイズ ソースから通知を受け取ることができます。 その参照カウントがゼロ、従わない**Unadvise**の正常な呼び出しにやられた後にのみ、アドバイズ シンクを解放することを確認します。 **Unadvise**を呼び出す必要があるため、アドバイズ シンクを必要がなくなったとは限りません。 
  

