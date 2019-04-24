---
title: メッセージ受信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356946"
---
# <a name="message-reception-model"></a>メッセージ受信モデル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーは、mapi スプーラーが受信メール用にそれをポーリングする必要があるか、または新しいメールが到着したときに mapi スプーラーへのコールバックを実行するかどうかを制御します。 トランスポートプロバイダーは、 [ixpprovider:: transportlogon](ixpprovider-transportlogon.md)からポーリング要求に戻るときに、SP_LOGON_POLL フラグを設定します。 それ以外の場合、トランスポートプロバイダーは、受信メールが使用可能な場合は[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)を使用します。 受信メールが利用可能であることを学習した後、MAPI スプーラーは新しいメッセージを開き、トランスポートプロバイダーに、受信したメッセージのプロパティをメッセージに保存するよう要求します。 
  
このプロセスは次のように動作します。
  
1. 使用可能なメッセージは、 **imapisupport:: SpoolerNotify**を呼び出すトランスポートプロバイダー、または[IXPLogon::P oll](ixplogon-poll.md)の MAPI スプーラーのいずれかによって示されます。
    
2. MAPI スプーラーは[IXPLogon:: startmessage](ixplogon-startmessage.md)を呼び出してプロセスを開始します。 
    
3. トランスポートプロバイダーは、 **startmessage**で参照される場所に参照値を配置します。 これらの参照値を使用すると、トランスポートプロバイダーと MAPI スプーラーは、配信するメッセージが複数ある場合にどのメッセージが処理されているかを追跡できます。
    
4. トランスポートプロバイダーは、渡された[IMessage: imapiprop](imessageimapiprop.md)インスタンスにメッセージデータを格納します。 
    
5. トランスポートプロバイダーは、 **IMessage**インスタンスに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出し、 **startmessage**から値を返します。
    
6. MAPI スプーラーは、メッセージ配信を停止する必要がある場合に[IXPLogon:: transportnotify](ixplogon-transportnotify.md)を呼び出します。 
    
> [!NOTE]
> トランスポートプロバイダーが大量のメッセージを配信する必要があり、トランスポートプロバイダーが**imapisupport::** oll ではなく SpoolerNotify を使用している場合は、 **IXPLogon::P**ではなく、 **SpoolerNotify**を呼び出さないように注意する必要があります。deprive の他のトランスポートプロバイダーを CPU 時間で提供します。 MAPI スプーラーには、この問題を回避するロジックがありますが、一般的には、 **SpoolerNotify**の呼び出し間隔は、トランスポートプロバイダーが1つのメッセージを処理するのにかかる時間より長くする必要があります。 > また、MAPI スプーラーで受信メッセージがすぐに処理されない場合もあります。 MAPI スプーラーは、受信メッセージを受信する前に、トランスポートプロバイダーに他のタスクを実行するように要求することができます。 
  

