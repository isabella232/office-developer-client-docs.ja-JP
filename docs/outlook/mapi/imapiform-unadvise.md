---
title: imapiformunadvise
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
  
以前に[imapiform:: アドバイズ](imapiform-advise.md)を呼び出して、フォームビューアーでの通知の登録を取り消します。
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulconnection_
  
> 順番キャンセルする通知登録を識別する接続番号。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録は取り消されました。
    
E_INVALIDARG 
  
> _ulconnection_パラメーターで渡された接続番号は、有効な登録を表していません。 
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiform:: アドバイズ**メソッドを呼び出して、最初に設定された通知の登録**** を取り消します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームビューアーの view アドバイズシンクに対して保持しているポインターを破棄するには、 [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出します。 通常、**リリース**は、**アドバイズ**中止呼び出し中に呼び出されます。 ただし、別のスレッドが、view アドバイズシンクの[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドの1つを呼び出しているプロセス内にいる場合は、 **IMAPIViewAdviseSink**メソッドが戻るまで、 **Release**呼び出しを遅延させます。 
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

