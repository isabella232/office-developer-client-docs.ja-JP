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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579488"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[IMAPIForm::Advise](imapiform-advise.md)を呼び出すことによって確立されていたフォーム ビューアーを使用して通知の登録をキャンセルします。
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]キャンセルする通知の登録を識別する接続の数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録が取り消されました。
    
E_INVALIDARG 
  
> _UlConnection_パラメーターに渡される接続数は、有効な登録を表していません。 
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、 **IMAPIForm::Advise**メソッドを呼び出すことによって最初に確立したことを示す通知の登録をキャンセルする**IMAPIForm::Unadvise**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

破棄するがフォーム ビューアーのビューを保持しているポインターは、その[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、シンクを案内します。 一般に、**リリース**と呼ばれる**Unadvise**の呼び出し中にします。 ただし、 [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドのいずれかのプロセスでは、別のスレッド ビューのシンクをアドバイス、 **IMAPIViewAdviseSink**メソッドが戻るまでに**リリース**の呼び出しを遅延します。 
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

