---
title: スレッドセーフオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310039"
---
# <a name="implementing-thread-safe-objects"></a>スレッドセーフオブジェクトの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターフェイスメソッドの呼び出しから直接取得されるオブジェクトの場合は、スレッドセーフを確実にするためにプロバイダーが責任を負っています。 コールバックオブジェクトを使用すると、クライアントアプリケーションの責任を負うことになります。
  
クライアントは、MAPI ユーティリティ[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すことによって、スレッドセーフな通知コールバックを実装できます。 **HrThisThreadAdviseSink**は、スレッドセーフでないアドバイズシンクをスレッドセーフなアドバイズシンクに変換します。 進行状況のコールバックの場合は、このようなユーティリティはありません。 クライアントは、MAPI スレッドセーフの進行状況オブジェクトを使用するか、手動で作成するかを選択できます。 
  
スレッドセーフオブジェクトは、スレッドに対応している場合もあります。 スレッド対応オブジェクトは、それを使用しているすべてのスレッドに対して個別のコンテキストを保持します。 スレッドセーフなオブジェクトでスレッドを認識する必要はありませんが、スレッドの認識をサポートすることは状況によっては役に立ちません。 2つの MAPI テーブルでは、定義によって常に独自のコンテキストが提供されます。 別のスレッドで使用される1つのテーブルは、一意のコンテキストを提供しません。
  
クライアントは、 **MAPIInitialize**呼び出しに使用したのと同じスレッドで通知を受信するか、**アドバイズ**呼び出しに使用されたものと同じスレッドで、または MAPI が所有する別のスレッドで通知を受信するかを選択できます。 **MAPIInitialize**の呼び出しに使用したのと同じスレッドに通知が配信されるようにするために、クライアントは[MAPIInitialize](mapiinitialize.md)を呼び出し、 [MAPIINIT_0](mapiinit_0.md)構造の**ulflags**メンバーに0を渡します。 通知は、メインメッセージループ中に配信されます。 
  
MAPI が所有するスレッドで通知を受信するために、クライアントは**MAPIINIT_0**構造体の**ulflags**メンバーを MAPI_MULTITHREAD_NOTIFICATIONS に設定して**MAPIInitialize**を呼び出します。 **アドバイズ**呼び出しは、ラップされたバージョンではなく、クライアントのアドバイズシンクオブジェクトで行われます。 
  
通知が**アドバイズ**に使用されたのと同じスレッドに到着するように、クライアントは[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出し、新しく作成されたラップアドバイズシンクを、元のアドバイズシンクではなく**アドバイズ**に渡します。 **MAPIInitialize**は、フラグの値を使用して呼び出すことができます。 
  

