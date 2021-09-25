---
title: 通知のタイミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 55bc73a914802e8b3d794348d0bc28c4cdbafda9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590934"
---
# <a name="timing-a-notification"></a>通知のタイミング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知は非同期プロセスなので、イベントが発生した直後ではなく、いつでも通知できます。
  
 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドへの呼び出しのタイミングは、アドバイス ソースを実装するサービス プロバイダーによって異なります。 サービス プロバイダーは、次のいずれかの方法でクライアントに通知できます。 
  
- イベントと同時に。
    
- イベントの直後。
    
- イベントに続く後の時点で、おそらく **Unadvise 呼び出しの後** 。 
    
ほとんどのサービス プロバイダーは、イベントを担当する MAPI メソッドが呼び出し元に戻った後に **OnNotify** を呼び出します。 たとえば、メッセージへの変更が保存された場合 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出し後、または **IUnknown::Release** 呼び出し後にメッセージが解放された場合に、メッセージに対する通知が送信されます。 通知が送信されるまで、メッセージ ストアに変更は表示されません。 
  
登録を取り消す **Unadvise** を呼び出した後、アドバイス ソースから通知を受信できます。 **Unadvise** の正常な呼び出しに従うのではなく、参照カウントが 0 に落ちた後にのみ、アドバイス シンクを解放してください。 **Unadvise** を呼び出したので、アアドバイス シンクは不要になったと仮定して下さい。 
  

