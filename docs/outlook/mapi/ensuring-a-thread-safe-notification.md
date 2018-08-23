---
title: スレッド セーフ通知の確認
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800004"
---
# <a name="ensuring-a-thread-safe-notification"></a>スレッド セーフ通知の確認

  
  
**適用対象**: Outlook 
  
クライアントは、マルチ スレッドのプラットフォームで実行している場合は、特定のスレッドで、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドの呼び出しが発生することを保証する必要があります。 **OnNotify**への呼び出しは、任意のスレッドで発生することが通常、ために、エラーの原因をデバッグするが難しいことと、予期しない、望ましくないスレッドで通知を受信することができます。 
  
**アドバイズ**するために使用されたのと同じスレッドで呼び出し、**アドバイズ**を呼び出す前に[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出して、 **OnNotify**に特定の通知のための呼び出しが行われていることを保証します。 * * * * HrThisThreadAdviseSink。 アドバイズ シンク オブジェクトから新しいアドバイズ シンク オブジェクトを作成します。 **Advise**への呼び出しでは、この新しいオブジェクトを渡します。 アドバイズ シンクが動作しない可能性の特定のスレッドのコンテキストの外部のオブジェクトは常に登録する必要がありますが、すべてのクライアントは、 **HrThisThreadAdviseSink**で作成したシンク オブジェクトを案内します。
  

