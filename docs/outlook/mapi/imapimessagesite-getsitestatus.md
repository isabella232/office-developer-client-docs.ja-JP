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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800592"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**適用されます**: Outlook 
  
メッセージに関するメッセージのサイト オブジェクトの現在のメッセージのサイトの機能に対応する情報を返します。
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [out]フラグのビットマスクであり、メッセージの状態に関する情報を提供へのポインター。 次のフラグを設定することができます。
    
VCSTATUS_COPY 
  
> メッセージをコピーすることができます。 
    
VCSTATUS_DELETE 
  
> メッセージを削除することができます。
    
VCSTATUS_DELETE_IS_MOVE 
  
> 削除されると、メッセージは、メッセージ ・ ストアからすぐに削除されているのではなく、メッセージ ・ ストア内の**削除済みアイテム**フォルダーに移動します。 
    
VCSTATUS_MOVE 
  
> メッセージを移動することができます。
    
VCSTATUS_NEW_MESSAGE 
  
> 新しいメッセージを作成することができます。
    
VCSTATUS_SAVE 
  
> メッセージを保存することができます。
    
VCSTATUS_SUBMIT 
  
> メッセージを送信することができます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム オブジェクトは、現在のメッセージのメッセージ サイト オブジェクトの機能を取得する**IMAPIMessageSite::GetSiteStatus**メソッドを呼び出します。 _LpulStatus_パラメーターで返されるフラグは、メッセージのサイトに関する情報を提供します。 通常、フォームは、有効または、フラグが提供する機能に関する情報のサイトのメッセージの実装によって、メニュー コマンドを無効にします。 新しいメッセージは、 [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドまたは[IPersistMessage::Load](ipersistmessage-load.md)メソッドによってフォームに読み込まれている場合は、ステータス フラグを選択してください。 いくつかのメッセージ サイト オブジェクト、特に読み取り専用オブジェクトは、メッセージを保存または削除を許可しません。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**IMAPIMessageSite::GetSiteStatus**メソッドには、どのような操作したり、現在のメッセージに対しては実行できませんを決定するいくつかの計算を実行するクライアント アプリケーションが必要です。 通常、ステータス行に現在のメッセージのメッセージ ストア プロバイダーを探してに関連するまたはどのアクションを決定するのには、ストア プロバイダーのクエリを実行するクライアント アプリケーションはメッセージ ストアを使用して実行できます。 たとえば、MAPI_DELETE_IS_MOVE フラグを返すかどうかを決定するには、内の**削除済みアイテム**フォルダーがあるかどうかを確認するメッセージ ストア オブジェクトの**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) のプロパティをチェックしますメッセージ ・ ストアです。 
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI では、 **IMAPIMessageSite::GetSiteStatus**メソッドを使用して、指定したサイトのステータスを取得します。 それは、VCSTATUS_NEW_MESSAGE、VCSTATUS_SAVE、または VCSTATUS_SUBMIT を返すことができます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[PidTagIpmWastebasketEntryId の標準的なプロパティ](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームのインタ フェース](mapi-form-interfaces.md)

