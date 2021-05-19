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
  
フォーム オブジェクトからの通知の登録と処理は、他の MAPI オブジェクトとは異なるプロセスです。 フォーム通知のシンクに対するアドバイスは **、IMAPIAdviseSink** インターフェイスまたは **IMAPIFormAdviseSink** インターフェイスを **IMAPIAdviseSink** インターフェイスではなく実装します。 [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) および [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) には、対応するアアドバイス ソースが生成できる可能性のあるイベントごとに 1 つ、複数のメソッドがあります。 たとえば **、IMAPIFormAdviseSink** には、フォーム ビューアーの状態の変更を処理する [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) と、正しいフォームで新しいメッセージを表示する [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) の 2 つのメソッドがあります。 
  
フォームのイベント処理戦略は、OLE で実装されたイベント処理戦略に似ています。 クライアントは、ほとんどの MAPI オブジェクトの場合と同様に、特定のイベントの種類に登録しません。 通知に登録すると、特定のアドバイス ソースによって生成できる任意の種類のイベントを受信できるという前提があります。 すべての登録済みイベントを処理するために **IMAPIAdviseSink::OnNotify** を記述する必要があります。 フォーム内のメソッドはシンク オブジェクトが 1 つのイベントを対象とするとアドバイスしますので、これらのメソッドを実装する方が簡単です。 
  

