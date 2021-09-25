---
title: 通知のThread-Safeする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a0154e82227adc381b2e53cee47562be7ba3112b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601087"
---
# <a name="ensuring-a-thread-safe-notification"></a>通知のThread-Safeする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントがマルチスレッド プラットフォームで実行されている場合は [、IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドの呼び出しが特定のスレッドで発生することを保証する必要があります。 **OnNotify** の呼び出しは通常、任意のスレッドで発生する可能性があります。予期しないスレッドや不要なスレッドに関する通知を受け取り、デバッグが困難なエラーにつながる可能性があります。 
  
特定の通知に対する **OnNotify** の呼び出しが **、Advise** 呼び出しに使用されたのと同じスレッドで行われることを保証するには、Advise を呼び出す前に [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) を呼び出 **します**。 ** **HrThisThreadAdviseSink**** は、アドバイス シンク オブジェクトから新しいアアドバイス シンク オブジェクトを作成します。 この新しいオブジェクトを呼び出しで Advise に **渡します**。 特定のスレッドのコンテキスト外で動作しない可能性があるシンク オブジェクトをアドバイスするクライアントはすべて **、HrThisThreadAdviseSink** で作成されたアアドバイス シンク オブジェクトを常に登録する必要があります。
  

