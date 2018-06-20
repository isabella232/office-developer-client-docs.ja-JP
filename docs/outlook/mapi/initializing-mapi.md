---
title: MAPI を初期化しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5f1dac712731175978bc639cc7296171448a41e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801087"
---
# <a name="initializing-mapi"></a>MAPI を初期化しています。

  
  
**適用されます**: Outlook 
  
MAPI ライブラリを使用するすべてのクライアント アプリケーションは**生じます**関数を呼び出す必要があります。 詳細については、[生じます](mapiinitialize.md)を参照してください。 **生じます**では、セッションのグローバル データを初期化し、呼び出しを受け入れるため、MAPI ライブラリを準備します。 いくつかの状況で設定するのには重要ないくつかのフラグがあります。 
  
- MAPI_NT_SERVICE
    
    クライアントが Windows サービスとして実装されている場合は、MAPI_NT_SERVICE フラグを設定します。 クライアントは Windows サービスであり、このフラグを設定しないで場合、MAPI が認識されず、サービスとして。 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    MAPI_MULTITHREAD_NOTIFICATIONS フラグは、MAPI 通知の管理方法に関連しています。 MAPI では、通知を生成するオブジェクトへの変更が発生したときに、ウィンドウ メッセージを受信する非表示のウィンドウを作成します。 ウィンドウ メッセージは、ある時点で、通知を送信して、適切な[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出せる原因で処理されます。 
    
- MAPI_NO_COINIT
    
    [CoInitialize](http://msdn.microsoft.com/en-us/library/ms886303.aspx)の呼び出しで COM を初期化するために**生じます**が試みないように、MAPI_NO_COINT フラグを設定します。 **MAPIINIT_0**構造体が渡された場合に**生じます** _ulFlags_ MAPI_NO_COINIT に設定すると、MAPI は、COM が既に初期化されてし、 **CoInitialize**の呼び出しを使用しないと見なされます。
    
MAPI が使用されていたスレッドに通知ウィンドウを作成する MAPI_MULTITHREAD_NOTIFICATIONS のフラグが渡されない場合に**生じます**の最初の呼び出しをします。 MAPI_MULTITHREAD_NOTIFICATIONS が渡された場合、MAPI が別のスレッドに通知ウィンドウを作成、通知の処理に専用のスレッドです。 MAPI では、通知を非表示のウィンドウを作成するために使用されるスレッドを受け取ります。 
  
- メッセージ ループがあります。
    
- セッションの有効期間全体にわたってブロックを解除されたままになります。
    
- クライアントによって作成された他のスレッドよりも長い有効期間があります。 
    
**生じます**の最初の呼び出しにフラグを設定することでスレッドを使用することができます。 通知を処理するために、スレッドの 1 つを許可する危険性は、スレッドが消える場合は、通知ウィンドウが破棄される、他のスレッドのいずれかに通知が送信される不要になったことです。 特別な処理は、非表示のウィンドウのメッセージ キューに投稿される通知メッセージのディスパッチを制御する必要な場合があります。 
  
通知を処理する別のウィンドウを使用する場合は、適切なスレッドに適切な時に通知が表示されることを保証します。 確認し、[通知] ウィンドウに転記される Windows メッセージを処理する特別なコードを使用する必要はありません。 
  
MAPI は、次の種類のクライアント アプリケーションが通知をサポートするための非表示のウィンドウを作成する別のスレッドを使用することを推奨します。
  
- マルチ スレッドのすべてのクライアントです。
    
- シングル スレッドの Windows サービスと Win32 コンソール アプリケーションをします。
    
- 通知に、メイン スレッドを使用する必要のないシングル スレッドのクライアントです。
    
別のスレッドのアプローチを使用するには、MAPI_MULTITHREAD_NOTIFICATIONS フラグを設定するすべてのスレッドで**生じます**を呼び出します。 
  
> [!NOTE]
> のみクライアントの最初の呼び出しに**生じます**が、通知をサポートするために作成される非表示のウィンドウ。 2 回目以降では、参照カウントをインクリメントする唯一の原因を呼び出します。 
  

