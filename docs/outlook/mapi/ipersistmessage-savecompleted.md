---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317137"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**適用対象**: Outlook 2013 | Outlook 2016 
  
保存操作が完了したフォームに通知します。 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>パラメーター

_pMessage_
  
> [in]新しく保存されたメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
E_INVALIDARG 
  
> _pMessage パラメーター_ は NULL で、フォームは [HandsOffFromNormal](handsofffromnormal-state.md)または [HandsOffAfterSave](handsoffaftersave-state.md)状態のいずれかです。 
    
E_UNEXPECTED 
  
> フォームは、次のいずれかの状態ではありません。
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>注釈

**IPersistMessage::SaveCompleted** メソッドは、フォーム ビューアーによって呼び出され、保留中のすべての変更が保存されたというフォームを通知します。 **SaveCompleted は** 、フォームが次のいずれかの状態にある場合にのみ呼び出す必要があります。 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**SaveCompleted** メソッドが実行できるアクションは、メッセージ ポインター パラメーターに含まれるもの、およびメッセージの状態に応じていくつか考えられる操作です。 ただし、アクションが成功した場合は  _、pMessage_ パラメーターがポイントするメッセージの現在の状態を常に保存し、フォームを標準状態 [に移行](normal-state.md) します。 
  
次の表に **、SaveCompleted** の実装で実行する必要があるアクションに影響を与える条件を示します。
  
|**条件**|**処理**|
|:-----|:-----|
|_pMessage パラメーター_ は NULL で [、IPersistMessage::Save](ipersistmessage-save.md)メソッドの _fSameAsLoad_ パラメーターは TRUE に設定されます。  <br/> |すべての登録済 [みビューアーの IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。  <br/> |
|_pMessage パラメーター_ は NULL で **、IPersistMessage::Save** メソッドの _fSameAsLoad_ パラメーターは FALSE に設定されます。  <br/> |S_OK ��Ԃ��܂��B  <br/> |
|フォームは HandsOffFromNormal 状態です。  <br/> |現在のメッセージを解放し、pMessage パラメーターが指すメッセージ  _に置き換_ える。 置換メッセージの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) メソッドを呼び出し、次のS_OK。  <br/> |
|フォームは HandsOffAfterSave 状態です。  <br/> |すべての登録済 **みビューアーの IMAPIViewAdviseSink::OnSaved** メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。  <br/> |
|フォームは [NoScribble 状態](noscribble-state.md) です。  <br/> |現在のメッセージを解放し、pMessage が指すメッセージに  _置き換える_。 置換メッセージの **IUnknown::AddRef メソッドを呼び出** します。 すべての登録済 **みビューアーの IMAPIViewAdviseSink::OnSaved** メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。  <br/> |
|フォームは HandsOff 状態の 1 つで  _、pMessage_ パラメーターは NULL に設定されます。  <br/> |値をE_INVALIDARG。  <br/> |
|フォームは、HandsOff 状態または NoScribble 状態以外の状態です。  <br/> |値をE_UNEXPECTED。  <br/> |
   
ストレージ オブジェクトの保存の詳細については [、IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) メソッドまたは [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) メソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [フォームの状態](form-states.md)
