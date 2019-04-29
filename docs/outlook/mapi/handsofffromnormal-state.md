---
title: 標準の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426472"
---
# <a name="handsofffromnormal-state"></a>標準の状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準の状態は、[標準として[保存](handsoffaftersave-state.md)する (標準)。 これは、フォームの内容を永続的なストレージに保存するプロセスの一部です。 この状態では、フォームオブジェクトは、メッセージのプロパティの値のメモリ内コピーを変更しないようにする必要があります。これらの変更を保存する機会が他にはない可能性があるためです。 次の表では、標準状態からの使用可能な移行について説明します。 
  
|IPersistMessage * * メソッド * *|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage! =_ NULL)  <br/> |メッセージオブジェクトのメッセージを_pmessage_に置き換えます。これは、前の呼び出しによって取り消されたメッセージの置換である[IPersistMessage::](ipersistmessage-handsoffmessage.md)[配布] [メッセージ] に置き換えられます。 新しいメッセージのデータは、失効したメッセージと同じであることが保証されます。 この呼び出しの後に、メッセージを clean としてマークしたり、 [IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)を呼び出すことができないようにする必要があります。 **SaveCompleted**の呼び出しが成功した場合は、[通常](normal-state.md)の状態を入力します。 それ以外の場合は、[標準] をそのままにします。  <br/> |通常または標準の標準  <br/> |
|**IPersistMessage:: SaveCompleted**(_pmessage = =_ NULL)  <br/> |最後のエラーを E_UNEXPECTED に設定します。  <br/> |HandsOffFromNormal  <br/> |
|**** [IPersistMessage:: Save](ipersistmessage-save.md)、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)、または[IPersistMessage:: Load](ipersistmessage-load.md)を実行します。 <br/> |最後のエラーを E_UNEXPECTED に設定します。  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |直前のエラーを返します。  <br/> |HandsOffFromNormal  <br/> |
|その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド  <br/> |最後のエラーを E_UNEXPECTED に設定します。  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

