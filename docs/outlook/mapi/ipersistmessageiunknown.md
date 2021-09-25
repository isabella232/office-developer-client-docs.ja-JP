---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e95a52056f8ad9936e8071176fc2bd55e16acfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587917"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーがフォームの格納を処理し、さまざまな状態間を切り替えできます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ オブジェクトの永続化  <br/> |
|実装元:  <br/> |フォーム オブジェクト  <br/> |
|呼び出し元:  <br/> |フォーム ビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IPersistMessage  <br/> |
|ポインターの種類:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |フォーム オブジェクトの前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |フォームを管理できるフォーム サーバーを表す識別子を返します。  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |フォームで、前回の保存以降に行われた変更を確認します。  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |新しいメッセージを初期化します。  <br/> |
|[Load](ipersistmessage-load.md) <br/> |指定したメッセージのフォームを読み込む。  <br/> |
|[Save](ipersistmessage-save.md) <br/> |変更されたフォームを、読み込まれたメッセージまたは作成されたメッセージに保存します。  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |保存操作が完了したフォームに通知します。  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |フォームが現在のメッセージを解放します。  <br/> |
   
## <a name="remarks"></a>注釈

**IPersistMessage インターフェイスを実装するには、すべてのフォームが必要** です。 
  
 **IPersistMessage** は、OLE [IPersistStorage インターフェイスと同様に動作](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) します。 詳細については **、「IPersistStorage メソッド」を** 参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

