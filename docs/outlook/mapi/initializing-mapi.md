---
title: MAPI の初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309731"
---
# <a name="initializing-mapi"></a>MAPI の初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ライブラリを使用するすべてのクライアントアプリケーションは、 **MAPIInitialize**関数を呼び出す必要があります。 詳細については、「 [MAPIInitialize](mapiinitialize.md)」を参照してください。 **MAPIInitialize**は、セッションのグローバルデータを初期化し、呼び出しを受け入れるように MAPI ライブラリを準備します。 状況によっては、次のようないくつかのフラグが設定されている場合があります。 
  
- MAPI_NT_SERVICE
    
    クライアントが Windows サービスとして実装されている場合は、MAPI_NT_SERVICE フラグを設定します。 クライアントが Windows サービスで、このフラグが設定されていない場合、MAPI はサービスとして認識しません。 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    MAPI_MULTITHREAD_NOTIFICATIONS フラグは、MAPI が通知を管理する方法に関連しています。 MAPI は、通知を生成するオブジェクトに変更が発生したときにウィンドウメッセージを受信する非表示のウィンドウを作成します。 ウィンドウメッセージは何らかの時点で処理され、通知が送信され、適切な[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドが呼び出されます。 
    
- MAPI_NO_COINIT
    
    MAPI_NO_COINT フラグを設定して、 **MAPIInitialize**が[CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx)の呼び出しで COM を初期化しないようにします。 _ulflags_が MAPI_NO_COINIT に設定されている場合、 **MAPIINIT_0**構造体が**MAPIInitialize**に渡されると、MAPI は COM が既に初期化されていると見なし、 **CoInitialize**への呼び出しをバイパスします。
    
MAPI_MULTITHREAD_NOTIFICATIONS フラグが渡されない場合、MAPI は最初の**MAPIInitialize**呼び出しで使用されたスレッドに通知ウィンドウを作成します。 MAPI_MULTITHREAD_NOTIFICATIONS が渡されると、通知の処理専用のスレッドが生成されると、MAPI は別のスレッドで通知ウィンドウを作成します。 MAPI では、非表示の通知ウィンドウを作成するために使用されているスレッドが次のことを前提としています。 
  
- メッセージループがあります。
    
- セッションが終了するまで、ブロックされないままになります。
    
- クライアントによって作成された他のスレッドよりも長い有効期間がある。 
    
最初の**MAPIInitialize**呼び出しでフラグを設定することによって、どのスレッドを使用するかを選択できます。 スレッドの1つが通知を処理できるようにする危険性は、スレッドが表示されなくなると、通知ウィンドウが破棄され、他のスレッドに通知を送信できなくなることです。 また、非表示のウィンドウのメッセージキューにポストされる通知メッセージのディスパッチを制御するために、特別な処理が必要になることがあります。 
  
別のウィンドウを使用して通知を処理する場合は、適切なスレッドの適切なタイミングで通知が表示されることを確認してください。 通知ウィンドウにポストされた Windows メッセージを確認して処理するための特別なコードは必要ありません。 
  
MAPI では、次の種類のクライアントアプリケーションが別のスレッドを使用して通知をサポートする非表示のウィンドウを作成することをお勧めします。
  
- すべてのマルチスレッドクライアント。
    
- シングルスレッド Windows サービスおよび Win32 コンソールアプリケーション。
    
- 通知にメインスレッドを使用する必要がない、シングルスレッドクライアント。
    
個別のスレッドアプローチを使用するには、すべてのスレッドで**MAPIInitialize**を呼び出し、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定します。 
  
> [!NOTE]
> クライアントの最初の**MAPIInitialize**への呼び出しでは、通知をサポートする非表示のウィンドウが作成されます。 以降の呼び出しでは、参照カウントがインクリメントされます。 
  

