---
title: フォーム通知の送信と受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339712"
---
# <a name="sending-and-receiving-form-notifications"></a>フォーム通知の送信と受信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム通知は MAPI で使用され、フォームからビューアーへの通信や、ビューアーからフォームへの通信を容易にすることができます。
  
フォームは、次のいずれかのイベントが発生したときに、ビューアーに通知を送信します。
  
- フォームは閉じられています。
    
- 新しいメッセージがフォームに読み込まれます。
    
- 保存操作が完了しました。
    
- メッセージが送信されます。
    
これらの各イベントの種類は、IMAPIViewAdviseSink の特定のメソッドに対応します[。 IUnknown](imapiviewadvisesinkiunknown.md)は、フォームビューアーで実装する必要があるインターフェイスの1つです。 イベントが発生すると、フォームは、ビューアーのアドバイズシンクで対応する**IMAPIViewAdviseSink**メソッドを呼び出します。 たとえば、閲覧者が表示する必要がある新しいメッセージが到着すると、フォームは[IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出します。 
  
自分のビューアーに適した方法で、ビューのアドバイズシンクを実装します。標準の実装はありません。 たとえば、 **onnewmessage**では、現在のフォルダーの contents テーブルのビューを更新して、新しく到着したメッセージを含めることができます。 [IMAPIViewAdviseSink:: onsubmitted](imapiviewadvisesink-onsubmitted.md)で、送信されたメッセージイベントを受信したときに呼び出されるメソッド。送信されたメッセージを [送信済みアイテム] フォルダーにコピーすることができます。
  
フォームに影響を与える変更が発生したとき、および新しいメッセージを読み込むときに、フォームから通知が送信されます。 フォームに通知するには、 **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md)または[IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md)のいずれかのメソッドを呼び出します。 状態を伝達するために、 **OnChange**を呼び出します。 たとえば、新しいメッセージが到着したときに、フォルダーの最後のアイテムがフォームに表示されている場合は、VCSTATUS_NEXT フラグを設定して**OnChange**を呼び出し、次のアイテムがあることを示します。 
  
**OnActivateNext**を呼び出して、新しいメッセージの到着をフォームに通知します。これは、表示することができない場合があります。 メッセージのメッセージクラスを**OnActivateNext**に渡します。 
  
クライアントアプリケーションへの form オブジェクトによる通知は、クライアントアプリケーションの**IMAPIViewAdviseSink**インターフェイスによって処理されます。 詳細については、「 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)」を参照してください。
  

