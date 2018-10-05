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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395057"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームに通知する、保存操作が完了しました。 
  
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
  
> 通知が正常に完了しました。
    
E_INVALIDARG 
  
> _PMessage_パラメーターが NULL と、フォームは、 [HandsOffFromNormal](handsofffromnormal-state.md)または[HandsOffAfterSave](handsoffaftersave-state.md)の状態のいずれかの方法です。 
    
E_UNEXPECTED 
  
> 状態は、次のいずれかのフォームではありません。
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>備考

**IPersistMessage::SaveCompleted**メソッドは、すべての保留中の変更が保存されているフォームを通知するためにフォーム ビューアーによって呼び出されます。 **SaveCompleted**は、フォームが次の状態のいずれかの場合にのみ呼び出す必要があります。 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>実装者へのメモ

**SaveCompleted**メソッドを実行できるいくつかの実行可能なアクションがある、どのようなメッセージによっては、ポインター パラメーターが含まれるとのメッセージではどのような状態。 ただし、アクションが成功すると、常にフォームを保存_pMessage_パラメーターが指すメッセージと切り替えの現在の状態の[通常](normal-state.md)の状態にします。 
  
次の表では、 **SaveCompleted**の実装で実行する必要があります操作に影響を与える条件について説明します。
  
|**条件**|**アクション**|
|:-----|:-----|
|_PMessage_パラメーターが NULL と[IPersistMessage::Save](ipersistmessage-save.md)メソッドの_fSameAsLoad_パラメーターが TRUE に設定します。  <br/> |すべての登録されているビューアーの[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。  <br/> |
|_PMessage_パラメーターが NULL と**IPersistMessage::Save**メソッドの_fSameAsLoad_パラメーターが FALSE に設定されています。  <br/> |S_OK ��Ԃ��܂��B  <br/> |
|フォームでは、HandsOffFromNormal 状態にします。  <br/> |現在のメッセージを解放し、 _pMessage_パラメーターで指定されたメッセージに置き換えます。 交換メッセージの[IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出すし、S_OK を返します。  <br/> |
|フォームでは、HandsOffAfterSave 状態にします。  <br/> |すべての登録されているビューアーの**IMAPIViewAdviseSink::OnSaved**メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。  <br/> |
|フォームでは、 [NoScribble](noscribble-state.md)状態にします。  <br/> |現在のメッセージを解放し、 _pMessage_に示されるメッセージに置き換えます。 交換メッセージの**IUnknown::AddRef**メソッドを呼び出します。 すべての登録されているビューアーの**IMAPIViewAdviseSink::OnSaved**メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。  <br/> |
|HandsOff 状態のいずれかでは、フォームと_pMessage_パラメーターは NULL に設定します。  <br/> |E_INVALIDARG を返します。  <br/> |
|フォーム以外 HandsOff 状態のいずれかの状態または状態にある、NoScribble です。  <br/> |E_UNEXPECTED が返されます。  <br/> |
   
ストレージ ・ オブジェクトを保存する方法の詳細については、 [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted)または[IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)のメソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [フォームの状態](form-states.md)
