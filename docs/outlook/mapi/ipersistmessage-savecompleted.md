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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317137"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**適用対象**: Outlook 2013 | Outlook 2016 
  
保存操作が完了したことをフォームに通知します。 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>パラメーター

_pmessage_
  
> 順番新しく保存されたメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知は正常に実行されました。
    
E_INVALIDARG 
  
> _pmessage_パラメーターが NULL で、フォームは、[標準] または [[標準](handsofffromnormal-state.md)] [[保存](handsoffaftersave-state.md)の状態] のどちらかです。 
    
E_UNEXPECTED 
  
> フォームが次のいずれかの状態になっていません。
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>解説

**IPersistMessage:: SaveCompleted**メソッドは、すべての保留中の変更が保存されたことをフォームに通知するためにフォームビューアーによって呼び出されます。 **SaveCompleted**は、フォームが次のいずれかの状態にある場合にのみ呼び出す必要があります。 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>実装に関するメモ

**SaveCompleted**メソッドが実行できるアクションには、メッセージポインターパラメーターに含まれる内容と、メッセージの状態によっていくつかあります。 ただし、正常に処理された場合は、 _pmessage_パラメーターが参照しているメッセージの現在の状態を常に保存し、フォームを[通常](normal-state.md)の状態に切り替えます。 
  
次の表では、 **SaveCompleted**の実装で実行する必要がある処理に影響する条件について説明します。
  
|**条件**|**処理**|
|:-----|:-----|
|_pmessage_パラメーターが NULL で、 [IPersistMessage:: Save](ipersistmessage-save.md)メソッドの_fsameasload_パラメーターが TRUE に設定されています。  <br/> |登録されているすべてのビューアーの[IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。  <br/> |
|_pmessage_パラメーターが NULL で、 **IPersistMessage:: Save**メソッドの_fsameasload_パラメーターが FALSE に設定されています。  <br/> |S_OK ��Ԃ��܂��B  <br/> |
|フォームは、[標準時の標準状態にあります。  <br/> |現在のメッセージを解放し、 _pmessage_パラメーターで示されるメッセージに置き換えます。 置換メッセージの[IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出し、S_OK を返します。  <br/> |
|フォームは、[保存の状態にあります。  <br/> |登録されているすべてのビューアーの**IMAPIViewAdviseSink:: onsaved**メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。  <br/> |
|フォームは、 [noscribble](noscribble-state.md)状態にあります。  <br/> |現在のメッセージを解放し、それを_pmessage_で示されるメッセージに置き換えます。 置換メッセージの**IUnknown:: AddRef**メソッドを呼び出します。 登録されているすべてのビューアーの**IMAPIViewAdviseSink:: onsaved**メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。  <br/> |
|フォームは HandsOff 状態のいずれかで、 _pmessage_パラメーターが NULL に設定されています。  <br/> |E_INVALIDARG を返します。  <br/> |
|フォームは、HandsOff 状態または noscribble 状態のいずれでもない状態にあります。  <br/> |E_UNEXPECTED を返します。  <br/> |
   
ストレージオブジェクトの保存の詳細については、 [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted)メソッドまたは[IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)メソッドのマニュアルを参照してください。 
  
## <a name="see-also"></a>関連項目

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [フォームの状態](form-states.md)
