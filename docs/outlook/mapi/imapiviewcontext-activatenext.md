---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d4d8f2b8ea54c4eaa7fd6dff7b8051e20780504
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625267"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**適用対象**: Outlook 2013 | Outlook 2016 
  
ビューの順序で次または前のメッセージをアクティブ化します。 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

_ulDir_
  
> [in]アクティブ化するメッセージに関する情報を示す状態フラグ。 有効なフラグ設定は次のとおりです。
    
  - VCDIR_CATEGORY: ビューアーは、ビューの別のカテゴリでメッセージをアクティブ化する必要があります。 アクティブ化するメッセージは次の場合です。 
        
    - このフラグが OR の場合は、次のビュー カテゴリの最初のVCDIR_NEXT。 
        
    - 前のビュー カテゴリの最後のメッセージ (このフラグが **OR** で、前のVCDIR_PREVが展開されている場合。 
        
    - 前のビュー カテゴリの最初のメッセージ (このフラグが **OR** で、前のVCDIR_PREVが展開されていない場合。 この場合、前のカテゴリは自動的に展開されます。 
        
  - VCDIR_DELETE: 現在のメッセージが削除されたため、ビューアーは次または前のメッセージをアクティブにする必要があります。 
        
  - VCDIR_MOVE: 現在のメッセージが移動されたため、ビューアーは次または前のメッセージをアクティブにする必要があります。 
        
  - VCDIR_NEXT: ビューアーは、ビューの順序で次のメッセージをアクティブにする必要があります。 
        
  - VCDIR_PREV: ビューアーは、ビューの順序で前のメッセージをアクティブにする必要があります。 
        
  - VCDIR_UNREAD: ビューアーは、ビューの順序で次または前の未読メッセージをアクティブにする必要があります。 
    
_prcPosRect_
  
> [in]アクティブ化されたWindows表示するウィンドウのサイズと位置を含む **RECT** 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常にアクティブ化されました。 
    
S_FALSE 
  
> メッセージは正常にアクティブ化されましたが、プロセスで別の種類のフォームが開かされました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIViewContext::ActivateNext** メソッドを呼び出して、ユーザーに表示されるメッセージを変更します。 _ulDir_ パラメーターで渡される値は、アクティブ化するメッセージと、場合によっては理由を示します。 このVCDIR_NEXTおよびVCDIR_PREVIOUSは、ビューで [**次** へ] または [前へ] コマンドをそれぞれ選択したユーザーに対応します。 通常、これらの操作は、フォーム ビューアーのメッセージの一覧で 1 つのメッセージを上下に移動する操作に対応します。 
  
このVCDIR_DELETEおよびVCDIR_MOVEフラグは [、IMAPIMessageSite::D eleteMessage](imapimessagesite-deletemessage.md) メソッドと [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) メソッドによってそれぞれ設定されます。 これらのメソッドの実装では **、ActivateNext** を適切な方向に呼び出し **、ActivateNext** 呼び出しが失敗しなかった場合は、メッセージに対して要求された操作を実行します。 通常、フォーム ビューアーを使用すると、ユーザーはメッセージ リスト内を移動する方向を指定できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)の実装では _、ulDir_ の値に応じて、フォルダー内の次または前のメッセージが現在のメッセージになります。 **ActivateNext が返** された後 [、IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md)を呼び出して、新しくアクティブ化されたメッセージへのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ActivateNext** が S_FALSE を返す場合、または現在のメッセージが存在しない場合は、フォームの [IMAPIForm::ShutdownForm](imapiform-shutdownform.md)メソッドの呼び出しを含む通常のシャットダウン手順を実行します。 次または前のメッセージが表示される場合は  _、prcPosRect_ パラメーターで渡されたウィンドウ四角形を使用して表示します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI は、 **この関数に IMAPIViewContext::ActivateNext メソッド** を実装します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

