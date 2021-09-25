---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 48d5f054e53daa4594b06d5240f50ae403c359f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596210"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージに対するメッセージ サイトの機能に関する情報をメッセージ サイト オブジェクトから返します。
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>パラメーター

 _lpulStatus_
  
> [out]メッセージの状態に関する情報を提供するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
VCSTATUS_COPY 
  
> メッセージはコピーできます。 
    
VCSTATUS_DELETE 
  
> メッセージは削除できます。
    
VCSTATUS_DELETE_IS_MOVE 
  
> 削除されると、メッセージはメッセージ ストアからすぐに削除されるのではなく、メッセージ ストア内の削除済みアイテム フォルダーに移動されます。 
    
VCSTATUS_MOVE 
  
> メッセージは移動できます。
    
VCSTATUS_NEW_MESSAGE 
  
> 新しいメッセージを作成できます。
    
VCSTATUS_SAVE 
  
> メッセージを保存できます。
    
VCSTATUS_SUBMIT 
  
> メッセージは送信できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::GetSiteStatus** メソッドを呼び出して、現在のメッセージに対するメッセージ サイト オブジェクトの機能を取得します。 _lpulStatus_ パラメーターで返されるフラグは、メッセージ サイトに関する情報を提供します。 通常、フォームは、メッセージ サイトの実装の機能に関するフラグによって提供される情報に応じて、メニュー コマンドを有効または無効にします。 [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage::Load](ipersistmessage-load.md)メソッドによって新しいメッセージがフォームに読み込まれる場合は、状態フラグをチェックする必要があります。 一部のメッセージ サイト オブジェクト (特に読み取り専用オブジェクト) では、メッセージを保存または削除できません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IMAPIMessageSite::GetSiteStatus** メソッドでは、現在のメッセージに対して実行できる操作または実行できない操作を決定するために、クライアント アプリケーションが何らかの計算を実行する必要があります。 通常、現在のメッセージのメッセージ ストア プロバイダーの状態行を確認するか、ストア プロバイダーにクエリを実行して、メッセージ ストアを使用してクライアント アプリケーションが実行できるアクションを決定します。 たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを判断するには、メッセージ ストア オブジェクトの **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)プロパティを調して、メッセージ ストアに **Deleted Items** フォルダーが含されているかどうかを確認します。 
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI は **IMAPIMessageSite::GetSiteStatus** メソッドを使用して、指定されたサイトの状態を取得します。 このメソッドは、VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、またはVCSTATUS_SUBMIT。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[PidTagIpmWastebasketEntryId 標準プロパティ](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

