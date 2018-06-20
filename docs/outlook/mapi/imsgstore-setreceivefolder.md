---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801027"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**適用されます**: Outlook 
  
特定のメッセージ クラスの着信メッセージの送信先として、フォルダーを確立します。
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in]新しいに関連するメッセージ クラスへのポインターでは、フォルダーが表示されます。 セット_lpszMessageClass_パラメーターが NULL または空の文字列を**SetReceiveFolder**に設定、既定ではメッセージ ストアのフォルダーが表示されます。 
    
 _ulFlags_
  
> [in]渡された文字列内のテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> メッセージ クラスの文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のメッセージ クラスの文字列です。
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]受信フォルダーとして設定するフォルダーのエントリの識別子へのポインター。 置換_lpEntryID_パラメーターが NULL の場合、 **SetReceiveFolder**に設定、現在ではメッセージ ストアの既定のフォルダーが表示されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 受信フォルダーが正常に確立しました。
    
## <a name="remarks"></a>備考

**IMsgStore::SetReceiveFolder**メソッドは、特定のメッセージ クラスに対応する受信フォルダーを変更または設定します。 **SetReceiveFolder**とクライアント指定することも、後続の呼び出しを使用して、別に定義されたメッセージ クラスごとにフォルダーが表示されるか複数のメッセージ クラスのすべての受信メッセージが同じフォルダーに移動するかを指定します。 などのクライアントは独自のフォルダーに到着したメッセージの独自クラスを持つことができます。 Fax アプリケーションには、ストア プロバイダーが着信 fax を格納する 1 つのフォルダーと、プロバイダーが発信 fax を配置する別のフォルダーを指定できます。
  
**SetReceiveFolder**への呼び出し中にエラーが発生した場合、受信フォルダーの設定は変更されません。 
  
**SetReceiveFolder**が変更された場合、受信フォルダーの設定_lpEntryID_では NULL に設定をデフォルトの受信フォルダーを設定する必要があります、指定した既存の設定がない場合でも、 **SetReceiveFolder**は S_OK を返しますメッセージ クラスです。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnSetReceiveFolder  <br/> |MFCMAPI では、 **IMsgStore::SetReceiveFolder**メソッドを使用して、特定のメッセージ クラスに対応する受信フォルダーとしてフォルダーを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

