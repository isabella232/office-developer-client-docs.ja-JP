---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3745b8c9b779f40e9356efeec35a78025193965c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630517"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のメッセージ クラスの受信メッセージの宛先としてフォルダーを確立します。
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpszMessageClass_
  
> [in]新しい受信フォルダーに関連付けるメッセージ クラスへのポインター。 _lpszMessageClass_ パラメーターが NULL または空の文字列に設定されている場合 **、SetReceiveFolder** はメッセージ ストアの既定の受信フォルダーを設定します。 
    
 _ulFlags_
  
> [in]渡された文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージ クラスの文字列は Unicode 形式です。 メッセージ クラスMAPI_UNICODEが設定されていない場合、メッセージ クラス文字列は ANSI 形式です。
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]受信フォルダーとして確立するフォルダーのエントリ識別子へのポインター。 _lpEntryID_ パラメーターが NULL に設定されている場合 **、SetReceiveFolder** は現在の受信フォルダーをメッセージ ストアの既定値に置き換える。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダーが正常に確立されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::SetReceiveFolder** メソッドは、特定のメッセージ クラスの受信フォルダーを設定または変更します。 **SetReceiveFolder** を使用すると、クライアントは、連続する呼び出しを使用して、定義されたメッセージ クラスごとに異なる受信フォルダーを指定するか、複数のメッセージ クラスの受信メッセージがすべて同じフォルダーに移動することを指定できます。 たとえば、クライアントは独自のクラスのメッセージを独自のフォルダーに到着できます。 FAX アプリケーションは、ストア プロバイダーが受信 FAX を置く 1 つのフォルダーと、プロバイダーが送信 FAX を置く別のフォルダーを指定できます。
  
**SetReceiveFolder** の呼び出し中にエラーが発生した場合、受信フォルダーの設定は変更されません。 
  
**SetReceiveFolder** が _lpEntryID_ を NULL に設定して受信フォルダーの設定を変更すると、既定の受信フォルダーを設定する必要がある場合 **、SetReceiveFolder** は、指定されたメッセージ クラスに既存の設定が存在しない場合でも、S_OK を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI は **、IMsgStore::SetReceiveFolder** メソッドを使用して、フォルダーを特定のメッセージ クラスの受信フォルダーとして設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

