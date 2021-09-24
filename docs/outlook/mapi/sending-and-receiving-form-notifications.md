---
title: フォーム通知の送受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 57a4e4d1a39130e666b786f51c0ea48c7966c656
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550065"
---
# <a name="sending-and-receiving-form-notifications"></a>フォーム通知の送受信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム通知は、フォームからビューアー、およびビューアーからフォームへの両方の通信を容易にするために MAPI で使用されます。
  
フォームは、次のいずれかのイベントが発生すると、ビューアーに通知を送信します。
  
- フォームは閉じられています。
    
- 新しいメッセージがフォームに読み込まれます。
    
- 保存操作が完了しました。
    
- メッセージが送信されます。
    
これらの各イベントの種類は [、IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)、フォーム ビューアーが実装する必要があるインターフェイスの 1 つで、特定のメソッドに対応しています。 イベントが発生すると、フォームはビューアーのアドバイス シンクで対応する **IMAPIViewAdviseSink** メソッドを呼び出します。 たとえば、ビューアーが表示に含める必要がある新しいメッセージが届いた場合、フォームは [IMAPIViewAdviseSink::OnNewMessage メソッドを呼び出](imapiviewadvisesink-onnewmessage.md) します。 
  
ビューのアアドバイス シンクを、ビューアーに合った方法で実装します。標準実装はありません。 たとえば **、OnNewMessage** で、現在のフォルダーのコンテンツ テーブルのビューを更新して、新しく到着したメッセージを含めできます。 [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md)では、送信されたメッセージ イベントを受信するときに呼び出されるメソッドを、送信済みメッセージを送信済みアイテム フォルダーにコピーできます。
  
フォームは、フォームに影響を与える変更が発生し、新しいメッセージを読み込むときに、ビューアーから通知を受け取ります。 フォームに通知するには **、IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) または [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)のいずれかのメソッドを呼び出します。 状態 **を伝える OnChange** を呼び出します。 たとえば、新しいメッセージが届いたときにフォルダー内の最後のアイテムがフォームに表示されている場合は、VCSTATUS_NEXT フラグを設定して **OnChange** を呼び出して、フォームに次のアイテムが表示されたことを示します。 
  
**OnActivateNext** を呼び出して、表示できない可能性がある新しいメッセージがフォームに到着すると通知します。 メッセージのメッセージ クラスを **OnActivateNext に渡します**。 
  
クライアント アプリケーションへのフォーム オブジェクトによる通知は、クライアント アプリケーションの **IMAPIViewAdviseSink インターフェイスによって処理** されます。 詳細については [、「IMAPIViewAdviseSink : IUnknown 」を参照してください](imapiviewadvisesinkiunknown.md)。
  

