---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396184"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのさまざまな状態間の遷移にストレージを処理するためにフォームのビューアーを使用できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |メッセージ オブジェクトを永続化します。  <br/> |
|実装元:  <br/> |フォーム オブジェクト  <br/> |
|呼び出し元:  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IPersistMessage  <br/> |
|ポインターの型。  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](ipersistmessage-getlasterror.md) <br/> |フォーム オブジェクトでは、前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |フォームを管理するフォームのサーバーを表す識別子を返します。  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |最後の保存以降に加えた変更のフォームをチェックします。  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |新しいメッセージを初期化します。  <br/> |
|[Load](ipersistmessage-load.md) <br/> |指定されたメッセージのフォームが読み込まれます。  <br/> |
|[Save](ipersistmessage-save.md) <br/> |変更後のフォームを元に読み込みまたは作成したメッセージに保存します。  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |フォームに通知する、保存操作が完了しました。  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |フォームの現在のメッセージを解放するが発生します。  <br/> |
   
## <a name="remarks"></a>備考

すべてのフォームは、 **IPersistMessage**インターフェイスを実装する必要があります。 
  
 **IPersistMessage**は、[すること](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)の OLE インターフェイスと同様に動作します。 詳細については、**すること**の方法を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

