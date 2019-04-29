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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430708"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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

 _ulattachmentnum_
  
> 順番削除する添付ファイルのインデックス番号を指定します。 これは、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティの値です。
    
 _uluiparam_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで ATTACH_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI progress オブジェクトの実装を使用して進行状況インジケーターを表示します。 ATTACH_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番ユーザーインターフェイスの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ATTACH_DIALOG 
  
> 操作が続行されると、進行状況インジケーターの表示を要求します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に削除されました。
    
## <a name="remarks"></a>注釈

**IMessage::D eleteattach**メソッドは、メッセージ内から添付ファイルを削除します。 
  
削除された添付ファイルは、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまで完全に削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**deleteattach**を呼び出す前に、添付ファイルとその各ストリームの**IUnknown:: Release**メソッドを呼び出します。 
  
添付ファイルの削除は時間がかかることがあるため、 **deleteattach**には進行状況インジケーターを表示するメカニズムが用意されています。 進行状況インジケーターの表示を要求するには、 [imapiprogress](imapiprogressiunknown.md)へのポインターを渡します: IUnknown 実装または NULL (実装されていない場合)。 _uluiparam_パラメーターでウィンドウハンドルを指定し、 _ulflags_パラメーターに ATTACH_DIALOG フラグも指定する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AttachmentsDlg  <br/> |CAttachmentsDlg:: OnDeleteSelectedItem  <br/> |mfcmapi は、 **IMessage::D eleteattach**メソッドを使用して、選択されている添付ファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

