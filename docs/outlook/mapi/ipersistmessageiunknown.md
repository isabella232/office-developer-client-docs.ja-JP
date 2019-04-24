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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309605"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームビューアーがフォームのストレージを処理し、さまざまな状態を切り替えることができるようにします。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |メッセージオブジェクトを保持する  <br/> |
|実装元:  <br/> |フォーム オブジェクト  <br/> |
|呼び出し元:  <br/> |フォームビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IPersistMessage  <br/> |
|ポインターの種類:  <br/> |lppersistmessage  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |form オブジェクトの前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |フォームを管理できるフォームサーバーを表す識別子を返します。  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |前回の保存以降に加えられた変更について、フォームをチェックします。  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |新しいメッセージを初期化します。  <br/> |
|[Load](ipersistmessage-load.md) <br/> |指定したメッセージのフォームを読み込みます。  <br/> |
|[Save](ipersistmessage-save.md) <br/> |変更したフォームを、読み込みまたは作成されたメッセージに保存し直します。  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |保存操作が完了したことをフォームに通知します。  <br/> |
|[「soffmessage」](ipersistmessage-handsoffmessage.md) <br/> |フォームに現在のメッセージを解放させます。  <br/> |
   
## <a name="remarks"></a>解説

**IPersistMessage**インターフェイスを実装するには、すべてのフォームが必要です。 
  
 **IPersistMessage**は、OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx)インターフェイスと同じように動作します。 詳細については、 **IPersistStorage**メソッドを参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

