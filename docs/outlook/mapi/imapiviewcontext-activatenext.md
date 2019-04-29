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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410617"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**適用対象**: Outlook 2013 | Outlook 2016 
  
表示順序に従って、次または前のメッセージをアクティブにします。 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

_uldir_
  
> 順番アクティブ化するメッセージに関する情報を提供するステータスフラグ。 有効なフラグの設定は次のとおりです。
    
  - VCDIR_CATEGORY: ビューアーでは、ビューの別のカテゴリにあるメッセージをアクティブ化する必要があります。 アクティブにするメッセージは次のとおりです。 
        
    - このフラグが VCDIR_NEXT の場合は、次のビューカテゴリ**** の最初のメッセージ。 
        
    - このフラグが VCDIR_PREV で、前のカテゴリが展開さ**** れている場合、前のビューカテゴリの最後のメッセージ。 
        
    - このフラグが VCDIR_PREV で、前のカテゴリが展開さ**** れていない場合、前のビューカテゴリの最初のメッセージ。 この場合、前のカテゴリは自動拡張を行います。 
        
  - VCDIR_DELETE: 現在のメッセージが削除されているため、閲覧者は次または前のメッセージをアクティブにする必要があります。 
        
  - VCDIR_MOVE: 現在のメッセージが移動されたため、閲覧者は次または前のメッセージをアクティブにする必要があります。 
        
  - VCDIR_NEXT: 閲覧者は、表示順序で次のメッセージをアクティブ化する必要があります。 
        
  - VCDIR_PREV: 閲覧者は、表示順序で前のメッセージをアクティブ化する必要があります。 
        
  - VCDIR_UNREAD: 閲覧者は、表示順序で、次または前の未読メッセージをアクティブにする必要があります。 
    
_prcposrect_
  
> 順番アクティブ化されたメッセージの表示に使用されるウィンドウのサイズと位置を含む Windows **RECT**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常にアクティブ化されました。 
    
S_FALSE 
  
> メッセージは正常にアクティブ化されましたが、プロセスで別の種類のフォームが開かれました。
    
## <a name="remarks"></a>注釈

Form オブジェクトは、 **imapiviewcontext:: ActivateNext**メソッドを呼び出して、ユーザーに表示されるメッセージを変更します。 _uldir_パラメーターで渡される値は、アクティブ化する必要があるメッセージと、場合によっては理由を示します。 VCDIR_NEXT および VCDIR_PREVIOUS の各フラグは、ビュー内で**次**または**前**のコマンドを選択したユーザーにそれぞれ対応します。 通常、これらの操作は、フォームビューアーのメッセージの一覧で1つ上または下のメッセージを移動することに対応します。 
  
VCDIR_DELETE および VCDIR_MOVE フラグは、それぞれ[IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md)メソッドと[IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md)メソッドによって設定されます。 これらのメソッドの実装は、適切な方向で**ActivateNext**を呼び出し、 **ActivateNext**呼び出しが失敗しなかった場合にメッセージに対して要求された操作を実行します。 通常、フォームビューアーを使用すると、ユーザーはメッセージリスト内で移動する方向を指定できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

[imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)の実装により、 _uldir_の値に応じて、フォルダー内の次のメッセージまたは前のメッセージが作成されます (現在のメッセージ)。 **ActivateNext**が戻ると、 [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md)を呼び出して、新しくアクティブ化されたメッセージへのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ActivateNext**が S_FALSE を返す場合、または現在のメッセージが存在しない場合は、通常のシャットダウン手順を実行します。これには、フォームの[imapiform:: shutdownform](imapiform-shutdownform.md)メソッドの呼び出しが含まれている必要があります。 次または前のメッセージが表示された場合は、 _prcposrect_パラメーターで渡されたウィンドウ四角形を使用して表示します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: ActivateNext  <br/> |mfcmapi は、この関数に**imapiviewcontext:: ActivateNext**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

