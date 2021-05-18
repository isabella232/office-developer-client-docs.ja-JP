---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329471"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPIForm::Advise](imapiform-advise.md)を呼び出して以前に確立されたフォーム ビューアーを使用して通知の登録をキャンセルします。
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]取り消す通知登録を識別する接続番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が取り消されました。
    
E_INVALIDARG 
  
> _ulConnection_ パラメーターで渡される接続番号は、有効な登録を表すではありません。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIForm::Unadvise** メソッドを呼び出して **、IMAPIForm::Advise** メソッドを呼び出して最初に確立した通知の登録をキャンセルします。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーのビューに保持しているポインターを破棄するには、 [その IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを呼び出します。 通常、 **リリースは** **Unadvise 呼び出し中に呼び出** されます。 ただし、別のスレッドがビューの IMAPIViewAdviseSink メソッドのいずれかを呼び出す過程にある場合は **、IMAPIViewAdviseSink** メソッドが返されるまで Release 呼び出しを遅延します。 [](imapiviewadvisesinkiunknown.md) 
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

