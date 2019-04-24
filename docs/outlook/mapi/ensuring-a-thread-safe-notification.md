---
title: スレッドセーフ通知の確認
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316594"
---
# <a name="ensuring-a-thread-safe-notification"></a>スレッドセーフ通知の確認

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントがマルチスレッドのプラットフォームで実行されている場合は、特定のスレッドで[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドが呼び出されることを保証する必要があります。 通常、 **onnotify**への呼び出しはすべてのスレッドで発生するため、予期しない不要なスレッドで通知を受信し、デバッグが困難なエラーが発生する可能性があります。 
  
通知呼び出しに使用したのと同じスレッドで、特定の通知に対する**onnotify**への呼び出し**** が行われることを保証するには、 **advise**を呼び出す前に[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出します。 * * * * HrThisThreadAdviseSink * * * * アドバイズシンクオブジェクトから新しいアドバイズシンクオブジェクトを作成します。 この新しいオブジェクトを**Advise**の呼び出しで渡します。 特定のスレッドのコンテキストの外部では動作しない可能性があるアドバイズシンクオブジェクトを持つすべてのクライアントは、 **HrThisThreadAdviseSink**で作成されたアドバイズシンクオブジェクトを常に登録する必要があります。
  

