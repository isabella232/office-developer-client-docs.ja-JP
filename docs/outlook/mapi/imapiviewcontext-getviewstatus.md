---
title: imapiviewcontextgetviewstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351178"
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

 _lアウト状態_
  
> 読み上げビューアーの状態を提供するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリに、次または前のメッセージがあります。 
    
VCSTATUS_DELETE 
  
> フォームでは、メッセージを削除できます。 
    
VCSTATUS_INTERACTIVE 
  
> フォームにユーザーインターフェイスが表示されます。 このフラグが設定されていない場合、通常はユーザーインターフェイスが表示される原因となる動詞に応答しても、フォームはユーザーインターフェイスを表示しません。 
    
VCSTATUS_MODAL 
  
> フォームはビューアーに対してモーダルです。 
    
VCSTATUS_NEXT 
  
> ビューに次のメッセージがあります。 
    
VCSTATUS_PREV 
  
> ビューに前のメッセージがあります。 
    
VCSTATUS_READONLY 
  
> メッセージは読み取り専用モードで開かれます。 Delete、submit、および move 操作を無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> ビューに次または前の未読メッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 閲覧者の状態が正常に返されました。
    
## <a name="remarks"></a>解説

form オブジェクトは、 **imapiviewcontext:: getviewstatus**メソッドを呼び出して、**次**のコマンドがメッセージをアクティブ化する方向で、またはその両方の方向に、フォームビューでアクティブ化するメッセージがまだあるかどうかを判断します。**前**のコマンドがメッセージをアクティブにする方向、または両方の方向。 _lVCSTATUS_NEXT status_パラメーターで指定された値は、VCSTATUS_PREV フラグが[imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)に対して有効かどうかを判断するために使用されます。 VCSTATUS_DELETE フラグが設定されていても、VCSTATUS_READONLY フラグが設定されていない場合は、 [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md)メソッドを使用してメッセージを削除できます。 
  
通常、フォームはメニューコマンドとボタンが閲覧者のコンテキストに対して有効でない場合は無効にします。 ビューアーは、 [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md)メソッドを呼び出すことによって、状態を変化させるようにフォームに通知できます。 
  
VCSTATUS_MODAL フラグが設定されているのは、以前の imapiform でハンドルが渡されているウィンドウに対してフォームがモーダルである必要がある場合です[。:D overb](imapiform-doverb.md)呼び出し。 VCSTATUS_MODAL が設定されている場合、フォームが閉じるまで、 **DoVerb**呼び出しが行われたスレッドをフォームで使用できます。 VCSTATUS_MODAL が設定されていない場合、このウィンドウではフォームがモーダルではないので、スレッドを使用してはなりません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: getviewstatus  <br/> |mfcmapi は、この関数の**imapiviewcontext:: getviewstatus**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

