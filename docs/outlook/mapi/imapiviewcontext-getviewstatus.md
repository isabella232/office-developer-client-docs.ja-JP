---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b8549c2abbad33baf38312f0d803f1f6f3a8244
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579895"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のビューアーの状態を取得します。 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>パラメーター

 _lpulStatus_
  
> [out]ビューアーの状態を提供するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリに次または前のメッセージがあります。 
    
VCSTATUS_DELETE 
  
> フォームを使用すると、メッセージを削除できます。 
    
VCSTATUS_INTERACTIVE 
  
> フォームにユーザー インターフェイスが表示されます。 このフラグを設定しない場合、フォームは、通常はユーザー インターフェイスが表示される動詞に応答しても、ユーザー インターフェイスの表示を抑制する必要があります。 
    
VCSTATUS_MODAL 
  
> フォームはビューアーに対してモーダルです。 
    
VCSTATUS_NEXT 
  
> ビューに次のメッセージがあります。 
    
VCSTATUS_PREV 
  
> ビューに前のメッセージがあります。 
    
VCSTATUS_READONLY 
  
> メッセージは読み取り専用モードで開きます。 削除、送信、および移動操作は無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> ビューに次または前の未読メッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビューアーの状態が正常に返されました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIViewContext::GetViewStatus** メソッドを呼び出して、次のコマンドがメッセージをアクティブ化する方向、前のコマンドがメッセージをアクティブ化する方向、または両方向で、フォーム ビューでアクティブ化するメッセージが増えるかどうかを判断します。 _lpulStatus_ パラメーターが示す値を使用して [、imapIViewContext::ActivateNext](imapiviewcontext-activatenext.md)に対して VCSTATUS_NEXT フラグと VCSTATUS_PREV フラグが有効かどうかを判断します。 VCSTATUS_DELETE フラグが設定されているが、VCSTATUS_READONLY フラグが設定されていない場合は [、IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) メソッドを使用してメッセージを削除できます。 
  
通常、フォームは、ビューアーのコンテキストに対して無効な場合、メニュー コマンドとボタンを無効にします。 閲覧者は [、IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) メソッドを呼び出すことによって、フォームに状態の変更を通知できます。 
  
フォームVCSTATUS_MODAL前の [IMAPIForm::D oVerb](imapiform-doverb.md) 呼び出しでハンドルが渡されるウィンドウにモーダルである必要がある場合、このフラグが設定されます。 このVCSTATUS_MODAL設定されている場合、フォームは、フォームが閉じるまで **DoVerb** 呼び出しが行われたスレッドを使用できます。 このVCSTATUS_MODAL設定されていない場合、フォームはこのウィンドウにモーダルではなく、スレッドを使用する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI は、 **この関数に IMAPIViewContext::GetViewStatus** メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

