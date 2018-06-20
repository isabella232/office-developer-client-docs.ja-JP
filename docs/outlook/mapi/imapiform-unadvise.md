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
ms.openlocfilehash: 826863e30ae39d3c8d523bd2dff84731bcf16971
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800528"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**適用されます**: Outlook 
  
[IMAPIForm::Advise](imapiform-advise.md)を呼び出すことによって確立されていたフォーム ビューアーを使用して通知の登録をキャンセルします。
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in]キャンセルする通知の登録を識別する接続の数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 登録が取り消されました。
    
E_INVALIDARG 
  
> _UlConnection_パラメーターに渡される接続数は、有効な登録を表していません。 
    
## <a name="remarks"></a>備考

フォームの閲覧者は、 **IMAPIForm::Advise**メソッドを呼び出すことによって最初に確立したことを示す通知の登録をキャンセルする**IMAPIForm::Unadvise**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

破棄するがフォーム ビューアーのビューを保持しているポインターは、その[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、シンクを案内します。 一般に、**リリース**と呼ばれる**Unadvise**の呼び出し中にします。 ただし、 [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドのいずれかのプロセスでは、別のスレッド ビューのシンクをアドバイス、 **IMAPIViewAdviseSink**メソッドが戻るまでに**リリース**の呼び出しを遅延します。 
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)

