---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321414"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージを削除します。
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

 _pViewContext_
  
> [in]ビュー コンテキスト オブジェクトへのポインター。
    
 _prcPosRect_
  
> [in]現在のフォームのウィンドウ サイズと位置を含む [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) 構造体へのポインター。 次に表示されるフォームでは、このウィンドウの四角形も使用されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> この操作は、このメッセージ サイトではサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::D eleteMessage** メソッドを呼び出して、フォームが現在表示しているメッセージを削除します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

DeleteMessage の戻り **値に** 続いて、フォーム オブジェクトは新しいメッセージを確認し、存在しない場合は自分自身を閉じなければならない。 **DeleteMessage** が処理されたメッセージが削除済みまたは削除済みアイテム フォルダーに移動されたかどうかを判断するために、フォーム オブジェクトは [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドを呼び出して、DELETE_IS_MOVE フラグが返されたかどうかを判断できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

メッセージを削除した後、フォーム ビューアーの **DeleteMessage** メソッドの実装が次のメッセージに移動する場合、実装は [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) メソッドを呼び出し、実際の削除を実行する前に VCDIR_DELETE フラグを渡す必要があります。 フォーム ビューアーの **DeleteMessage** の実装が削除済みメッセージ (削除済みアイテムフォルダーなど) を移動する場合、メッセージが変更された場合、そのメッセージに対する変更を保存する必要があります。 
  
DeleteMessage の一般的な **実装では、** 次のタスクを実行します。 
  
1. 実装がメッセージを移動している場合は [、iPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出し、pMessage パラメーターに null を渡し _、fSameAsLoad_ パラメーターに true を渡します。  
    
2. このメソッドは **IMAPIViewContext::ActivateNext** メソッドを呼び出し  _、ulDir_ パラメーターに VCDIR_DELETEフラグを渡します。 
    
3. **ActivateNext 呼び出し** が失敗すると、その呼び出しが返されます。 **ActivateNext が** メソッドを返S_FALSE、IPersistMessage::HandsOffMessage メソッド [を呼び出](ipersistmessage-handsoffmessage.md)します。 
    
4. メッセージを削除または移動します。
    
フォームのウィンドウ **で使用される RECT** 構造を取得するには [、GetWindowRect](https://msdn.microsoft.com/library/ms633519)関数Windows呼び出します。 
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

