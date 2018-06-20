---
title: フォームの通知を送受信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4730fb04d530fce516fe1ca4fd572c58fc1f1ffa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803860"
---
# <a name="sending-and-receiving-form-notifications"></a>フォームの通知を送受信します。

  
  
**適用されます**: Outlook 
  
フォームの通知は、MAPI の両方のビューアーに、フォームとフォームに、ビューアーからの通信を容易にするために使用されます。
  
フォームは、次のイベントのいずれかが発生したとき、ビューアーに通知を送信します。
  
- フォームを閉じる。
    
- フォームでは、新しいメッセージが読み込まれます。
    
- セーブ ・ オペレーションが完了しました。
    
- メッセージを送信します。
    
内の特定のメソッドに対応している各タイプのイベント[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)をフォームのビューアーを実装しなければならないインタ フェースのいずれかです。 イベントが発生したとき、フォームの呼び出しが、ビューアーに対応する**IMAPIViewAdviseSink**メソッドには、シンクの案内です。 などのビューアーの表示に含めることは、新しいメッセージが到着したら、フォームは、 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出します。 
  
ビューのアドバイス、納得が、ビューアーのようにシンクの実装標準の実装はありません。 などの**OnNewMessage**では、新しく到着したメッセージを含むように現在のフォルダーの内容のテーブルのビューを更新できます。 [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md)を送信されたメッセージのイベントが発生したときに呼び出されるメソッドでは、送信済みアイテム フォルダーに送信されたメッセージをコピーできます。
  
フォームは、フォームに影響する変更が発生したときと、新しいメッセージをロードしている場合、ビューアーから通知を受け取ります。 フォームを通知するために**IMAPIFormAdviseSink**のメソッドのいずれかの呼び出し: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md)または[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)です。 ステータスを通信するためには、 **OnChange**を呼び出します。 たとえば、フォームが表示して最後の項目のフォルダーに新しいメッセージが到着したとき、ということは今すぐ次の項目に VCSTATUS_NEXT フラグを設定しての**OnChange**を呼び出します。 
  
フォームを新しいメッセージの到着を通知する**OnActivateNext**を呼び出すこと、できないことがあります表示できるようにします。 メッセージのメッセージ クラスを**OnActivateNext**に渡します。 
  
フォーム オブジェクトをクライアント アプリケーションでの通知は、クライアント アプリケーションの**IMAPIViewAdviseSink**のインターフェイスによって処理されます。 詳細についてを参照してください[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)。
  

