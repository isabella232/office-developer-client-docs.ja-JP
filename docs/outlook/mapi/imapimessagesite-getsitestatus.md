---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430127"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージのメッセージサイトの機能に関する情報をメッセージサイトオブジェクトから返します。
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>パラメーター

 _lアウト状態_
  
> 読み上げメッセージの状態に関する情報を提供するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
VCSTATUS_COPY 
  
> メッセージをコピーできます。 
    
VCSTATUS_DELETE 
  
> メッセージを削除できます。
    
VCSTATUS_DELETE_IS_MOVE 
  
> 削除されると、メッセージはメッセージストアからすぐに削除されるのではなく、メッセージストア内の**削除済みアイテム**フォルダーに移動されます。 
    
VCSTATUS_MOVE 
  
> メッセージを移動できます。
    
VCSTATUS_NEW_MESSAGE 
  
> 新しいメッセージを作成できます。
    
VCSTATUS_SAVE 
  
> メッセージを保存できます。
    
VCSTATUS_SUBMIT 
  
> メッセージを送信できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

Form オブジェクトは**IMAPIMessageSite:: getsitestatus**メソッドを呼び出して、現在のメッセージのメッセージサイトオブジェクトの機能を取得します。 _lアウト status_パラメーターで返されるフラグは、メッセージサイトに関する情報を提供します。 通常、フォームは、フラグがメッセージサイト実装の機能について提供する情報に応じて、メニューコマンドを有効または無効にします。 [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage:: Load](ipersistmessage-load.md)メソッドによってフォームに新しいメッセージが読み込まれた場合は、状態フラグをチェックする必要があります。 一部のメッセージサイトオブジェクト (特に読み取り専用オブジェクト) では、メッセージを保存または削除することはできません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IMAPIMessageSite:: getsitestatus**メソッドでは、現在のメッセージに対して実行可能な操作と実行できない操作を決定するために、クライアントアプリケーションが計算を実行することが必要になる場合があります。 通常は、現在のメッセージのメッセージストアプロバイダーの状態行を参照するか、ストアプロバイダーに照会して、メッセージストアを使用してクライアントアプリケーションが実行できるアクションを確認します。 たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを判断するには、メッセージストアオブジェクトの**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) プロパティを調べて、**削除済みアイテム**フォルダーがあるかどうかを確認します。メッセージストア。 
  
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: getsitestatus  <br/> |mfcmapi は、 **IMAPIMessageSite:: getsitestatus**メソッドを使用して、指定されたサイトの状態を取得します。 VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、または VCSTATUS_SUBMIT を返すことができます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[PidTagIpmWastebasketEntryId 標準プロパティ](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

