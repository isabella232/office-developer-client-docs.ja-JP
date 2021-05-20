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

 _ulAttachmentNum_
  
> [in]削除する添付ファイルのインデックス番号。 これは、添付ファイルのプロパティ [(PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)**プロパティPR_ATTACH_NUM** 値です。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウを処理します。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター ATTACH_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で ATTACH_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]ユーザー インターフェイスの表示を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ATTACH_DIALOG 
  
> 操作が進むにつれて進行状況インジケーターの表示を要求します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に削除されました。
    
## <a name="remarks"></a>注釈

**IMessage::D eleteAttach** メソッドは、メッセージ内から添付ファイルを削除します。 
  
メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドが呼び出されるまで、削除された添付ファイルは完全に削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**DeleteAttach を呼び出** す前に、添付ファイルとそのストリームの **IUnknown::Release** メソッドを呼び出します。 
  
添付ファイルの削除は長いプロセスになる可能性があるから **、DeleteAttach は** 進行状況インジケーターを表示するメカニズムを提供します。 [IMAPIProgress : IUnknown](imapiprogressiunknown.md)実装または実装がない場合は NULL にポインターを渡して進行状況インジケーターの表示を要求できます。 また、ulUIParam パラメーターでウィンドウ ハンドルを指定し  _、ulFlags_ パラメーター ATTACH_DIALOGフラグ  _を指定する必要_ があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI は **、IMessage::D eleteAttach** メソッドを使用して、選択した添付ファイルを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

