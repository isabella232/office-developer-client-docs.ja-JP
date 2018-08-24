---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588504"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**適用対象**: Outlook 2013 | Outlook 2016 
  
ビューの順序で次または前のメッセージをアクティブにします。 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

_ulDir_
  
> [in]ステータスのフラグを有効にするメッセージに関する情報を提供します。 有効なフラグの設定は次のとおりです。
    
  - VCDIR_CATEGORY: ビューアーがビューの別のカテゴリでメッセージを有効にします。 メッセージを有効にするのには次のとおりです。 
        
    - このフラグが VCDIR_NEXT で、**または**ed の場合、次のビュー カテゴリの最初のメッセージです。 
        
    - 前のビューのカテゴリをこのフラグが VCDIR_PREV の**OR**演算の場合、前のカテゴリの最後のメッセージを展開します。 
        
    - 前のビューのカテゴリをこのフラグが VCDIR_PREV の**OR**演算の場合、前のカテゴリの最初のメッセージが展開されていません。 ここで前の分類では、自動拡張が行われます。 
        
  - VCDIR_DELETE: ビューアーがアクティブに、次または前のメッセージの現在のメッセージが削除されたためです。 
        
  - VCDIR_MOVE: ビューアーがアクティブに、次または前のメッセージの現在のメッセージが移動されたためです。 
        
  - VCDIR_NEXT: ビューアーが表示順序の次のメッセージを有効にします。 
        
  - VCDIR_PREV: ビューアーが表示順序で前のメッセージを有効にします。 
        
  - VCDIR_UNREAD: ビューアーが表示順序で次または前の未読メ ッ セージを有効にします。 
    
_prcPosRect_
  
> [in]Windows **RECT**へのポインターでは、アクティブ化されたメッセージの表示に使用するウィンドウの位置とサイズを含む構造体です。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージは正常にアクティブになります。 
    
S_FALSE 
  
> メッセージが正常にアクティブ化されたが、プロセスで開いているフォームの別の種類です。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、ユーザーに表示されているメッセージを変更するのには**IMAPIViewContext::ActivateNext**メソッドを呼び出します。 _UlDir_パラメーターで渡された値は、どのようなメッセージがアクティブ化され、一部にする必要があることを示します、場合によってはその理由です。 VCDIR_NEXT と VCDIR_PREVIOUS のフラグは、ユーザーがビューでは、**次**または**前**のコマンドを選択すると、それぞれに対応します。 これらの操作は、通常 1 つのメッセージのメッセージ フォーム ビューアーの一覧で上下に移動するのには対応しています。 
  
VCDIR_DELETE と VCDIR_MOVE のフラグがそれぞれの[IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md)と[IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md)メソッドによって設定されます。 これらのメソッドの実装は適切な方向で**ActivateNext**を呼び出すし、 **ActivateNext**の呼び出しが失敗しなかった場合、メッセージで要求された操作を実行します。 フォーム ビューアーは、通常メッセージの一覧内を移動する方向を指定するユーザーを有効にします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)の実装は、次または前のメッセージを_ulDir_、現在のメッセージの値に応じて、フォルダーになります。 **ActivateNext**が返されると、新しくアクティブになったメッセージへのポインターを取得するのには[IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md)を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ActivateNext**は S_FALSE を返す場合、または現在のメッセージが存在しない場合は、フォームの[IMAPIForm::ShutdownForm](imapiform-shutdownform.md)メソッドを呼び出す必要がありますが、通常のシャット ダウン手順を実行します。 次または前のメッセージが表示されている場合は、表示するために、 _prcPosRect_パラメーターに渡されたウィンドウの四角形を使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI では、この関数では、 **IMAPIViewContext::ActivateNext**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

