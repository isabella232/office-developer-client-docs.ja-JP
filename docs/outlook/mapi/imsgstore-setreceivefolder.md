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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434089"
---
# <a name="imsgstoresetreceivefolder"></a>IMsgStore::SetReceiveFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のメッセージクラスの受信メッセージの送信先としてフォルダーを確立します。
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpszmessageclass_
  
> 順番新しい受信フォルダーに関連付けられるメッセージクラスへのポインター。 _lpszmessageclass_パラメーターが NULL または空の文字列に設定されている場合、 **setreceivefolder**は、メッセージストアの既定の受信フォルダーを設定します。 
    
 _ulFlags_
  
> 順番渡された文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージクラスの文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、メッセージクラスの文字列は ANSI 形式になります。
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番受信フォルダーとして確立するフォルダーのエントリ識別子へのポインター。 _lpentryid_パラメーターが NULL に設定されている場合、 **setreceivefolder**は現在の受信フォルダーをメッセージストアの既定値で置き換えます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 受信フォルダーが正常に確立されました。
    
## <a name="remarks"></a>注釈

**IMsgStore:: setreceivefolder**メソッドは、特定のメッセージクラスの受信フォルダーを設定または変更します。 **setreceivefolder**では、クライアントは、連続した呼び出しを使用して、定義された各メッセージクラスに対して異なる受信フォルダーを指定したり、複数のメッセージクラスの受信メッセージをすべて同じフォルダーに移動するように指定したりできます。 たとえば、クライアントは独自のフォルダーにメッセージの独自のクラスを受け取ることができます。 fax アプリケーションは、受信 fax を格納する1つのフォルダーと、プロバイダーが発信 fax を配置する別のフォルダーを指定できます。
  
**setreceivefolder**の呼び出し中にエラーが発生しても、受信フォルダーの設定は変わりません。 
  
**setreceivefolder**で、 _lpentryid_が NULL に設定されている受信フォルダーの設定を変更すると、既定の受信フォルダーが設定されていることを示します。 **setreceivefolder**は、指定されたメッセージクラス。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: OnSetReceiveFolder  <br/> |mfcmapi は、 **IMsgStore:: setreceivefolder**メソッドを使用して、特定のメッセージクラスの受信フォルダーとしてフォルダーを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

