---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348777"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したメッセージクラスの受信メッセージの宛先として、またはメッセージストアの既定の受信フォルダーとして確立されたフォルダーを取得します。
  
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

 _lpszmessageclass_
  
> 順番受信フォルダーに関連付けられているメッセージクラスへのポインター。 _lpszmessageclass_パラメーターが NULL または空の文字列に設定されている場合、 **getreceivefolder**はメッセージストアの既定の受信フォルダーを返します。 
    
 _ulFlags_
  
> 順番渡された文字列と返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージクラスの文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、メッセージクラスの文字列は ANSI 形式になります。
    
 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げ要求された受信フォルダーのエントリ識別子へのポインターへのポインター。
    
 _lppszExplicitClass_
  
> 読み上げ_lppentryid_によって参照されるフォルダーを受信フォルダーとして明示的に設定する、メッセージクラスへのポインターへのポインター。 このメッセージクラスは、 _lpszmessageclass_パラメーターのクラス、またはそのクラスの基本クラスのいずれかである必要があります。 NULL を渡すと、 _lppentryid_が指すフォルダーが、メッセージストアの既定の受信フォルダーであることを示します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダーが正常に返されました。
    
## <a name="remarks"></a>解説

**IMsgStore:: getreceivefolder**メソッドは、受信フォルダーのエントリ id を取得します。これは、特定のメッセージクラスの受信メッセージを受信するように指定されたフォルダーです。 呼び出し元は、 _lpszmessageclass_パラメーターでメッセージクラスまたは NULL を指定できます。 _lpszmessageclass_が NULL の場合、 **getreceivefolder**は次の値を返します。 
  
- _lppszExplicitClass_では、明示的に受信フォルダーを設定する、 _lpszmessageclass_が指すメッセージクラスの最初の基本クラスの名前。 
    
- _lppentryid_の場合、 _lppszExplicitClass_パラメーターによって参照される基本クラスの受信フォルダーのエントリ識別子。 
    
たとえば、メッセージクラス IPM の受信フォルダーがあるとし**ます。メモ**は、受信トレイのエントリ識別子に設定され、 _lpszmessageclass_の内容を IPM に設定して、 **getreceivefolder**が呼び出され**ます。注電話番号** **IPM.メモ電話**には、明示的な受信フォルダーが設定されていません。 **getreceivefolder**は、 _lppentryid_および IPM で受信トレイのエントリ識別子を返し**ます。** _lppszExplicitClass_でメモします。
  
クライアントがメッセージクラスの**getreceivefolder**を呼び出し、そのメッセージクラスの受信フォルダーが設定されていない場合、 _lppszExplicitClass_は、長さ0の文字列、Unicode 形式の文字列、または ANSI 形式の文字列のいずれかになります。クライアントは_ulflags_パラメーターに MAPI_UNICODE フラグを設定します。 
  
_lpszmessageclass_パラメーターで NULL を渡すことによって取得される既定の受信フォルダーは、すべてのメッセージストアに常に存在します。 
  
クライアントは、そのエントリ識別子を保持するメモリを解放するために、 _lppentryid_で返されたエントリ識別子を使用して実行されたときに[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。 また、 _lppszExplicitClass_で返されたメッセージクラス文字列を使用して、その文字列を保持するメモリを解放する場合も、 **MAPIFreeBuffer**を呼び出す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions  <br/> |getinbox  <br/> |mfcmapi は、 **IMsgStore:: getreceivefolder**メソッドを使用して、受信トレイフォルダーを見つけます。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

