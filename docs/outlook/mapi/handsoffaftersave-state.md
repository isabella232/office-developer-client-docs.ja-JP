---
title: 保存の状態を処理する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406606"
---
# <a name="handsoffaftersave-state"></a>保存の状態を処理する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[保存の状態を維持するのは、フォームの内容を永続的なストレージに保存するプロセスの一部です。 この状態では、フォームオブジェクトは、メッセージのプロパティの値のメモリ内コピーを変更しないようにする必要があります。これらの変更を保存する機会が他にはない可能性があるためです。 次の表では、保存の状態から許可される遷移について説明します。
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)(_pmessage! =_ NULL)  <br/> |埋め込みオブジェクトを開きます。 _pmessage_に格納されているメッセージのデータは、前の[IPersistMessage:: Save](ipersistmessage-save.md)呼び出しのメッセージと同じであることが保証されています。 **SaveCompleted**の呼び出しが成功した場合は、通常の状態を入力します。 それ以外の場合は、最後のエラーを E_OUTOFMEMORY に設定し、[保存の状態] のままにしておきます。  <br/> |[Normal](normal-state.md)または標準の保存  <br/> |
|**IPersistMessage:: SaveCompleted**(_pmessage = =_ NULL)  <br/> |最後のエラーを E_INVALIDARG または E_UNEXPECTED に設定します。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage:: IPersistMessage soffmessage](ipersistmessage-handsoffmessage.md)、 **Save**、または[:: InitNew](ipersistmessage-initnew.md) <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |form オブジェクトに対象のメッセージのデータを読み込みます。 この呼び出しは、フォームオブジェクトがフォルダー内の次または前のメッセージに送られるときに発生する可能性があります。  <br/> |標準  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |直前のエラーを返します。  <br/> |HandsOffAfterSave  <br/> |
|その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド  <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>関連項目



[フォームの状態](form-states.md)

