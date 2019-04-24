---
title: imapiform IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321778"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームビューアーがフォームビューのコンテキストとフォームの通知を操作したり、フォームの動詞を実行したり、フォームをシャットダウンしたりできるようにします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |フォーム オブジェクト  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォームビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIForm  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[setviewcontext](imapiform-setviewcontext.md) <br/> |フォームのビューコンテキストを確立します。  <br/> |
|[getviewcontext](imapiform-getviewcontext.md) <br/> |フォームの現在のビューコンテキストを返します。  <br/> |
|[shutdownform](imapiform-shutdownform.md) <br/> |フォームを閉じます。  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |フォームが特定の動詞に関連付けられている任意のタスクを実行するよう要求します。  <br/> |
|[助言](imapiform-advise.md) <br/> |フォームに影響を与えるイベントに関する通知に対してフォームビューアーを登録します。  <br/> |
|[アドバイズ](imapiform-unadvise.md) <br/> |以前に呼び出し先の**アドバイズ**によって設定されたフォームビューアーでの通知の登録を取り消します。  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |form オブジェクトの前に発生したエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

