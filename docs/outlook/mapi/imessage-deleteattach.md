---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800897"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**適用対象**: Outlook 
  
添付ファイルを削除します。
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulAttachmentNum_
  
> [in]削除する添付ファイルのインデックス番号です。 これは、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティの値です。
    
 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたは windows のこのメソッドは、表示を処理します。 _UlFlags_パラメーターに ATTACH_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーには、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターが表示されます。 _UlFlags_に ATTACH_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]ユーザー インターフェイスの表示を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
ATTACH_DIALOG 
  
> 操作の進行中は、進行状況インジケーターの表示を要求します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 添付ファイルが正常に削除されました。
    
## <a name="remarks"></a>注釈

**IMessage::DeleteAttach**メソッドは、メッセージ内から添付ファイルを削除します。 
  
メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまで、削除された添付ファイルは完全に削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**DeleteAttach**を呼び出す前に、添付ファイルとそのストリームのそれぞれ**が**メソッドを呼び出します。 
  
添付ファイルを削除できますが、手間がかかりますので、 **DeleteAttach**は進行状況インジケーターを表示するメカニズムを提供します。 ポインターを渡すことによって、進行状況インジケーターの表示を要求することができます、 [IMAPIProgress: IUnknown](imapiprogressiunknown.md)実装、または NULL の場合は、実装する必要はありません。 _UlUIParam_パラメーターと、ATTACH_DIALOG のフラグ、 _ulFlags_パラメーターにウィンドウ ハンドルを指定することもする必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI では、 **IMessage::DeleteAttach**メソッドを使用して、選択した添付ファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

