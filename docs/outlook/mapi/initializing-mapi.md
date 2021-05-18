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
  
MAPI ライブラリを使用するクライアント アプリケーションはすべて **、MAPIInitialize 関数を呼び出す必要** があります。 詳細については [、「MAPIInitialize」を参照してください](mapiinitialize.md)。 **MAPIInitialize は** 、セッションのグローバル データを初期化し、呼び出しを受け入れる MAPI ライブラリを準備します。 いくつかの状況で設定することが重要なフラグがいくつかある。 
  
- MAPI_NT_SERVICE
    
    クライアントが windows MAPI_NT_SERVICE実装されている場合は、このフラグを設定します。 クライアントが Windows サービスであり、このフラグを設定しない場合、MAPI はサービスとして認識できません。 
    
- MAPI_MULTITHREAD_NOTIFICATIONS
    
    [MAPI_MULTITHREAD_NOTIFICATIONS] フラグは、MAPI が通知を管理する方法に関連します。 MAPI は、通知を生成するオブジェクトに対する変更が発生すると、ウィンドウ メッセージを受信する非表示のウィンドウを作成します。 ウィンドウ メッセージは、ある時点で処理され、通知が送信され、適切な [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドが呼び出されます。 
    
- MAPI_NO_COINIT
    
    **MAPIInitialize** MAPI_NO_COINT呼び出しで COM を初期化しようとしないので、このフラグを [設定します](https://msdn.microsoft.com/library/ms886303.aspx)。 MAPIINIT_0構造体が **mapiInitialize** に渡され _、ulFlags_ が MAPI_NO_COINIT に設定されている場合、MAPI は COM が既に初期化済みと見なされ **、CoInitialize** への呼び出しをバイパスします。
    
このMAPI_MULTITHREAD_NOTIFICATIONSが渡されない場合、MAPI は最初の **MAPIInitialize** 呼び出しに使用されたスレッドに通知ウィンドウを作成します。 MAPI は、通知を処理するために専用のスレッドMAPI_MULTITHREAD_NOTIFICATIONS場合は、別のスレッドに通知ウィンドウを作成します。 MAPI では、非表示の通知ウィンドウの作成に使用されるスレッドが次の処理を行う必要があります。 
  
- メッセージ ループを設定します。
    
- セッションの一生を通してブロック解除されたままにします。
    
- クライアントによって作成された他のスレッドよりも長い有効期間を持つ。 
    
最初の **MAPIInitialize** 呼び出しでフラグを設定することで、使用するスレッドを選択できます。 スレッドの 1 つで通知を処理できる危険性は、スレッドが消えると、通知ウィンドウが破棄され、通知を他のスレッドに送信できなくなるという危険があります。 また、非表示ウィンドウのメッセージ キューに投稿される通知メッセージのディスパッチを制御するために、特別な処理が必要になる場合があります。 
  
別のウィンドウを使用して通知を処理する場合は、通知が適切なスレッドに適切な時刻に表示されます。 通知ウィンドウに投稿された Windows メッセージをチェックして処理する特別なコードは必要はありません。 
  
MAPI では、次の種類のクライアント アプリケーションが別のスレッドを使用して、通知サポート用の非表示ウィンドウを作成する必要があります。
  
- すべてのマルチスレッド クライアント。
    
- シングル スレッド Windows サービスと Win32 コンソール アプリケーション。
    
- 通知にメイン スレッドを使用する必要ないシングル スレッド クライアント。
    
個別のスレッド アプローチを使用するには、すべてのスレッドで **MAPIInitialize** を呼び出し、MAPI_MULTITHREAD_NOTIFICATIONSします。 
  
> [!NOTE]
> **MAPIInitialize** へのクライアントの最初の呼び出しのみ、通知をサポートするために非表示ウィンドウが作成されます。 それ以降の呼び出しでは、参照カウントが増分されるのみです。 
  

