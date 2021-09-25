---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3037187383cd5a00c96ce51c66950ee795e15052
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604832"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したメッセージ クラスの受信メッセージの送信先として、またはメッセージ ストアの既定の受信フォルダーとして確立されたフォルダーを取得します。
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>パラメーター

 _lpszMessageClass_
  
> [in]受信フォルダーに関連付けられているメッセージ クラスへのポインター。 _lpszMessageClass_ パラメーターが NULL または空の文字列に設定されている場合 **、GetReceiveFolder** はメッセージ ストアの既定の受信フォルダーを返します。 
    
 _ulFlags_
  
> [in]渡された文字列と返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージ クラスの文字列は Unicode 形式です。 メッセージ クラスMAPI_UNICODEが設定されていない場合、メッセージ クラス文字列は ANSI 形式です。
    
 _lpcbEntryID_
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEntryID_
  
> [out]要求された受信フォルダーのエントリ識別子へのポインターを指すポインター。
    
 _lppszExplicitClass_
  
> [out]  _lppEntryID_ が指すフォルダーを受信フォルダーとして明示的に設定するメッセージ クラスへのポインターを指すポインター。 このメッセージ クラスは  _、lpszMessageClass_ パラメーターのクラスと同じか、そのクラスの基本クラスのいずれかである必要があります。 NULL を渡す場合は  _、lppEntryID_ が指すフォルダーがメッセージ ストアの既定の受信フォルダーです。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダーが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::GetReceiveFolder** メソッドは、受信フォルダー (特定のメッセージ クラスの受信メッセージを受信するために指定されたフォルダー) のエントリ識別子を取得します。 呼び出し元は  _、lpszMessageClass_ パラメーターでメッセージ クラスまたは NULL を指定できます。 _lpszMessageClass が_ NULL の場合 **、GetReceiveFolder は次** の値を返します。 
  
- _lppszExplicitClass_ では、受信フォルダーを明示的に設定する _lpszMessageClass_ が指すメッセージ クラスの最初の基本クラスの名前を指定します。 
    
- _lppEntryID では__、lppszExplicitClass_ パラメーターが指す基本クラスの受信フォルダーのエントリ識別子。 
    
たとえば、メッセージ クラス IPM の受信フォルダーと **します。メモ** は受信トレイのエントリ識別子に設定され **、GetReceiveFolder** は _lpszMessageClass_ の内容を IPM に設定して呼び **出されます。注。電話**. **IPM の場合。注。電話** 明示的な受信フォルダー セットが存在しない場合 **、GetReceiveFolder** は _lppEntryID_ と IPM の受信トレイのエントリ **識別子を返します。** _lppszExplicitClass のメモ_。
  
クライアントがメッセージ クラスの **GetReceiveFolder** を呼び出し、そのメッセージ クラスの受信フォルダーを設定していない場合  _、lppszExplicitClass_ は、クライアントが  _ulFlags_ パラメーターに MAPI_UNICODE フラグを設定したかどうかに応じて、長さ 0 の文字列、Unicode 形式の文字列、または ANSI 形式の文字列のいずれかです。 
  
_lpszMessageClass_ パラメーターに NULL を渡して取得した既定の受信フォルダーは、すべてのメッセージ ストアに常に存在します。 
  
クライアントは [、lppEntryID](mapifreebuffer.md) で返されるエントリ識別子を使用して、そのエントリ識別子を保持するメモリを解放するときに  _MAPIFreeBuffer_ 関数を呼び出す必要があります。 また _、lppszExplicitClass_ で返されるメッセージ クラス文字列を使用して、その文字列を保持するメモリを解放するときに **MAPIFreeBuffer** を呼び出す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI は **、IMsgStore::GetReceiveFolder** メソッドを使用して受信トレイ フォルダーを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

