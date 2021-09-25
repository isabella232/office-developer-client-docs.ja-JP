---
title: オブジェクトのThread-Safe実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf3b3e9dddaeb09a15ab658b6a6cd6d8447c4140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630545"
---
# <a name="implementing-thread-safe-objects"></a>オブジェクトのThread-Safe実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターフェイス メソッドから返されるオブジェクトが直接呼び出される場合、スレッドセーフを確保する責任はプロバイダーの責任です。 コールバック オブジェクトでは、クライアント アプリケーションの責任です。
  
クライアントは、MAPI ユーティリティ [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すことによって、スレッド セーフな通知コールバックを実装できます。 **HrThisThreadAdviseSink** は、スレッド セーフでないアドバイス シンクをスレッド セーフに変換します。 進行状況コールバックの場合、そのようなユーティリティはありません。 クライアントは、MAPI スレッド セーフの進行状況オブジェクトを使用するか、手動で作成することもできます。 
  
スレッド セーフ オブジェクトは、スレッドを認識する場合と認識しない場合があります。 スレッド対応オブジェクトは、使用しているスレッドごとに個別のコンテキストを維持します。 サービス プロバイダーは、スレッド セーフ オブジェクトでスレッド認識をサポートする必要はありません。ただし、スレッド認識のサポートは状況によっては役立ちます。 2 つの MAPI テーブルは、定義によって常に独自のコンテキストを提供します。 異なるスレッドで使用される 1 つのテーブルは、固有のコンテキストを提供する必要はありません。また、一意のコンテキストを提供する必要はありません。
  
クライアントは **、MAPIInitialize** 呼び出しに使用されたのと同じスレッド **、Advise** 呼び出しに使用されたスレッド、または MAPI が所有する別のスレッドで通知を受信する方法を選択できます。 **MAPIInitialize** の呼び出しに使用されたスレッドと同じスレッドに通知が確実に届くには、クライアントが [MAPIInitialize](mapiinitialize.md)を呼び出し、MAPIINIT_0 構造体の **ulFlags** メンバーで [0 を渡](mapiinit_0.md)します。 その後、メイン メッセージ ループ中に通知が配信されます。 
  
MAPI が所有するスレッドで通知を受信するには、クライアントが **MAPIInitialize** を呼び出し **、MAPIINIT_0** 構造体の **ulFlags** メンバーを MAPI_MULTITHREAD_NOTIFICATIONS に設定します。 **Advise 呼び** 出しは、ラップされたバージョンではなく、クライアントのアアドバイス シンク オブジェクトで行います。 
  
**通知** が、Advise を呼び出すのに使用されたスレッドと同じスレッドに確実に到着するために、クライアントは [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出し、新しく作成されたラップされたアアドバイス シンクを元のアアドバイス シンクではなく、アドバイスに渡します。 **MAPIInitialize は** 、いずれかのフラグ値で呼び出されます。 
  

