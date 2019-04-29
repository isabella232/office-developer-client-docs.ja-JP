---
title: MAPI フォーム通知
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418611"
---
# <a name="mapi-forms-notifications"></a>MAPI フォーム通知

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームオブジェクトからの通知の登録と処理は、他の MAPI オブジェクトの処理とは異なります。 フォーム通知のアドバイズシンクは、 **IMAPIAdviseSink**ではなく、 **IMAPIViewAdviseSink**または**IMAPIFormAdviseSink**のいずれかのインターフェイスを実装します。 [IMAPIViewAdviseSink: iunknown](imapiviewadvisesinkiunknown.md)および[IMAPIFormAdviseSink: iunknown](imapiformadvisesinkiunknown.md)には、複数のメソッドがあります。これには、対応するアドバイズソースが生成できるイベントのそれぞれについて1つのメソッドがあります。 たとえば、 **IMAPIFormAdviseSink**には次の2つのメソッドがあります。 [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md)を使用して、フォームビューアーの状態と[IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md)の変更を処理し、新しいメッセージを正しいフォームで表示します。 
  
フォームのイベント処理戦略は、OLE で実装されているイベント処理戦略に似ています。 クライアントは、ほとんどの MAPI オブジェクトの場合とは異なり、特定のイベントの種類に対して登録されません。 通知を登録すると、特定のアドバイズソースによって生成されるあらゆる種類のイベントを受け取ることが想定されます。 登録されているすべてのイベントを処理するには、 **IMAPIAdviseSink:: onnotify**を記述する必要があるため、これを実装するには、多数の異なるイベントに登録するクライアントにとっては複雑な場合があります。 form アドバイズシンクオブジェクトのメソッドは1つのイベントを対象としているため、これらのメソッドを実装する方が簡単です。 
  

