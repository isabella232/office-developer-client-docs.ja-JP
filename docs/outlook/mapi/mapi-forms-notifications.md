---
title: MAPI 通知をフォームします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7064aee2ccd35b6b372bc6f911c7508113c26162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801380"
---
# <a name="mapi-forms-notifications"></a>MAPI 通知をフォームします。

  
  
**適用対象**: Outlook 
  
登録して、フォーム オブジェクトからの通知の処理は、その他の MAPI オブジェクトよりも別のプロセスです。 アドバイズ シンク フォームの通知の実装のいずれか**IMAPIAdviseSink**ではなく、 **IMAPIViewAdviseSink**または**IMAPIFormAdviseSink**のインタ フェースです。 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)と[IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md)複数のメソッドを持つそれぞれ、対応する、ソースを通知する可能性があるイベントごとに 1 つが生成できます。 たとえば、 **IMAPIFormAdviseSink**には 2 つの方法: フォーム ビューアーのステータスと正しいフォームで新しいメッセージを表示する[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)への変更を処理するために[IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) 。 
  
イベント処理フォームのための戦略では、OLE の実装戦略を処理するイベントに似ています。 クライアントは、ほとんどの MAPI オブジェクトのように特定のイベントの種類の登録は行いません。 前提とする通知を登録することができます任意の種類の特定のアドバイスのソースによって生成されるイベントを受信します。 **IMAPIAdviseSink::OnNotify**は、すべての登録されているイベントを処理するために記述する必要が、それを実装することがあります、多くのさまざまなイベントを登録するクライアントの複雑です。 フォーム内のメソッドは、シンク オブジェクトのターゲットを知らせるため、これらのメソッドを実装する 1 つのイベントが簡単です。 
  

