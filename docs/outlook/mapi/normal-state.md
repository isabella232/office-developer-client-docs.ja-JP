---
title: 通常の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335744"
---
# <a name="normal-state"></a>通常の状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常の状態とは、フォームオブジェクトが最も多くの時間を費やしている場所で、クライアントアプリケーションが変更を保存したり、フォームを閉じたりするなどの操作を開始するのを待機します。 次の表は、通常の状態から許可される遷移を示しています。
  
|**IPersistMessage メソッド**|**Action**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage:: 保存](ipersistmessage-save.md)(_pmessage = =_ NULL、 _fsameasload = =_ TRUE)  <br/> または  <br/> **IPersistMessage:: 保存**(_pmessage! =_ NULL、 _fsameasload = =_ FALSE)  <br/> |変更されたすべての埋め込み OLE オブジェクトを、再帰的に保存します。 メッセージのデータをメッセージオブジェクトに保存します。 今後使用するために_fsameasload_フラグを[noscribble](noscribble-state.md)状態で保存します。  <br/> |NoScribble  <br/> |
|**IPersistMessage:: 保存**(_pmessage! =_ NULL、 _fsameasload = =_ TRUE)  <br/> |これは前の例と同じですが、この**Save**呼び出しはメモリが不足している状況では使用されていますが、メモリ不足の場合は失敗しません。  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |埋め込まれ**** たメッセージに対して、または ole [IPersistStorage:: 配布用](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx)の ole オブジェクトに対して、配布のために、このメソッドを再帰的に呼び出します。 メッセージオブジェクトおよび埋め込まれたメッセージまたはオブジェクトを解放します。  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)または[IPersistMessage:: Load](ipersistmessage-load.md) <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |標準  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |直前のエラーを返します。  <br/> |標準  <br/> |
|その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド  <br/> |[IPersistMessage: IUnknown](ipersistmessageiunknown.md)インターフェイスのドキュメントで説明されているとおりに実装します。  <br/> |標準  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

