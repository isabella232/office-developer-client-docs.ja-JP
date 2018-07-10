---
title: IMAPIViewContextGetViewStatus
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800901"
---
# <a name="imapiviewcontextgetviewstatus"></a>IMAPIViewContext::GetViewStatus

  
  
**適用されます**: Outlook 
  
ビューアーの現在の状態を取得します。 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [out]ビュアーのステータスを提供するフラグのビットマップへのポインター。 次のフラグを設定することができます。
    
VCSTATUS_CATEGORY 
  
> 別のカテゴリで次または前のメッセージが表示されます。 
    
VCSTATUS_DELETE 
  
> フォームにより、メッセージが削除されます。 
    
VCSTATUS_INTERACTIVE 
  
> フォームは、ユーザー インターフェイスを表示する必要があります。 このフラグが設定されていない場合は、フォームがユーザー インターフェイスを表示するのには通常、動詞への応答であっても、ユーザー インターフェイスを表示するを抑制する必要があります。 
    
VCSTATUS_MODAL 
  
> フォームでは、ビューアーに固有の値です。 
    
VCSTATUS_NEXT 
  
> ビューで次のメッセージが表示されます。 
    
VCSTATUS_PREV 
  
> ビューで前のメッセージが表示されます。 
    
VCSTATUS_READONLY 
  
> メッセージでは、読み取り専用モードで開くことができません。 削除、送信、および移動の操作を無効にする必要があります。 
    
VCSTATUS_UNREAD 
  
> ビューで次または前の未読メ ッ セージがあります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ビューアーのステータスが正常に返されました。
    
## <a name="remarks"></a>備考

フォーム オブジェクトのいずれかのフォーム ビューでアクティブにするより多くのメッセージがあるかどうかを決定する**IMAPIViewContext::GetViewStatus**メソッドを呼び出して、または双方向は、**次**のコマンドをアクティブにする方向でのメッセージで、**前**のコマンドが、メッセージをアクティブにする方向または双方向にします。 VCSTATUS_NEXT と VCSTATUS_PREV のフラグが[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)に対して有効かどうかを確認するのには、 _lpulStatus_パラメーターが指す値が使用されます。 フラグの場合、VCSTATUS_DELETE セットがない、VCSTATUS_READONLY フラグは、 [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md)メソッドを使用してメッセージを削除することができますし。 
  
通常、フォームを無効にするメニュー コマンドやボタンのコンテキストに対して有効でない場合。 ビューアーは、その[IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md)メソッドを呼び出して、ステータスの変更をするためのフォームを警告できます。 
  
フォームをモーダル ウィンドウのハンドルが渡される必要がある場合、VCSTATUS_MODAL フラグが設定されて、以前の[IMAPIForm::DoVerb](imapiform-doverb.md)呼び出しで。 VCSTATUS_MODAL が設定されている場合、フォームは、フォームを閉じるまでの**DoVerb**呼び出しを行ったスレッドを使用できます。 VCSTATUS_MODAL が設定されていない場合、フォームはモーダル ウィンドウにすることはできず、スレッドを使用する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetViewStatus  <br/> |MFCMAPI では、この関数では、 **IMAPIViewContext::GetViewStatus**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
